#### postgresql側

```markdown
# DB作成 CUI
createdb nyasocom

# DB作成 psql内
create database nyasocom;

# dbに接続
psql nyasocom

# postgresユーザ、nyasocomデータベースに接続
psql -U postgres -d nyasocom;

# テーブル作成
CREATE TABLE nyasocom
(id char(15) NOT NULL, url varchar NOT NULL, update varchar NOT NULL, PRIMARY KEY (id));

# データをインポート
\copy nyasocom from '~/nyasocom_pg/web/rss.csv' with csv
```

#### ユーザ/パスワード、設定をしない。 

cd /etc/postgresql/16/main

```markdown
...

# TYPE  DATABASE        USER            ADDRESS                 METHOD
# "local" is for Unix domain socket connections only
local   all             all                                     trust # scram-sha-256

...
```

_クエリの操作が必要、UNIX環境を推奨します_
