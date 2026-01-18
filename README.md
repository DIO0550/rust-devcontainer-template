# rust-devcontainer-template

AIツールがプリインストールされたRust開発環境のDev Containerテンプレートリポジトリです。

## 🚀 特徴

- **Rust環境**: `rust:1-trixie` ベースのコンテナ
- **AIツール**: GitHub Copilot、Claude Code等のAI開発支援ツールを搭載
- **開発ツール**: rust-analyzer、ESLint、Prettier等の拡張機能を自動インストール

## 📦 含まれるVS Code拡張機能

| 拡張機能                | 説明                |
| ----------------------- | ------------------- |
| rust-lang.rust-analyzer | Rust言語サポート    |
| GitHub.copilot          | GitHub Copilot      |
| GitHub.copilot-chat     | GitHub Copilot Chat |
| anthropic.claude-code   | Claude Code         |
| dbaeumer.vscode-eslint  | ESLint              |
| esbenp.prettier-vscode  | Prettier            |

## 🛠️ セットアップ

### 前提条件

- [Docker](https://www.docker.com/)
- [VS Code](https://code.visualstudio.com/)
- [Dev Containers拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### 環境変数

以下の環境変数をローカル環境に設定してください：

| 環境変数                       | 説明                                    |
| ------------------------------ | --------------------------------------- |
| `GITHUB_PERSONAL_ACCESS_TOKEN` | GitHub Personal Access Token            |
| `GIT_AUTHOR_NAME`              | Gitコミット時の作者名                   |
| `GIT_AUTHOR_EMAIL`             | Gitコミット時の作者メールアドレス       |
| `GIT_COMMITTER_NAME`           | Gitコミット時のコミッター名             |
| `GIT_COMMITTER_EMAIL`          | Gitコミット時のコミッターメールアドレス |

### マウント設定

以下のディレクトリがコンテナにマウントされます：

- `~/.codex` → `/home/vscode/.codex`
- `~/.config/gh` → `/home/node/.config/gh` (読み取り専用)

### 使い方

1. このテンプレートを使用して新しいリポジトリを作成
2. VS Codeでリポジトリを開く
3. コマンドパレット (`Ctrl+Shift+P` / `Cmd+Shift+P`) から「Dev Containers: Reopen in Container」を実行

## 📁 構成

```
.devcontainer/
├── devcontainer.json    # Dev Container設定
├── docker-compose.yml   # Docker Compose設定
└── rust/
    └── Dockerfile       # Rustコンテナ定義
```

## 🌐 ネットワーク

- ポート `5300` が公開されています
- `mcp-network` ブリッジネットワークに接続

## 📄 ライセンス

[LICENSE](LICENSE) ファイルを参照してください。
