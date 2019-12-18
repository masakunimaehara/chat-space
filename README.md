## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|s|null: false|
|username|string|null: false|
|password|string|null: false|
|email|string|null: false|
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
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|text||
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|










