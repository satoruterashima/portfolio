# SATO Works — Game UI Portfolio (v2.5)

SATO Works のゲームUI強化版ポートフォリオです。既存の `portfolio/index.html`（GitHub Pages用）を変更せず、`game-ui/index.html` に配置しています。

## Cloudflare Pages で公開する

Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git** から次の設定で公開できます。

| 設定 | 値 |
|---|---|
| GitHub repository | `satoruterashima/portfolio` |
| Production branch | `main` |
| Framework preset | `None` |
| Root directory | リポジトリのルート（変更しない） |
| Build command | **空欄** |
| Build output directory | `game-ui` |

このフォルダの `index.html` が新しい Cloudflare Pages サイトのトップページになります。

> 重要：出力先を `/（root）` や `public` にすると、既存の別サイトが公開対象になる可能性があります。**`game-ui`** を選んでください。

## 内容

- タクティカルHUD風のヒーロー
- ローディング／テレビ電源OFF風の終了演出（スマホは画面タップでスキップ可能）
- SCAN RADAR／スイープ通過時の4回点滅
- 実績カードの DETAIL 展開とフィルタ
- 公開済みデモへのリンク
- スマートフォン対応

## ローカル確認

```bash
python -m http.server 8000
```

リポジトリのルートで起動し、`http://localhost:8000/game-ui/` を開いてください。

## 注意

- サイト内の実績プレビュー画像・数値は、説明用のモックアップです。
- 外部デモの公開状態や問い合わせ先は、公開前に確認してください。
- このフォルダ単体で完結する静的HTMLのため、Node.jsやビルド処理は不要です。
