# Corn Tycoon 攻略ガイド（pxnas）

`pxnas.com` 用の静的サイト。**Corn Tycoon**（開発：Ctrl4ltDel）の非公式日本語攻略ガイドです。純粋な HTML / CSS / JS で構成され、ビルド不要です。

## 構成（クリーン URL：ディレクトリ式）

```
index.html                 トップページ
blog/index.html            攻略記事一覧
about/index.html           このサイトについて
faq/index.html             よくある質問
glossary/index.html        用語集
community/index.html       コミュニティ
updates/index.html         更新記録
privacy/index.html         プライバシーポリシー
terms/index.html           利用規約
contact/index.html         お問い合わせ
404.html                   404 ページ
sitemap.xml                sitemap
robots.txt                 robots
llms.txt                   AI 検索向けインデックス
assets/css/style.css       全ページ共通スタイル
assets/js/main.js          モバイルメニューなど
favicon.svg                ファビコン
```

## Cloudflare Pages の設定

| 項目 | 値 |
| --- | --- |
| Production branch | `main` |
| Build command | （空欄） |
| Build output directory | （空欄） |

## URL 規約

- 全ページ `.html` 拡張子なしのクリーン URL（ディレクトリ式）。
- 記事は `/blog/{slug}/`（slug は小文字英語・ハイフン区切り・日付なし）。

## 新しい攻略記事の追加方法

1. `blog/{slug}/index.html` を作成。
2. `blog/index.html` の一覧と、`index.html` の最新記事欄、`sitemap.xml` を更新。
3. `main` に push すると Cloudflare Pages が自動デプロイ。

## ローカル確認

```bash
python3 -m http.server 8080
```
