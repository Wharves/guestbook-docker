# Symfony5系 + MySQL8.0 + Docker 環境構築
## 要件(Homebrewにてインストール)
* git
```
brew install git

git --version
```
* Docker
```
brew install docker
brew cask install docker

docker -v
docker-compose -v
```
## 作業手順
### プロジェクトをクローン
```
git clone git@github.com:monjara/symfony-docker.git
```
### Dockerfile docker-compose.yml default.conf 内のプロジェクト名変更
各ファイル内のsymfony-appを任意のプロジェクト名に変更
### docker 立ち上げ
```
docker-compose up -d
```
### カウントディレクトリのパスを確認
```
docker-compose exec php pwd
```
### プロジェクト作成
```
docker-compose exec php composer create-project symfony/website-skelton .
```