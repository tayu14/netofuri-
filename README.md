<!-- er図のurl -->
<!-- https://lucid.app/lucidchart/1bb7a81c-4307-4f3f-bdd8-7b89eaece070/edit?beaconFlowId=BDB22C79C2CCB501&page=0_0#?folder_id=home&browser=icon -->

# アプリの概要

ネットフリックスではレビュー機能がないのでレビューで作品を探す人のためにアプリを作った

#　デプロイurl

https://netofuri.herokuapp.com/


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
