docker-compose.ymlファイルの置いてあるディレクトリで実行。

1.Railsのコンテナを起動してRailsのプロジェクトを作成するコマンド
$ docker-compose run web rails new . --force --database=mysql

2.Railsイメージのビルド実行コマンド
$ docker-compose build

3.config/database.ymlの修正内容

default内の項目を修正
password: password
host: db

4.コンテナをデタッチドモード（バックグラウンド）で実行するコマンド
$ docker-compose up -d

5.RailsのコンテナでDB作成のタスクを実行するコマンド
$ docker-compose run web bundle exec rake db:create


参考URL---
https://qiita.com/ftbyu/items/c2db4cbce602b0ad077c

https://teratail.com/questions/193008
