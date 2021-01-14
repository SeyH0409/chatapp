# テーブル設計

## users テーブル

| Column  | Type   | Options     |
| ------- | ------ | ----------- |
| name    | string | null: false |
| email   | string | null: false |

## rooms テーブル

| Column | type    | Options     |
| ------ | ------- | ----------- |
| name   | string  | null: false |

## room_users テーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| users  | references | null: false, foreign_key: true |
| rooms  | references | null: false, foreign_key: true |

## messages テーブル

| Column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| content | string     |                                |
| user    | references | null: false, foreign_key: true |

### Association

- belongs_to :room
- belongs_to :user