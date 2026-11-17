# SATO Works — Portfolio / Game UI (v3.0)

業務改善Webアプリ、AI・開発支援、Chrome拡張、個人プロダクトの制作実績を紹介する静的ポートフォリオです。ゲーム風のHUD、レーダー、起動画面の演出を維持しながら、**作品の目的・実装状況・公開先**が伝わる文言へ更新しています。

既存のリポジトリ直下 `index.html` は変更せず、このフォルダ内 `game-ui/index.html` を公開する想定です。

## プロジェクト（全9件）

| カテゴリ | 作品 | 状況 |
|---|---|---|
| 業務システム | GPS勤怠管理システム | 公開中（デモ） |
| 業務システム | 見積・請求書発行システム | 公開中（デモ） |
| Chrome拡張 | Video Time Notes | 公開中（Chromeウェブストア） |
| Chrome拡張 | Auto Manual Spec | 実機検証中 |
| Chrome拡張 | Real-time Audio Translator | 実機検証中 |
| AI・開発支援 | Personal AI Bridge | 開発中 |
| AI・開発支援 | Universal AI Monitor | 開発中 |
| 個人プロダクト | ANDW | 開発中 |
| 個人プロダクト | I'm done! | 仕様策定中 |

カテゴリと開発状況は**独立したフィルター**です。「開発・検証中」は開発中と実機検証中の両方を表示します。各カードの `DETAIL` で、解決する課題と現在の進捗を確認できます。

公開前の作品について、完成済み・本番運用中と誤認させないようにしています。

## Cloudflare Pages でGitHub連携

Cloudflare Dashboard → Workers & Pages → 新規作成 → Pages → GitHub接続から設定します。

| 設定 | 値 |
|---|---|
| GitHub repository | `satoruterashima/portfolio` |
| Production branch | `main` |
| Framework preset | `None` |
| Root directory | リポジトリのルート |
| Build command | 空欄 |
| Build output directory | `game-ui` |

静的な `index.html` だけで表示できます。Node.js・ビルドコマンドは不要です。すでにこの設定で連携済みなら、`main` 更新によって自動デプロイされます（Cloudflare側の連携設定によります）。

## ローカルプレビュー

```bash
python -m http.server 8000
```

リポジトリのルートで実行し、`http://localhost:8000/game-ui/` を開きます。

## 演出

- HUD風のトップ画面、SCAN RADAR、ポイント通過時の点滅
- テレビ電源OFF風のローディング終了演出
- マウス・キーボード・タップによるローディングスキップ
- 実績カード展開、カテゴリ・開発状況の絞り込み
- スマートフォン表示・低モーション設定への配慮

## 注意

- カード内のプレビューは説明用モックアップです。実際の製品画面ではありません。
- 公開前に、問い合わせメールアドレスの受信可否と外部リンクを確認してください。
- Real-time Audio Translatorの音声認識→翻訳字幕の一連の動作、Auto Manual Specの実機撮影などは検証継続中です。
- 本番へのデプロイはCloudflareのGitHub連携設定に依存します。

## 実スクリーンショットの掲載方針（2026-11-17）

- GPS勤怠管理システム：実際のダッシュボードと清掃スケジュールの2画面を掲載
- 見積・請求書発行システム：実際の帳票確認と帳票作成の2画面を掲載
- 上記以外の7作品：仮のUIイラストを廃止し、実スクリーンショットを受領するまで「SCREENSHOT PENDING」と表示
- 画像は `game-ui/assets/projects/` に保存したWebP画像（元の縦長スクリーンショットをリサイズ・圧縮したもの）
- カテゴリ・開発状況・9作品の説明文・ローディング／レーダー演出は維持
