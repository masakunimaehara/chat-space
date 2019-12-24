## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, index: true|
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
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|string||
|text|text||
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user












