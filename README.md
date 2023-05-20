# 職務経歴書

## 基本情報

|key|value|
|---|---|
|氏名|荒木 裕登|
|ふりがな|あらき ゆうと|
|生年月日|1992年1月1日|
|居住地|東京|
|最終学歴|明治大学食料環境政策学科卒|
|GitHub| <a src="https://github.com/ucho456" target="_blank">https://github.com/ucho456</a> |

<br /><br />

## 保有スキル
#### 言語
###### Javascript 4年, Typescript 3年

#### フロントエンドフレームワーク
###### Next.js v13 1年, Vue.js v2 3年

#### バックエンドフレームワーク
###### Node.js (Express 3年, Nest.js 1年)

#### データベース
###### MySQL 3年, PostgreSQL 1年

#### インフラ
###### GCP

<div style="page-break-before:always"></div>
<br /><br />

## 職務経歴詳細

## 株式会社EARTHBRAIN（2022/11 ~ 現在）

### 

### 技術スタック
Typescript, Node.js(FW: Nest.js, ORM: Prisma), Next.js, Storybook, PostgreSQL, Docker, GCP

Slack, Jira, Notion, Miro, Box, Gather, Figma

### 概要
動物病院が業務に必要な機能がシームレスに使用できるクラウド型のレセプトコンピューターサービスの新規開発に携わっていました。主な機能として従業員の勤怠管理、スケジュール管理、予約、電子カルテ、会計、保険請求、データ分析などがあります。

### チーム構成
テックリード1名、コーダー4名の5名体制。

### 担当した役割
バックエンド開発・フロントエンド設計、開発、コードレビューを担当しました。

### 発揮したバリュー
### 取り組み１：フロントエンドの設計
#### 課題と背景
OAuth2.0の認可サーバーのフロントエンド設計・開発を行いました。
1. タイムラグが存在する為、その際にデータの整合性を保つ為にエラーを出す必要があった。
2. 無駄なリクエストが発生しており、通信費用が嵩む。

#### 対応
Web Socketの仕組みを使用できるSocket.ioを導入し、非同期双方向通信を実現した。これによりサーバー側のデータ変更をトリガーにフロントへ更新情報を伝える事が可能になった。導入にあたり工夫した点としてはSocket通信専用のサーバーを立てたこと。Web Socketはステートフル通信であり、Webアプリと接続を維持し続ける必要があるが、セッションの生存時間が長い為、その間はリソースを専有してしまう事になる。それによる負荷がかからないように別サーバーでの実装とした。

#### 成果
1. リアルタイム同期により不必要なエラーを削減
2. 必要最低限のリクエストで済むようになり、通信費削減

### 取り組み２：コンポーネントのパッケージ化とStorybookでカタログ化
#### 課題と背景
フロントエンドチームのデザインを合わせる為にコードを見せて頂いたが、、、、

#### 対応
GitHub packagesを使用してコンポーネントをパッケージ化しました。これによりコードの単一化、デザインの統一ができました。またStorybookを導入し、コンポーネントのカタログを作り

#### 成果
1. 型が分からない事で起きる不具合修正などのボトルネック解消の基盤を作った。
2. 型システムの恩恵やエディタの入力補完を受けられるようになった。

<div style="page-break-before:always"></div>
<br /><br />

## 会社名：ピクオス株式会社（2019/11〜2022/10）

### プロジェクト名：動物病院向けクラウド型レセコンサービスの開発

### 技術スタック
Javascript, Typescript, Vue.js v2, Node.js(FW: Express, ORM: Sequelize), MySQL, GCP

Teams, Trello

### 概要
動物病院が業務に必要な機能がシームレスに使用できるクラウド型のレセプトコンピューターサービスの新規開発に携わっていました。主な機能として従業員の勤怠管理、スケジュール管理、予約、電子カルテ、会計、保険請求、データ分析などがあります。

### チーム構成
テックリード1名、コーダー4名の5名体制。

### 担当した役割
基本設計・詳細設計・フロントエンド開発・バックエンド開発・コードレビュー

### 発揮したバリュー
### 取り組み１：非正規化によるDB設計の改善
#### 課題と背景
１つの医院アカウントを複数の医師が使用するシステムの都合上、データをリアルタイムで共有する必要があった。当時その方法としてフロント側でCron処理を行い1分毎にリクエストを発行し、最新データを取得するという仕組みを採用していた為、以下のような問題が発生していた。
1. タイムラグが存在する為、その際にデータの整合性を保つ為にエラーを出す必要があった。
2. 無駄なリクエストが発生しており、通信費用が嵩む。

#### 対応
Web Socketの仕組みを使用できるSocket.ioを導入し、非同期双方向通信を実現した。これによりサーバー側のデータ変更をトリガーにフロントへ更新情報を伝える事が可能になった。導入にあたり工夫した点としてはSocket通信専用のサーバーを立てたこと。Web Socketはステートフル通信であり、Webアプリと接続を維持し続ける必要があるが、セッションの生存時間が長い為、その間はリソースを専有してしまう事になる。それによる負荷がかからないように別サーバーでの実装とした。

#### 成果
1. リアルタイム同期により不必要なエラーを削減
2. 必要最低限のリクエストで済むようになり、通信費削減

### 取り組み３：TypeScript導入と差し替えの基盤づくり
#### 課題と背景
Javascriptのままだとサービスが大きくなるにつれてデバックの困難さなどで、特に修正作業に時間が掛かったり、別のバグを生んでしまったりと多大なコストがかかっていた。大型アップデートが落ち着いた所でテックリードに提案し実装をさせてもらえる事になった。

#### 対応
バックエンドのNode.jsから移行作業を行いました。移行にあたり苦労したのは、サービスの根幹部から移行していかないと連鎖的にコンパイルエラーが発生してしまうので、エンドポイントを一つTypescript化させるまで長かった。2週間ほど工程はかかったが一つのAPIエンドポイント丸々TypeScript化させる事ができ、移行作業の基盤を作る事ができた。

#### 成果
1. 型が分からない事で起きる不具合修正などのボトルネック解消の基盤を作った。
2. 型システムの恩恵やエディタの入力補完を受けられるようになった。

<div style="page-break-before:always"></div>
<br /><br />

## 業務外

## 【個人開発】
