## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, index|
|password|string|null: false|
 ### Association
 - has_many :messages
 - has_many :group_users
 - has_many :groups, through::group_users 


 ## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association
- has_many :users, through::group_users
- has_many :group_users
- has_many :messages


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text|null: false|
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|

## photos_tagsテーブル
|Column|Type|Options|
|------|----|-------|
|image|string||










