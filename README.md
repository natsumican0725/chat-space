## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false|
|e-mail|integer|null: false, foreign_key: true|
|body|text|foreign_key: true|
|image|string|foreign_key: true|

### Association
- belongs_to :group
- has_many :members
- has_many :messages

##groupテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|name|integer|null: false|

### Association
- has_many :members
- has_many :messages
- has_many :users

##messageテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|body|text|foreign_key: true|
|name|integer|null: false|
|image|string|foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
- belongs_to :member