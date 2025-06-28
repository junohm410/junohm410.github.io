# CLAUDE.md

このファイルは、このリポジトリでコードを扱う際のClaude Code (claude.ai/code) へのガイダンスを提供します。

## プロジェクト概要

**HTML Energy運動**にインスパイアされた純粋なHTML/CSS/JS静的サイトです。Jekyll等の静的サイトジェネレータを使用せず、手書きHTMLでシンプルな個人サイトを構築しています。

### 目標
- 自己紹介ページ（TOPページに統合済み）
- 各種SNSやブログへのリンク集
- いくつかの静的な記事ページ
- **HTML Energyの哲学に基づく**シンプルで個人的な表現

## HTML Energy 哲学

このプロジェクトは**HTML Energy運動**にインスパイアされています：

### コア理念
- **即座性**: HTMLに「hello」と書けば「hello」が表示される
- **手書きHTML**: 生のHTMLを直接記述
- **非抽象化**: プログラミングより先に画面で見える
- **個人的表現**: 商業的最適化ではなく純粋な創造欲求

### 技術的特徴
- セマンティックなHTML構造
- インラインスタイリングも使用可能: `style=`や`onclick=`属性
- 最小限の依存関係
- 手作業によるコーディング

## 技術スタック

- **静的HTML/CSS/JavaScript**: フレームワーク不使用
- **ホスティング**: GitHub Pages (junohm410.github.io)
- **コンテンツ言語**: 主に日本語
- **スタイリング**: ミニマルCSS、タイポグラフィ重視
- **フォント**: モノスペース（Courier New等）

## リポジトリ構造

```
/home/junohm410/projects/junohm410.github.io/
├── index.html              # メインページ（自己紹介・リンク・すべて統合）
├── articles/               # 記事ページ
│   └── test.html           # サンプル記事
└── assets/
    ├── css/
    │   └── style.css       # メインCSSファイル
    ├── js/                 # JavaScript用（将来）
    └── images/
        ├── image.png       # TOP画像
        ├── logo.png        # ファビコン
        └── posts/          # 記事用画像
            └── IMG_0586.JPG
```

## 共通コマンド

### 開発・テスト

```bash
# ローカルサーバー（Python）
python -m http.server 8000
# または
python3 -m http.server 8000

# ローカルサーバー（Node.js）
npx serve .

# ローカルでhttp://localhost:8000で確認
```

### Git操作

```bash
# ステータス確認
git status

# GitHub Pagesにデプロイ
git add .
git commit -m "コミットメッセージ"
git push origin main
```

## コンテンツ管理

### メインページ（index.html）
すべてのコンテンツが統合されています：
- 自己紹介
- SNS/ブログリンク
- HTML Energyへの言及

### 新しい記事の作成
1. `/articles/`ディレクトリに新しいHTMLファイルを作成
2. 以下のテンプレートを使用：

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>記事タイトル - shodan</title>
  <meta name="description" content="記事の説明">
  <link rel="shortcut icon" type="image/x-icon" href="/assets/images/logo.png">
  <link rel="stylesheet" href="../assets/css/style.css">
</head>
<body>
  <a href="../index.html">..</a>
  
  <article>
    <p><time datetime="YYYY-MM-DD">YYYY-MM-DD</time></p>
    <h1>記事タイトル</h1>
    <!-- 記事内容 -->
  </article>
</body>
</html>
```

### 画像の追加
- メイン画像: `/assets/images/`
- 記事用画像: `/assets/images/posts/` または `/assets/images/articles/`
- パス例: `<img src="/assets/images/posts/filename.jpg" alt="説明">`

## スタイリング指針

### CSS設計
- **ミニマリズム**: 最小限のスタイル
- **タイポグラフィ重視**: モノスペースフォント、適切な行間
- **レスポンシブ**: max-width使用、モバイル対応
- **色使い**: 控えめなグレースケール中心

### HTML Energy的スタイリング
```html
<!-- インラインスタイルも使用可能 -->
<p style="color: #666; font-style: italic;">特別な文章</p>

<!-- シンプルなHTMLタグでの表現 -->
<p style="text-align: center; font-size: 1.2em; font-weight: bold;">重要な情報</p>
```

## GitHub Pages デプロイメント

`main`ブランチへのプッシュで自動デプロイ：
1. 変更をプッシュ
2. GitHub Pagesが自動ビルド・デプロイ
3. `https://junohm410.github.io/`で公開

## 開発ノート

### HTML Energy 重要原則
- **手作業**: コードは手で書く
- **即座性**: 結果がすぐ見える
- **個性**: 商業的でない個人的表現
- **シンプルさ**: 複雑な抽象化を避ける

### ファイル管理
- HTMLファイルは手動作成
- 画像は`/assets/images/`に配置
- 記事は`/articles/`に配置
- 最小限の構造を維持

### パフォーマンス
- 軽量CSS（ミニマルスタイル）
- 高速読み込み時間
- フレームワーク不使用
- 最小限の依存関係

## 新しいClaude インスタンス向けクイックスタート

1. **プロジェクト理解**: HTML Energy哲学に基づく純粋なHTML静的サイト
2. **技術方針**: 手書きHTML/CSS、フレームワーク不使用
3. **構造理解**: index.html（メイン・すべて統合）、articles/（記事）
4. **スタイリング**: assets/css/style.css、ミニマル＋タイポグラフィ重視
5. **デプロイ**: GitHub Pages自動デプロイ
6. **哲学**: 手作業、即座性、個人的表現を重視

このプロジェクトは**HTML Energy**の精神に基づき、ウェブの根本的な喜びと個人的表現を重視した純粋な静的サイトです。