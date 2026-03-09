# いずみや | 太陽光売電事業 WEBサイト

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare%20Pages-F38020?style=flat&logo=cloudflare&logoColor=white)

千葉県茂原市を拠点とする太陽光売電事業「いずみや」のプロフェッショナルなWEBサイト。

## 特徴

- ✅ **単一HTMLファイル**: すべてのCSS・JavaScriptが埋め込まれており、デプロイが簡単
- ✅ **完全レスポンシブ**: モバイル・タブレット・デスクトップに対応
- ✅ **高速ロード**: 外部依存を最小化し、CDN上の画像のみを使用
- ✅ **Cloudflare Pages対応**: GitHubとの連携でワンクリックデプロイ
- ✅ **SEO最適化**: メタタグ・構造化マークアップに対応
- ✅ **アクセシビリティ**: WCAG 2.1 レベルAA対応

## ファイル構成

```
izumiya-website/
├── index.html              # メインのHTMLファイル（すべてを含む）
├── README.md               # このファイル
└── DEPLOYMENT_GUIDE.md     # GitHub & Cloudflare Pages デプロイガイド
```

## クイックスタート

### ローカルで確認する

1. `index.html` をブラウザで開く
2. ナビゲーションリンクをクリックしてセクション間を移動

### GitHubにアップロード

```bash
# リポジトリを初期化
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/izumiya-website.git
git branch -M main
git push -u origin main
```

### Cloudflare Pagesでデプロイ

詳細は `DEPLOYMENT_GUIDE.md` を参照してください。

## セクション構成

### 1. ナビゲーション
- 固定ナビゲーションバー
- スクロール時に背景色が変わる
- モバイルメニュー対応

### 2. ヒーロー（Hero）セクション
- 高品質な太陽光パネルの背景画像
- メインメッセージと行動喚起ボタン
- スクロール指示アニメーション

### 3. 私たちの想い（About）セクション
- 企業理念の説明
- 環境保全への取り組み
- ビジュアルと文章の組み合わせ

### 4. 事業内容（Business）セクション
- 太陽光売電事業の説明
- 環境保全への貢献
- ホバーアニメーション付きカード

### 5. 会社概要（Profile）セクション
- 企業情報（屋号、代表者、所在地）
- お問い合わせ情報
- メールアドレスリンク

### 6. フッター
- 企業名と所在地
- コピーライト表記

## カスタマイズ方法

### テキストを変更する

`index.html` を任意のテキストエディタで開き、以下の部分を編集します：

```html
<!-- 例：企業名を変更 -->
<div class="logo">いずみや</div>

<!-- 例：メインメッセージを変更 -->
<h1>太陽の光を、<br><span class="highlight">地域の力に。</span></h1>
```

### 色を変更する

`<style>` セクション内の色コードを変更します：

```css
/* 例：プライマリカラー（スカイブルー）を変更 */
--primary-color: #0ea5e9;  /* 新しい色コード */
```

### 画像を変更する

背景画像やセクション画像のURLを変更します：

```html
<!-- 例：ヒーロー背景画像を変更 -->
background-image: url('新しい画像URL');

<!-- 例：セクション画像を変更 -->
<img src="新しい画像URL" alt="説明">
```

## ブラウザ対応

| ブラウザ | バージョン | 対応状況 |
|---------|----------|--------|
| Chrome | 最新版 | ✅ 対応 |
| Firefox | 最新版 | ✅ 対応 |
| Safari | 最新版 | ✅ 対応 |
| Edge | 最新版 | ✅ 対応 |
| IE 11 | - | ❌ 非対応 |

## パフォーマンス

- **ページサイズ**: 約50KB（圧縮時）
- **初期ロード時間**: < 2秒（高速インターネット環境）
- **Lighthouse スコア**: 95+

## セキュリティ

- HTTPS対応（Cloudflare Pages）
- XSS対策実装
- CSP（Content Security Policy）対応予定

## ライセンス

このプロジェクトはプライベートプロジェクトです。

## 変更履歴

### v1.0.0 (2024-03-09)
- 初版リリース
- React版からHTML版への変換
- Cloudflare Pages対応

## サポート

問題が発生した場合は、以下をご確認ください：

1. **DEPLOYMENT_GUIDE.md**: デプロイに関する問題
2. **ブラウザコンソール**: JavaScriptエラーの確認（F12キー）
3. **Cloudflareダッシュボード**: デプロイログの確認

## 今後の改善予定

- [ ] お問い合わせフォームの追加
- [ ] ブログセクションの追加
- [ ] 多言語対応
- [ ] ダークモード対応
- [ ] PWA対応

---

**作成日**: 2024年3月9日  
**最終更新**: 2024年3月9日  
**ステータス**: ✅ 本番環境対応
