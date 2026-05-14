# dotfiles

chezmoi によって管理している dotfile です

## セットアップ

### 1. chezmoi のインストール

```bash
brew install chezmoi
```

### 2. リポジトリの取得と適用

```bash
chezmoi init --apply https://github.com/aoi2005/dotfiles
```

### 3. メールアドレスの設定

以下の `example@example.com` の部分を git で使用しているメールアドレスに変更して実行してください。

```bash
cat >> ~/.local/share/chezmoi/.chezmoidata.toml << 'EOF'
email = "example@example.com"
EOF
```

その後、改めて apply を実行してください。

```bash
chezmoi apply
```

### 4. Homebrew パッケージのインストール

Homebrew にファイルに記述されているパッケージを全てインストールします。

```bash
brew bundle install --file=~/.config/Brewfile
```

## 管理しているツール

- Git
- Zsh
- Starship
- iTerm2
- VSCode
