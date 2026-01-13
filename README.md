# 高中教材使用反馈系统

## 项目概述
这是一个基于Web的教材使用反馈系统，前端部署在GitHub Pages，数据存储在GitHub Issues。

## 功能特点
1. 美观的响应式问卷界面
2. 数据自动存储到GitHub Issues
3. 支持数据导出为Excel
4. 跨设备访问

## 部署步骤

### 1. 准备工作
- 注册GitHub账号
- 创建一个新的仓库（如：teaching-feedback）
- 生成GitHub个人访问令牌（Settings → Developer settings → Personal access tokens → Tokens (classic)）
  - 权限选择：repo（完全控制仓库）、user（用户信息）

### 2. 本地文件准备
将以下文件上传到GitHub仓库：
- `index.html` (主页面文件)
- `api.py` (数据处理脚本)
- `app.py` (可选：本地运行的后端)
- `requirements.txt` (依赖列表)

### 3. 启用GitHub Pages
1. 进入仓库设置（Settings）
2. 找到"Pages"选项
3. 分支选择：main，目录选择：/ (root)
4. 保存后访问 https://[你的用户名].github.io/[仓库名]/

### 4. 配置GitHub Token
在HTML文件中搜索 `GITHUB_TOKEN`，替换为你的真实令牌：
或者使用后端API方式（推荐）

## 数据管理

### 查看反馈数据
1. 直接在GitHub仓库的Issues页面查看
2. 或运行 `api.py` 脚本查看

### 导出Excel数据
运行以下命令：
```bash
python api.py
选择选项2，输入文件名即可导出
