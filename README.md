# Ionic 3 Tutorial

[Ionic 3 Tutorial](https://ionicframework.com/docs/intro/installation/)
をやって見ましょう。

目次

- インストール
- プロジェクトの作成
- アプリの起動
- Ionic Viewへデプロイ
- 参考

## インストール

Install nvm

  ```
  curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
  ```

Install NodeJS 6

  ```
  nvm install 6
  nvm use 6
  ```

Install Ionic

  ```
  npm install -g ionic cordova
  ```

## プロジェクトの作成

`ionic start app tutorial`を実行すると、`app`フォルダーに
Tutorialテンプレートでプロジェクトを新規作成し、git も初期化してくれる親切さです。

途中で、
`? Link this app to your Ionic Dashboard to use tools like Ionic View?`
と質問される時は `Y` と回答しましょう。

次のような画面出力になります。

  ```
  $ ionic start app tutorial
  ✔ Creating directory ./app - done!
  [INFO] Fetching app base (https://github.com/ionic-team/ionic2-app-base/archive/master.tar.gz)
  ✔ Downloading - done!
  [INFO] Fetching starter template tutorial
       (https://github.com/ionic-team/ionic2-starter-tutorial/archive/master.tar.gz)
  ✔ Downloading - done!
  ✔ Updating package.json with app details - done!
  ✔ Creating configuration file ionic.config.json - done!
  [INFO] Installing dependencies may take several minutes!
  > npm install
  ✔ Running command - done!
  > npm install --save-dev --save-exact @ionic/cli-plugin-ionic-angular@latest
  ✔ Running command - done!
  > git init
  ✔ Running command - done!
  > git add -A
  ✔ Running command - done!
  > git commit -m "Initial commit" --no-gpg-sign
  ✔ Running command - done!

  ♬ ♫ ♬ ♫  Your Ionic app is ready to go! ♬ ♫ ♬ ♫

  Run your app in the browser (great for initial development):
  ionic serve

  Run on a device or simulator:
  ionic cordova run ios

  Test and share your app on a device with the Ionic View app:
  http://view.ionic.io

  ? Link this app to your Ionic Dashboard to use tools like Ionic View? Yes

  You will need to login in order to link this app. Please run the following commands to do so.
  ionic login - login first
  ionic link - then link your app

  Go to your newly created project: cd ./app
  ```

## アプリの起動

ローカルでアプリを起動して、ブラウザー内で確認するには

  ```
  cd app
  ionic serve
  ```

iOS版を確認するには(XCode command line developer toolsが必要)

  ```
  ionic cordova platform add ios
  ionic cordova run ios
  ```

Android版も同様です (Android SDKが必要)。

## Ionic Viewへデプロイ

## デプロイ準備
[Ionic View](http://view.ionic.io/)へデプロイすることによって
iOSやAndroid端末で簡単に確認することができるようになります。

まず[Ionicアカウントを作成](https://apps.ionic.io/signup)してから、
ローカルに戻ってログインし、アプリを Ionic Viewへリンクします。

  ```
  ionic login
  ionic link
  ```

### デプロイ実施！

  ```
  ionic upload --deploy production
  ```

## 参考

- [Ionic Tutorial](https://ionicframework.com/docs/intro/tutorial/)
- [Install Node.js for Debian based Linux](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
