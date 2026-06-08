# task-board

## プロジェクト概要

タスク管理ボードアプリケーション。

## Git 運用ルール

- コードを変更するたびに、変更内容をコミットして GitHub にプッシュする
- コミットメッセージは変更内容を端的に表す日本語または英語で記述する
- `main` ブランチへの直接プッシュを基本とする（別途ブランチ戦略を定める場合はこのルールを更新する）

### 手順

1. 変更をステージング: `git add <file>`
2. コミット: `git commit -m "メッセージ"`
3. プッシュ: `git push origin main`

## デプロイ先

https://fusahiko-ishikawa.github.io/task-board/

- ホスティング: GitHub Pages
- `main` ブランチへのプッシュで GitHub Actions が自動ビルド＆デプロイ

## 技術スタック

| 用途 | 技術 |
|------|------|
| UIフレームワーク | React 18 |
| ビルドツール | Vite 6 |
| 言語 | JavaScript (JSX) |
| スタイリング | CSS (`.css` ファイル) |
| 状態永続化 | localStorage |
| CI/CD | GitHub Actions |

## コンポーネント命名規約

- コンポーネントファイル: PascalCase（例: `TaskItem.jsx`）
- コンポーネント関数: PascalCase（例: `function TaskItem()`）
- CSSクラス名: kebab-case（例: `.task-item`, `.delete-btn`）
- 状態変数: camelCase（例: `inputValue`, `tasks`）
- イベントハンドラ: `handle` プレフィックス + PascalCase（例: `handleKeyDown`）

## 開発環境

- OS: Windows 11
- Shell: PowerShell
- 開発サーバー起動: `npm run dev` → http://localhost:5173

## 注意事項

- `.env` などの機密情報を含むファイルはコミットしない
- `node_modules/` や `dist/` などのビルド成果物はコミットしない
