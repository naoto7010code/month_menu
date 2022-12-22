# テーブル設計

## users テーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------- |
| username           | string | null: false               |
| encrypted_password | string | null: false               |
| birthday           | date   | null: false               |

### Association

- has_many :menu

## menus テーブル

| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| user               | references | null: false, foreign_key: true |
| menuname           | string     | null: false                    |
| category_id        | integer    | null: false                    |

### Association

- belongs_to :user

