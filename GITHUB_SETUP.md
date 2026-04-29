# GitHub 設置步驟

按照以下步驟將 Prince Sohyeon Portal 上傳到 GitHub：

## 第一步：在 GitHub 創建倉庫

1. 登錄 GitHub (https://github.com)
2. 點擊右上角 "+" → "New repository"
3. 倉庫名稱：`prince-sohyeon-portal`
4. 描述（可選）：`A comprehensive historical portal dedicated to Prince Sohyeon of Chosŏn (1612–1645)`
5. 選擇 Public 或 Private
6. **不要** 勾選 "Initialize this repository with a README" （我們已經有了）
7. 點擊 "Create repository"

## 第二步：複製倉庫 URL

創建後，GitHub 會顯示倉庫 URL，格式為：
- HTTPS: `https://github.com/sheranma1/prince-sohyeon-portal.git`
- SSH: `git@github.com:sheranma1/prince-sohyeon-portal.git`

## 第三步：在終端執行 Git 命令

在 macOS 終端中，導航到項目文件夾並執行以下命令：

```bash
cd /Users/hualeyi/soyheon-combined

# 初始化 Git 倉庫
git init

# 添加遠程倉庫（選擇 HTTPS 或 SSH）
# 使用 HTTPS（推薦首次使用）：
git remote add origin https://github.com/sheranma1/prince-sohyeon-portal.git

# 或使用 SSH（需要配置 SSH keys）：
# git remote add origin git@github.com:sheranma1/prince-sohyeon-portal.git

# 添加所有文件
git add .

# 提交更改
git commit -m "Initial commit: Prince Sohyeon Portal with all components"

# 重命名分支為 main（如果需要）
git branch -M main

# 推送到 GitHub
git push -u origin main
```

## 第四步：驗證上傳

1. 訪問 https://github.com/sheranma1/prince-sohyeon-portal
2. 確認所有文件都已上傳
3. README.md 應該自動在倉庫頁面顯示

## 常見問題

### 如果遇到認證問題（HTTPS）
GitHub 不再支持密碼認證。需要使用：
- Personal Access Token（個人訪問令牌）或
- 配置 SSH keys

### 使用 Personal Access Token
1. 在 GitHub 設置中生成 token：Settings → Developer settings → Personal access tokens
2. 選擇 "repo" 範圍
3. 複製 token
4. 在終端提示輸入密碼時，貼上 token（而不是密碼）

### 設置 SSH（推薦）
1. 生成 SSH key：`ssh-keygen -t ed25519 -C "your_email@example.com"`
2. 添加到 SSH agent：`ssh-add ~/.ssh/id_ed25519`
3. 複製公鑰到 GitHub：Settings → SSH and GPG keys → New SSH key
4. 貼上 `~/.ssh/id_ed25519.pub` 的內容

## 之後的更新

如果之後修改了文件並想更新 GitHub：

```bash
git add .
git commit -m "Update: [描述你的更改]"
git push origin main
```

## 需要幫助？

- GitHub 文檔：https://docs.github.com
- Git 教程：https://git-scm.com/book/en/v2
