# FASTAPIのテンプレート

## 環境構築

### docker build+run
docker-composeが存在するディレクトリ化で、下記を実行することでbuildされて、runされる。

`docker compose up -d`

`docker compose down `

## サーバー起動

### FASTAPIのサーバー起動方法
Mainが存在するディレクトリ化で、下記のコードによりサーバー起動

`uvicorn main:app --host 127.0.0.1 --port 8000 --reload`

### docker環境でサーバー起動方法
docker-composeの存在するディレクトリ化で、下記のコードでDcoker上の環境でサーバー起動

-pは「ホストPCの8000番ポートへの通信は全てコンテナの3000番ポートへ流す」という意味：https://qiita.com/progra_dango/items/a115bc038c45879df83f

`docker-compose run　-p 8000:8000 python3 uvicorn main:app --host 127.0.0.1 --port 8000 --reload `

### docker上のpython環境へ入る
`docker compose exec python3 bash`

### pip install
requirements.txtに追加して、imagesを削除して再度buildする。
