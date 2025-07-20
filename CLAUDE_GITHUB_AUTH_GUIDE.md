# Claude Code GitHub 連携ガイド

Claude Code で GitHub を操作するための認証設定手順です。

## 前提条件
- Claude Code CLI がインストール済み
- GitHub アカウントを持っている

## セットアップ手順

### 1. Claude Code CLI 認証
```bash
# Claude Code の認証状態確認
claude auth status

# 未認証の場合はログイン
claude auth login
```

### 2. GitHub CLI インストール・認証

#### 通常環境（Windows/Mac/Linux）
```bash
# GitHub CLI のインストール確認
gh --version

# GitHub 認証
gh auth login
# → GitHub.com を選択
# → HTTPS を選択  
# → ブラウザで認証
```

#### Android/Termux 環境
```bash
# GitHub CLI インストール
pkg update && pkg upgrade
pkg install gh

# 認証開始（ワンタイムコード方式）
gh auth login --web
# 表示されるコード（例: AA5E-C631）をコピー
# ブラウザで https://github.com/login/device を開く
# コードを入力して認証

# 認証確認
gh auth status
```

### 3. Git 基本設定
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

# HTTPS認証情報の保存を有効化（オプション）
git config --global credential.helper store
```

## 動作確認

### リポジトリ操作テスト
```bash
# リポジトリ一覧表示
gh repo list --limit 5

# Claude Code で GitHub リポジトリを操作
claude "GitHubのリポジトリ一覧を表示して"
```

### トラブルシューティング

#### 認証エラーが出る場合
```bash
# Claude Code 再認証
claude auth logout
claude auth login

# GitHub CLI 再認証
gh auth logout
gh auth login
```

#### Termux でブラウザが開かない場合
- ワンタイムコードとURLを手動でブラウザに入力
- 認証完了後、何かコマンドを実行すると認証が有効化される

## 注意事項
- 認証トークンは適切に管理してください
- 公開リポジトリでトークンを公開しないよう注意
- 定期的に認証状態を確認することを推奨

## 関連リンク
- [Claude Code 公式ドキュメント](https://docs.anthropic.com/en/docs/claude-code)
- [GitHub CLI 公式ドキュメント](https://cli.github.com/)