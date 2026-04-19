# corsor_chat

Cursorチャット運用向けの最小セットアップ済みリポジトリです。

## 含まれる設定

- `.cursor/rules/chat-workflow.mdc`
  - 日本語中心での応答
  - 依頼範囲に限定した変更
  - スレッド議事録（3〜6行）運用ルール
- `.cursorignore`
  - インデックス対象から依存・生成物・ログ類を除外
- `docs/thread-minutes/`
  - スレッドごとの議事録・関連ドキュメント保存先
  - `_template.md` でテンプレートを提供
- `docs/thread-minutes/2026-04-18-slack-setup/docs/slack-cursor-setup.md`
  - Slack から Cursor Cloud Agent を使うための導入チェックリスト（スレッド配下）

## 議事録の運用

1. 新しいスレッド開始時に `docs/thread-minutes/` 配下へ議事録ファイル、またはスレッド用ディレクトリを作成
2. 議事録は 3〜6行で「依頼 / 実施 / 結果 / 次アクション」を記載
3. 詳細仕様やロードマップはスレッド用ディレクトリ配下の `docs/` に配置
4. 必要に応じて同ファイルや同ディレクトリ内の資料を更新
