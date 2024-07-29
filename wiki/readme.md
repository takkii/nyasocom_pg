#### データの入れ子。

```markdown
# db作成
createdb nyasocom

# dbに接続
psql nyasocom 

# テーブル作成
CREATE TABLE nyasocom
(id char(15) NOT NULL, url varchar NOT NULL, update varchar NOT NULL, PRIMARY KEY (id));

# データをインポート
\copy nyasocom from '~/nyasocom_pg/web/rss.csv' with csv
```

_DB操作が必要_
