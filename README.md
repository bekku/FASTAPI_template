# FASTAPI_template
FASTAPIのテンプレートです。

### Mainが存在するディレクトリ化で、下記のコードによりサーバーを実行
`uvicorn main:app --host 127.0.0.1 --port 8000 --reload`

### docker-composeの存在するディレクトリ化で、下記のコードでDcoker上の環境でサーバーを実行
-pはホストPCの8000をdockerの8000へ流す意味：https://qiita.com/progra_dango/items/a115bc038c45879df83f

`docker-compose run　-p 8000:8000 python3 uvicorn main:app --host 127.0.0.1 --port 8000 --reload `

### docker上のpython環境へ入る
`docker compose exec python3 bash`

### pip install
requirements.txtに追加して、imagesを削除して再度buildする。
