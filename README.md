# portfolio
SATOWorks｜小さな会社のアプリ屋　ポートフォリオ

## 公開手順

1. このリポジトリを `main` ブランチにプッシュします。
2. GitHub Actions が自動的に `gh-pages` ブランチへデプロイします。
3. GitHub リポジトリの「Settings > Pages」でソースを `gh-pages` ブランチ、フォルダ `/(root)` に設定します。
4. 公開URL は `https://satoruterashima.github.io/portfolio/` になります。

## 追加ファイル

- `sitemap.xml` : 検索エンジン向けサイトマップ
- `robots.txt` : 全クロール許可と sitemap の参照

## ローカルプレビュー

```bash
cd /workspaces/portfolio
python3 -m http.server 8000
```

その後、ブラウザで `http://127.0.0.1:8000` を開いてください。
