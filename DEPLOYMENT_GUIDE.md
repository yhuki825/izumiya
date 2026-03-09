# いずみや WEBサイト - GitHub & Cloudflare Pages デプロイガイド

## 概要

このガイドでは、いずみやのWEBサイト（単一HTMLファイル）をGitHubにアップロードし、Cloudflare Pagesでデプロイする手順を説明します。

---

## 前提条件

- GitHubアカウント（https://github.com）
- Cloudflareアカウント（https://www.cloudflare.com）
- Git がインストールされていること

---

## ステップ 1: GitHubリポジトリの作成

### 1-1. GitHubにログイン
1. https://github.com にアクセスしてログインします

### 1-2. 新しいリポジトリを作成
1. 右上の「+」アイコン → 「New repository」をクリック
2. リポジトリ名を入力（例：`izumiya-website`）
3. 説明を入力（例：`いずみや太陽光売電事業 WEBサイト`）
4. 「Public」を選択（Cloudflare Pagesでアクセス可能にするため）
5. 「Create repository」をクリック

### 1-3. ローカルマシンでGitを初期化
```bash
# プロジェクトフォルダに移動
cd /path/to/izumiya-website

# Gitを初期化
git init

# ファイルをステージング
git add index.html

# 初回コミット
git commit -m "Initial commit: Izumiya website"

# リモートリポジトリを追加（GitHubで表示されたURLを使用）
git remote add origin https://github.com/YOUR_USERNAME/izumiya-website.git

# メインブランチにリネーム
git branch -M main

# GitHubにプッシュ
git push -u origin main
```

---

## ステップ 2: Cloudflare Pagesへのデプロイ

### 2-1. Cloudflareにログイン
1. https://dash.cloudflare.com にアクセスしてログインします

### 2-2. Pages プロジェクトを作成
1. 左サイドバーで「Pages」をクリック
2. 「Create a project」をクリック
3. 「Connect to Git」を選択

### 2-3. GitHubリポジトリを接続
1. 「GitHub」を選択
2. GitHubアカウントの認可を行う
3. 作成した「izumiya-website」リポジトリを選択
4. 「Begin setup」をクリック

### 2-4. ビルド設定
1. **Project name**: `izumiya-website`（またはお好みの名前）
2. **Production branch**: `main`
3. **Build command**: 空欄のままにする（HTMLファイルのみのため不要）
4. **Build output directory**: `/`（ルートディレクトリ）
5. 「Save and Deploy」をクリック

### 2-5. デプロイ完了
- デプロイが完了すると、Cloudflareから自動的にURLが割り当てられます
- 例：`https://izumiya-website.pages.dev`

---

## ステップ 3: カスタムドメインの設定（オプション）

### 3-1. ドメインをCloudflareに登録
1. Cloudflareダッシュボード → 「Websites」
2. 「Add a site」をクリック
3. ドメイン名を入力
4. Cloudflareのネームサーバーに変更

### 3-2. Pages プロジェクトにドメインを接続
1. Pages プロジェクト → 「Custom domains」
2. 「Set up a custom domain」をクリック
3. ドメイン名を入力
4. 「Continue」をクリック

---

## ステップ 4: 更新とメンテナンス

### ローカルで変更を加える場合
```bash
# ファイルを編集後、以下を実行
git add index.html
git commit -m "Update: 説明"
git push origin main
```

Cloudflare Pagesは自動的にGitHubの変更を検出し、デプロイを開始します。

---

## トラブルシューティング

### デプロイが失敗する場合
1. Cloudflareダッシュボード → Pages → プロジェクト → 「Deployments」で詳細を確認
2. ビルドログを確認し、エラーメッセージを確認

### ドメインが反映されない場合
1. ネームサーバーの変更が反映されるまで最大48時間かかる場合があります
2. DNS設定を確認：https://www.whatsmydns.net/

### ファイルが見つからない場合
1. ファイルがリポジトリのルートディレクトリにあることを確認
2. ファイル名が `index.html` であることを確認

---

## よくある質問

**Q: HTTPSは対応していますか？**
A: はい、Cloudflare PagesはデフォルトでHTTPSに対応しています。

**Q: 複数のHTMLファイルを使用できますか？**
A: はい。ただし、このプロジェクトは単一のindex.htmlで構成されています。

**Q: ページビューやアクセス数を確認できますか？**
A: Cloudflareダッシュボード → Pages → Analytics で確認できます。

---

## サポート

問題が発生した場合：
- Cloudflare サポート：https://support.cloudflare.com
- GitHub サポート：https://support.github.com

---

## 更新履歴

- **2024年3月9日**: 初版作成
- **対応ブラウザ**: Chrome, Firefox, Safari, Edge（最新版）
- **レスポンシブ対応**: モバイル、タブレット、デスクトップ

---

**作成者**: Manus AI  
**最終更新**: 2024年3月9日
