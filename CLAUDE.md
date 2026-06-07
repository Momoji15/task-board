# Task Board Project

## Overview

タスク管理ボードアプリケーション。

## Git 運用ルール

- **コードを変更するたびに、必ず GitHub へプッシュすること。**
- コミットメッセージは変更内容を端的に表す日本語または英語で記述する。
- 直接 `main` ブランチへコミット・プッシュする（小規模プロジェクトのため）。
- 機能追加・バグ修正・リファクタリングのいずれも、変更完了後に即座にプッシュする。

### コミット & プッシュの手順

```powershell
git add <変更ファイル>
git commit -m "コミットメッセージ"
git push origin main
```

### 注意事項

- `git add .` は意図しないファイルを含めるリスクがあるため、原則としてファイルを明示して `add` する。
- `.env` やシークレットを含むファイルは絶対にコミットしない。
- プッシュ前に `git diff --staged` で差分を確認する習慣をつける。

## デプロイ先

- **GitHub Pages:** https://Momoji15.github.io/task-board/
- `main` ブランチへのプッシュで GitHub Actions が自動デプロイする。
- ワークフロー: `.github/workflows/deploy.yml`

## 技術スタック

| カテゴリ | 技術 |
|---|---|
| UI ライブラリ | React 18 |
| ビルドツール | Vite 5 |
| 言語 | JavaScript (JSX) |
| スタイリング | Plain CSS (CSS Modules なし) |
| 状態管理 | React `useState` / `useEffect` |
| 永続化 | `localStorage` |
| パッケージマネージャ | npm |

## コンポーネント命名規約

- コンポーネントファイルは **PascalCase** で命名する（例: `TaskItem.jsx`）。
- コンポーネント関数名もファイル名と一致させる。
- 1ファイル1コンポーネントを基本とする。
- CSS ファイルはコンポーネントと同名にする（例: `TaskItem.css`）。
- フック（カスタム Hook）は `use` プレフィックスを付け `camelCase` で命名する（例: `useLocalStorage.js`）。

## 開発環境

- OS: Windows 11
- Shell: PowerShell / Bash
- エディタ: VS Code
