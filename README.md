# docker-lamp

## Dockerコマンド

```bash
# Dockerイメージのビルド
$ docker-compose build
# コンテナを起動
$ docker-compose up -d
# コンテナを停止
$ docker-compose stop
# コンテナを削除
$ docker-compose down
# コンテナを削除 (データベース込)
$ docker-compose down --volumes
```


## アクセス確認

`http://localhost/index.html`

`http://localhost/info.php`


## MySQL動作確認

```bash
# mysqlのコンテナでbashを実行
$ docker exec -it docker-lamp_mysql_1 bash
# mysqlへログイン
$ mysql -u root -p
```

```mysql
# Version表示
mysql> select version();
# 終了
mysql> quit
```

### phpMyAdmin

`http://localhost:8080`


## 参考

- [Docker Desktop for WindowsをWSL2で使う](https://codeaid.jp/blog/docker-windowswsl2/)
- [Docker Composeを使ってLAMP環境を作る](https://codeaid.jp/blog/docker-lamp/)