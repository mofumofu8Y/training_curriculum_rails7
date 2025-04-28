##テーブル設計
### users テーブル

| カラム名   | データ型 | NULL許可 | 主キー | 外部キー | 説明             |
|------------|----------|----------|--------|----------|------------------|
| id         | integer  | NOT NULL |        |          | ユーザーID       |
| name       | string   | NOT NULL |        |          | ユーザー名       |
| email      | string   | NOT NULL |        |          | メールアドレス   |
| password   | string   | NOT NULL |        |          | パスワード       |
| created_at | datetime | NOT NULL |        |          | 作成日時         |
| updated_at | datetime | NOT NULL |        |          | 更新日時         |

---

### posts テーブル

| カラム名   | データ型 | NULL許可 | 主キー | 外部キー      | 説明             |
|------------|----------|----------|--------|---------------|------------------|
| id         | integer  | NOT NULL |        |                  | 投稿ID           |
| title      | string   | NOT NULL |        |               | タイトル         |
| body       | text     | NOT NULL |        |               | 本文             |
| user_id    | integer  | NOT NULL |        |               | 投稿者のユーザーID |
| created_at | datetime | NOT NULL |        |               | 作成日時         |
| updated_at | datetime | NOT NULL |        |               | 更新日時         |

---

### comments テーブル

| カラム名   | データ型 | NULL許可 | 主キー | 外部キー              | 説明                 |
|------------|----------|----------|--------|-----------------------|----------------------|
| id         | integer  | NOT NULL |        |                       | コメントID           |
| content    | text     | NOT NULL |        |                       | コメント本文         |
| user_id    | integer  | NOT NULL |        |                       | コメント投稿者ID     |
| post_id    | integer  | NOT NULL |        |                       | 対象の投稿ID         |
| created_at | datetime | NOT NULL |        |                       | 作成日時             |
| updated_at | datetime | NOT NULL |        |                       | 更新日時             |
