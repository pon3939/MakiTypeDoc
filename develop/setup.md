# 開発環境セットアップ手順

Node.jsのバージョン管理のためにnodistをインストールする

nodistのパッケージ管理にはChocolateyを使用する

## Chocolatey

[参考](https://chocolatey.org/install)

管理者権限のPowerShellを起動

```ps
# 必要に応じて実行ポリシーを変更する
Set-ExecutionPolicy RemoteSigned

# インストール
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

## nodist

[参考](https://github.com/nullivex/nodist#installation)

```ps
choco install nodist

# インストール後、パスを通すために一度ターミナルを再起動
# 下記でバージョンが表示されればOK
nodist -v

# とりあえずグローバルに最新をインストール
nodist 15.5.0
nodist npm 7.3.0
```

## Visual Studio Code

下記の拡張機能推奨

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## MakiType

[Makitype](https://github.com/pon3939/MakiType)をクローン
下記のコマンドで起動する

```ps
npm install
npm start
```
