# My Mac Setup

> All the apps / tools / settings I use on my Mac

- [What MacBook do I have?](#what-macbook-do-i-have)
- [Homebrew](#homebrew)
- [Quick Lauching](#quick-launching)
- [Development](#development)
- [Terminal](#terminal)
- [Apps](#apps)
- [Chrome Extentions](#chrome-extentions)
- [Reference](#reference)

## What MacBook do I have?

2023 14" MacBook Pro, Apple M2 Pro

## Homebrew

使用 [Homebrew](https://brew.sh/) 从命令行安装各种工具和软件：
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
具体安装细节参考 [Homebrew Installation Guide](https://www.youtube.com/watch?v=IWJKRmFLn-g)

## Quick Launching

用 [Raycast](https://www.raycast.com/) 代替 Spotlight 搜索：

```
brew install raycast
```

## Development

- 安装 [Git](https://git-scm.com/)：
    ```
    brew install git
    ```
- 安装 [Node.js](https://nodejs.org/en)：
    ```
    brew install node
    ```
- 安装 [pnpm](htts://pnpm.io) 包管理器：
    ```
    npm install -g pnpm
    ```
- 添加 GitHub SSH Key：[Setting GitHub SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
    ```bash
    # 1.
    ssh-keygen -t ed25519 -C "your_email@example.com"

    # 2.
    eval "$(ssh-agent -s)"

    # 3.
    ssh-add --apple-use-keychain ~/.ssh/id_ed25519

    # 4.
    open ~/.ssh/config

    # Add context below
    Host *
	    AddKeysToAgent yes
	    UseKeychain yes
	    IdentityFile ~/.ssh/id_ed25519

    # 5.
    pbcopy < ~/.ssh/id_ed25519.pub
    ```

## Terminal

- 终端：[iTerm2](https://iterm2.com/):
    ```
    brew install iterm2
    ```
- Shell：[Oh My Zsh](https://ohmyz.sh/)

## Apps

- 代码编辑器：[VS Code](https://code.visualstudio.com/)
- 浏览器：[Arc Browser](https://arc.net/)
- 密码管理器: [1Password](https://1password.com/)
- 邮件管理：[Spark](https://sparkmailapp.com/)
- 文本编辑器：[Typora](https://typora.io/)
- 录屏：[Screen Studio](https://screen.studio/)

## Chrome Extentions

- 查看某网站使用的技术栈：[Wappalyzer](https://chromewebstore.google.com/detail/gppongmhjkpfnbhagpmjfkannfbllamg?)

## Reference

- [Set up a Mac in 2024 for Power Users and Developers](https://www.youtube.com/watch?v=GK7zLYAXdDs)
