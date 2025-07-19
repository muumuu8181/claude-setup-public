# 🚀 Claude Code 新端末セットアップガイド

## 📋 このリポジトリの目的
新しい端末でClaude Codeを最速でセットアップするための**公開用ガイド**です。

## ⚡ クイックスタート（5分）

### 1. 基本セットアップ
```bash
# Claude Code CLI インストール
npm install -g @anthropic-ai/claude-code

# 認証
claude auth login

# GitHub CLI セットアップ
gh auth login
```

### 2. 基本作業の開始
```bash
# 既存プロジェクトをクローン
claude "https://github.com/muumuu8181/[リポジトリ名] をクローンして作業を開始"
```

## 🔐 詳細設定（認証後）

基本セットアップ完了後、以下のプライベートリポジトリで詳細設定を行ってください：

### プライベートリポジトリ一覧
- **claude-ai-toolkit** - 包括的な設定ガイド
- **firebase-configs** - Firebase/API設定情報
- **mcp-toolkit** - MCPサーバー設定

### アクセス方法
```bash
# GitHubに認証後、プライベートリポジトリにアクセス
claude "https://github.com/muumuu8181/claude-ai-toolkit をクローンして、詳細な設定手順を教えて"
```

## 📱 Android/Termux 特記事項

### 追加インストール
```bash
# パッケージ更新
pkg update && pkg upgrade

# Node.js（未インストールの場合）
pkg install nodejs-lts

# Git設定
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### ストレージアクセス（ファイル共有が必要な場合）
```bash
termux-setup-storage
```

## 🎯 よく使うコマンド

### Claude Code
```bash
# 新規作業開始
claude

# 特定リポジトリで作業
claude "リポジトリをクローンして〇〇を実装して"

# MCP確認
claude /mcp
```

### GitHub操作
```bash
# リポジトリ一覧
gh repo list

# Issue作成
gh issue create --title "タイトル" --body "内容"
```

## 📚 次のステップ

1. ✅ 基本セットアップ完了
2. 🔐 プライベートリポジトリにアクセス
3. 🛠️ 詳細設定（Firebase、MCP等）
4. 🚀 本格的な開発開始

---

## 🔗 関連リンク
- [Claude Code 公式ドキュメント](https://docs.anthropic.com/en/docs/claude-code)
- [GitHub CLI ドキュメント](https://cli.github.com/manual/)

**Note**: このリポジトリには認証情報は含まれていません。詳細設定はプライベートリポジトリで行ってください。