# README

B3 のワークショップで用いるサンプルコード

# 起動手順

## 0. リポジトリをフォークする。
###　1. Fork するリポジトリを開く

先生が指定したリポジトリ（https://github.com/r-nakashio/workshop/tree/workshop2025）にアクセスします。

###　2. 右上の「Fork」ボタンを押す

GitHub のリポジトリページ右上に Fork ボタン があります。

###　3. Fork 先を選ぶ

自分の GitHub アカウントを選びます。

mainブランチのみforkしますか？のチェックを外す。

リポジトリ名を変更したい場合はここで編集できます（通常はそのままでOK）。


## 1. Codespacesを起動する

###　1.リポジトリページの右上にある緑色の 「Code」 ボタンをクリックします。

###　2.「Codespaces」 タブに切り替えて、「Create codespace on main」 をクリックします。

少し時間がかかります。


## 2. TapyrusAPI の準備

クライアント証明書のPKCS12ファイルを配置します。
階層は以下のようになります。

```
- myapp
|-- app
|-- bin
|-- config
....
|-- tapyrus_api_client_cert.p12
```
### 1.1. クライアント証明書

Google ドライブで共有する `tapyrus_api_client_cert.p12` を `myapp` ディレクトリに置きます。

TapyrusAPI のクライアント証明書は API 利用のための認証情報になります。

### 1.2. アクセストークン, TapyrusAPI エンドポイント, クライアント証明書のパスフレーズ

```bash
cp .env.sample .env
```
注意点：bashとcodespaces:serverというターミナルが開くが、bashの方で実行すること。

`.env`ファイルを編集します。  
アクセストークン, TapyrusAPI エンドポイント, クライアント証明書のパスフレーズはハンズオン時にお伝えします。  

###　1.3. 設定したファイルを読み込ませる
crtl+shift+pを押してrebuildと入力し、codespaces: Rebuild Containerを選択する。

緑色のRebuildボタンを押す。

再ビルドされ設定ファイルが読み込まれます。

## 3. Web App を起動する

ターミナルのcodespaces:serverにてサーバーが起動しているので、URLにアクセスする。

# ワーク

1. [Work1 スクリプトの作成](doc/work1.md)
1. [Work2 ウェブアプリの作成](doc/work2.md)
