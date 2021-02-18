# テーブル設計

## users テーブル

| Column              | Type   | Options     |
| ------------------- | ------ | ----------- |
| nick_name           | string | null: false |
| first_name          | string | null: false |
| family_name         | string | null: false |
| email               | string | null: false |
| encrypted_password  | string | null: false |

### Association

- has_many : reviews
- has_many : comments

## reviews

| Column                 | Type       | Options     |
| ---------------------- | ---------- | ----------- |
| title                  | string     | null: false |
| review                 | text       | null: false |

### Association

- belongs_to : user
- has_many   : comments

## comments

| Column    | Type | Options    |
| --------- | ---- | ---------- |
| comments  | text | null:false |

### Association

- belongs_to : user
- belongs_to : reviews
