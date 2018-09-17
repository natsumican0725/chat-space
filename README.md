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
|name|integer|null: false|
|e-mail|integer|null: false, foreign_key: true|
|image|string|foreign_key: true|

### Association
- has_many :members
- has_many :messages

##groupテーブル
|Column|Type|Options|
|------|----|-------|
|name|integer|null: false|

### Association
- has_many :members
- has_many :messages

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
