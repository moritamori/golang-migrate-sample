# 環境変数: POSTGRESQL_URLを設定する

# データベース作成
```sh
$ psql postgres
```

```sql
CREATE DATABASE sample;
```

# バージョンを１つあげる（ユーザーテーブルを作る）
```sh
$ migrate -path db/migrations -database ${POSTGRESQL_URL} up 1
```

# バージョンを１つさげる（ユーザーテーブルを削除）
```sh
$ migrate -path db/migrations -database ${POSTGRESQL_URL} down 1
```

# 未実行のマイグレーションを全て実行（ユーザーテーブル、コメントテーブルを作成）
```sh
$ migrate -path db/migrations -database ${POSTGRESQL_URL} up
```

