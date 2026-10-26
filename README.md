# linux-nginx-practice
## Linux / Nginx 学習記録  
### 概要  
Ubuntu（WSL 2）環境でLinuxの基本操作を学び、Nginxを使ってHTMLページの配信を行いました。  
### 使用環境  
- ホストOS：Windows 11
- Linux実行環境：WSL 2
- Linuxディストリビューション：Ubuntu 26.04.1 LTS
- Webサーバー：Nginx 1.28.3
### 実施した内容
- Linuxの基本コマンド操作
- ファイル・ディレクトリの作成と操作
- ファイルのアクセス権限の確認
- Nginxのインストールと起動状態の確認
- HTMLファイルの作成とWeb配信
- HTTPステータスコードの確認
- Nginxのアクセスログ・エラーログの確認
- Nginx設定ファイルの確認と構文チェック
### 作成したファイル
- [index.html](./index.html)：Ngiinxで配信した自作HTMLページ
### 動作確認に使用したコマンド  
#### Nginxの稼働状態を確認
```bash
sudo systemctl status nginx
```
#### ローカルWebページのHTMLを取得
```bash
curl -s http://localhost/  
```  
#### HTTPステータスコードを確認
```bash
curl -s -o /dev/null -w "HTTP status: %{http_code}\n" http://localhost/
```
#### アクセスログ・エラーログを確認
```bash
sudo tail -n 10 /var/log/nginx/access.log
sudo tail -n 10 /var/log/nginx/error.log
```
#### Nginx設定ファイルの構文をチェック
```bash
sudo nginx -t
```
