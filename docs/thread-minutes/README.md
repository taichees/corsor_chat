# thread-minutes

スレッドごとに**1フォルダ**を作り、議事録と関連成果物をまとめて保存するディレクトリです。

## ディレクトリ構成

```
docs/thread-minutes/
├── README.md            ← このファイル
├── _template/           ← 新規スレッド用テンプレ
│   └── minutes.md
└── <YYYY-MM-DD-thread-slug>/
    ├── minutes.md       ← 議事録（必須）
    ├── *.html           ← 関連成果物（任意）
    ├── *.png            ← 関連成果物（任意）
    └── ...
```

## 使い方

1. 新しいスレッド開始時に `YYYY-MM-DD-thread-slug` 形式のフォルダを作成
2. `_template/minutes.md` をコピーして `<thread-folder>/minutes.md` に配置
3. **3〜6行** で簡潔に記載
4. 関連する成果物（HTML / 画像 / コード断片など）は**同じフォルダ内**に置く
5. 必要に応じて議事録を更新

## 議事録の必要項目

1. 依頼の要点（Request）
2. 実施内容（Actions）
3. 結果 / 次アクション（Outcome / Next）

## 命名規則

- フォルダ名: `YYYY-MM-DD-<kebab-case-slug>`
  - 例: `2026-04-18-coconala-thumbnail`
- 議事録ファイル名: `minutes.md` で固定
- 成果物ファイル名: 内容が分かるケバブケース（例: `coconala-thumbnail-webfix.html`）
