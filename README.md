# テーブル設計

## users テーブル

| Column        　　　　　　      | Type     | Options     |
| --------      　　　　　　      | ------   | ----------- |
| email         　　　　　　      | string   | null: false |
| encrypted_password            | string   | null: false |
| name      　　　　　　    　　　 | string   | null: false |

### Association
-has_many :lists


## lists テーブル

| Column             | Type       | Options     |
| ------             | ------     | ----------- |
| title              | string     | null:false  |
| user               | references | null:false, foreign_key: true |

### Association

-belongs_to :user
-has_many :cards
  

## cards テーブル

| Column         | Type       | Options     |
| ------         | ---------- | ------------|
| title          | string     | null:false  |
| memo           | text       | null:false  |
| list           | references | null:false, foreign_key: true  |

### Association
-belogs_to :list




