# pxnas — ゲーム攻略ガイドサイト

`pxnas.com` 用の静的サイト（ゲーム攻略ガイド）。純粋な HTML / CSS / JS で構成され、ビルド不要です。

## 構成

```
index.html                トップページ
guides/
  index.html              攻略一覧ページ
  sample-guide-1.html     攻略記事のサンプル①
  sample-guide-2.html     攻略記事のサンプル②
privacy.html              プライバシーポリシー
about.html                運営者情報（About Us）
terms.html                利用規約（Terms）
404.html                  404 ページ
assets/
  css/style.css           全ページ共通スタイル
  js/main.js              モバイルメニューなどの軽量 JS
favicon.svg               ファビコン
```

## Cloudflare Pages の設定

| 項目 | 値 |
| --- | --- |
| Production branch | `main` |
| Build command | （空欄） |
| Build output directory | （空欄） |
| Root directory | （空欄） |

> ビルド不要の静的サイトなので、ビルドコマンド・出力ディレクトリは空欄で OK です。

## 新しい攻略記事の追加方法

1. `guides/sample-guide-1.html` をコピーして、新しいファイル名（例：`guides/xxx-guide.html`）で保存します。
2. `<title>` と `<h1>`、本文を実際の内容に書き換えます。
3. `index.html` と `guides/index.html` の「攻略一覧」にカード（`<a class="card">`）を 1 つ追加して、リンクを新記事に向けます。
4. 変更を `main` ブランチに push すると、Cloudflare Pages が自動で再デプロイします。

## ローカルでの確認

このサイトはビルド不要なので、`index.html` をブラウザで直接開くだけでも確認できます。より正確に確認する場合は、このディレクトリで以下を実行して簡易サーバーを起動します。

```bash
npx serve .
# または
python3 -m http.server 8080
```

その後、ブラウザで http://localhost:8080 を開きます。
