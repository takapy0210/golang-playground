# golang-playground

Go言語を実行できる環境をDockerで構築しています.  
VSCodeのDevcontainer(Remote Container)機能を使って、コンテナ内部で開発・実行することも可能です.

## composeで実行

```sh
cd container
# ビルド
docker compose build

# 実行
docker compose up go-app
```

## Dev Containerを使う方法

- VSCodeのdev container機能を使ってコンテナに接続後、以下コマンドを実行する

```sh
cd container/app
go run main.go

# バイナリを生成して実行する場合
go build main.go
./main
```
