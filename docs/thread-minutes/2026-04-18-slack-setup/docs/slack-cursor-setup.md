# Cursor を Slack で操作する準備（Cloud Agent）

Slack から操作できる対象は、Cursor の **Cloud Agent** です。  
ローカルの Cursor アプリを直接リモート操作する機能ではありません。

## 1. 事前チェック

- Cursor の有料プランで Cloud Agent を利用できること
- Slack ワークスペースでアプリ導入権限（管理者承認を含む）があること
- 操作対象の GitHub リポジトリに Cursor がアクセスできること

## 2. 初期設定手順

1. Cursor ダッシュボードの Integrations で Slack を `Connect`
2. Slack 側で Cursor アプリをインストール（OAuth 許可）
3. Cloud Agent の初期設定を確認
   - GitHub 連携
   - デフォルトリポジトリ / ブランチ
   - usage-based pricing
   - Privacy / Security 設定
4. Slack チャンネルで `@Cursor settings` を実行し、チャンネル既定値を整える

## 3. 動作確認（最小）

1. `@Cursor help` でコマンド一覧を確認
2. `@Cursor in <repo>, <依頼内容>` で対象リポジトリを指定して実行
3. `@Cursor list my agents` で稼働中エージェントを確認
4. 完了通知から PR リンクや `Open in Cursor` を確認

## 4. 運用時の注意点

- Slack 連携時に要求される権限スコープは事前にレビューする
- 外部メンバーがいるチャンネルでは、要約や diff の表示ポリシーを設定する
- Cloud Agent のネットワーク到達先は必要に応じて制限（allowlist）する
- Cloud Agent はコマンド自動実行を行うため、機密情報を含む指示を避ける
- Legacy の Privacy Mode は Cloud Agent では使えない前提で設計する

## 5. トラブル時の切り分け

- Slack 側で `@Cursor` メンションに反応しない  
  - アプリがチャンネルに招待済みか
  - ワークスペースのアプリ承認が完了しているか
- エージェント起動後に失敗する  
  - リポジトリ指定が正しいか
  - GitHub 連携と Cloud Agent 設定が完了しているか
