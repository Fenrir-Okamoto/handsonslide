# Fenrir Handson
## Web2017

2017/10/7 Fenrir Inc.

---

### アジェンダ

- はじめに
- SPA/PWA の話
- ハンズオン

---

# はじめに

---

## 自己紹介

---

### 藤田周

- 主な仕事内容
    - バックエンド/フロントエンドエンジニア
- フェンリル歴
    - 1年以上
- 得意言語
    - PHP, AngularJS, Angular, TypeScript
- 趣味
    - 筋トレ, バーめぐり

---

### 岡本拓也

- 主な仕事内容
    - フロントエンドエンジニア/PM
- フェンリル歴
    - 1年半以上
- 得意言語
    - AngularJS, SASS, Javascript(ES2015)
- 趣味
    - 音楽鑑賞, ゲーム

---

## この会の概要

- 最近のフロントエンド動向を感じてもらう会
- フェンリルの技術を感じてもらう会

---

## フェンリルとは

https://www.fenrir-inc.com/jp/works/

---

## みん撃 名刺MAKER

---?image=https://raw.githubusercontent.com/Fenrir-Okamoto/handsonslide/master/images/job02.png&size=auto 90%

---

## JR西日本　列車走行位置

---?image=https://raw.githubusercontent.com/Fenrir-Okamoto/handsonslide/master/images/job01.png&size=auto 90%

---

## 対象者

- Web アプリ開発に興味のある方
- Web エンジニアに興味のある方
- 最近の Web フレームワークに興味のある方
- SPA に興味のある方
- PWA に興味のある方

---

## タイムテーブル

時刻  | 内容 | 備考
--- | --- | ---
11:00 - 11:10 | はじめに    | -
11:10 - 11:40 | SPA/PWA の話  | -
11:40 - 12:30 | ハンズオン１  | -
12:30 - 13:30 | 休憩  | -
13:30 - 15:00 | ハンズオン２  | -
15:00 - 16:30 | ハンズオン３  | -
16:30 - 17:00 | まとめ | -
17:00 - 19:00 | 懇親会 | -

---

# SPA/PWA の話

---

## SPA とは何か

> シングルページアプリケーション（英: single-page application、SPA）とは、    
単一のWebページのみから構成することで、デスクトップアプリケーションのようなユーザ体験を提供するWebアプリケーションまたはWebサイトである。    
必要なコード（HTML、JavaScript、CSS）は最初にまとめて読み込むか[1]、ユーザの操作などに応じて動的にサーバと通信し、必要なものだけ読み込みを行う。

引用: wikipedia

スマホアプリみたいに画面遷移がスムーズ

---

## SPA の技術要素

- JavaScriptフレームワーク
- Ajax
- WebSocket
- Server-sent events

など

引用: wikipedia

---

## PWA とは何か

> 信頼性 - 不安定なネットワーク状況であっても、即座にロードし、ダウンサウルスを表示しません。    

引用: Google Developers を google 翻訳

---

## PWA とは何か

> 高速 - スムーズなアニメーションでスムーズなアニメーションや、スクロールが不要なユーザーとのやりとりに迅速に対応します。    

引用: Google Developers を google 翻訳

---

## PWA とは何か

> エンゲージメント - 没入型ユーザーエクスペリエンスを備えた、デバイス上の自然なアプリのような感じ。

引用: Google Developers を google 翻訳

よりスマホアプリに近い表現を行う

---

## PWA デモ

- スプラッシュスクリーンが出る！
- chrome のヘッダがない！
- 画面遷移がスムーズ！

https://www.flipkart.com/

---

## 今回つくるもの

画像閲覧サービス    
「Fenridge(仮名)」

※Fenrir Image をもじったもの。ドイツ語でフィンランド

---

### 技術要素

- プロダクト
    - HTML5/CSS
    - Vue.js
    - Bootstrap
    - Flickr API
    - Lodash
    - jsonp

- 開発
    - vue-cli
    - Node.js

---

## Vue.js とは何か

> "Vue.js"（ヴュージェイエス）は、Webアプリケーションにおけるユーザーインターフェイスを構築するための、オープンソースのJavaScriptフレームワークである[4]。他のJavaScriptライブラリを使用するプロジェクトへの導入において、容易になるように設計されている。一方で高機能なシングルページアプリケーション（SPA）を構築することも可能である。

引用: wikipedia

---

### 画面イメージ

一覧ページ

---?image=https://raw.githubusercontent.com/Fenrir-Okamoto/handsonslide/master/images/top.png&size=auto 90%

---

### 画面イメージ

詳細ページ

---?image=https://raw.githubusercontent.com/Fenrir-Okamoto/handsonslide/master/images/detail.png&size=auto 90%

---

### 機能

- 48件 画像一覧
- クリックした画像の詳細情報

これらを SPA で！ PWA を意識して！
実装する。

---

### Vue.jsとは

ユーザーインターフェイスを構築するためのプログレッシブフレームワーク

- 学習コストが低い
- 既存サービスにも導入できる

---

# ハンズオン

---

## 作業内容

- 環境構築
- 共通ヘッダをつくる
- ナビゲーションをつくる
- 画像一覧をつくる
- お気に入り登録を作る
- 詳細ページをつくる

---

## 環境構築

---

```
cd お好きなディレクトリ/
git clone https://github.com/Fenrir-Okamoto/FenrirHandsonWeb2017.git
cd FenrirHandsonWeb2017/fenridge/
npm install
```

---

## ディレクトリ構成の確認

```
├── README.md
├── build
│   ├── build.js
│   ├── check-versions.js
│   ├── dev-client.js
│   ├── dev-server.js
│   ├── utils.js
│   ├── vue-loader.conf.js
│   ├── webpack.base.conf.js
│   ├── webpack.dev.conf.js
│   └── webpack.prod.conf.js
├── config
│   ├── dev.env.js
│   ├── index.js
│   └── prod.env.js
├── index.html
├── package.json
├── src
│   ├── App.vue
│   ├── assets
│   ├── components
│   ├── main.js
│   └── router
└── static
```

---

## ローカルサーバーを起動する

```
npm run dev
```

ブラウザで `http://localhost:8080` へアクセス

---

## エディタでひらく

`FenrirHandsonWeb2017/fenridge/` 以下をエディタで開こう

---

## PWA の アップシェルを作る

---

## 共通ヘッダを作ろう

---

## ナビゲーションを作ろう

--- 

## 画像一覧ページをつくろう

---

## Flickr API から画像一覧を取得しよう

---

## 画像一覧にスタイルを設定しよう

---

## ルーティングを作ろう

---

## 詳細ページをつくろう

---

## Flickr API から画像詳細を取得しよう

---

## 詳細ページにスタイルを設定しよう

---

## 自分で機能をつくってみよう

- お気に入り登録
- お気に入り一覧ページ
