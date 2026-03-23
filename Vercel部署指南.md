# 🚀 Vercel 部署指南 - 3分钟上线

## 准备工作 ✅

所有文件已准备完毕，位于：`C:\Users\wy_zhouyulong\qa-system\`

---

## 步骤一：注册 Vercel 账号（1分钟）

1. **打开浏览器，访问**: https://vercel.com/signup

2. **选择注册方式**（推荐使用 GitHub）:
   - 点击 "Continue with GitHub"
   - 或使用邮箱注册（填写邮箱和密码）

3. **如果选择 GitHub**:
   - 会跳转到 GitHub 登录页面
   - 输入 GitHub 用户名和密码
   - 点击 "Authorize Vercel"

4. **如果选择邮箱注册**:
   - 填写邮箱地址
   - 设置密码
   - 点击注册
   - 到邮箱中验证

5. **完成注册后会自动登录到 Vercel 控制台**

---

## 步骤二：部署项目（2分钟）

### 方法A：通过 GitHub 部署（推荐）

**1. 先将代码推送到 GitHub**

如果你有 GitHub 账号，在命令行执行：

```bash
# 在 GitHub 网站创建仓库后，复制仓库 URL，然后执行：
cd C:\Users\wy_zhouyulong\qa-system
git remote add origin https://github.com/你的用户名/qa-system.git
git branch -M main
git push -u origin main
```

**2. 在 Vercel 导入项目**

- 在 Vercel 控制台点击 "Add New..." → "Project"
- 点击 "Import Git Repository"
- 选择你刚才推送的 `qa-system` 仓库
- 点击 "Import"
- 直接点击 "Deploy"（无需修改任何配置）
- 等待 1-2 分钟，部署完成！

---

### 方法B：直接上传文件夹（更简单）

**1. 安装 Vercel CLI（首次使用）**

打开命令行（PowerShell 或 CMD），执行：

```bash
npm install -g vercel
```

如果提示 npm 不存在，需要先安装 Node.js:
- 访问 https://nodejs.org/
- 下载并安装 LTS 版本
- 安装完成后重新执行上面的命令

**2. 登录 Vercel**

```bash
vercel login
```

会打开浏览器，点击确认登录

**3. 部署项目**

```bash
cd C:\Users\wy_zhouyulong\qa-system
vercel
```

按提示操作：
- "Set up and deploy"? → 按回车（默认 Yes）
- "Which scope"? → 按回车（选择你的账号）
- "Link to existing project"? → 输入 `n` 然后回车（新项目）
- "What's your project's name"? → 按回车（默认 qa-system）
- "In which directory"? → 按回车（当前目录）
- "Want to override the settings"? → 输入 `n` 然后回车

完成！会显示你的网址！

---

### 方法C：Vercel 网页上传（最简单，无需命令行）

**1. 压缩文件夹**

- 进入 `C:\Users\wy_zhouyulong\qa-system\` 文件夹
- 选中以下文件（不要选 .git 文件夹和 .bat 文件）：
  - qa.html
  - admin.html
  - index.html
  - index-chat.html
  - vercel.json
  - README.md
  - 使用指南.md
  - 重启后操作指南.md
- 右键 → "发送到" → "压缩文件夹"
- 命名为 `qa-system.zip`

**2. 上传到 Vercel**

- 访问 https://vercel.com/new
- 登录你的 Vercel 账号
- 看到 "Import Git Repository" 页面
- 往下滚动，找到 "Or, upload a folder from your computer"
- 点击 "Browse" 或直接拖拽 `qa-system.zip` 文件
- 等待上传和部署完成（约 1 分钟）

---

## 步骤三：获取网址并测试

部署完成后，Vercel 会显示：

```
✅ Deployed to production

🔗 https://qa-system-xxxx.vercel.app
```

1. **点击网址或复制到浏览器**
2. **测试访问**:
   - 直接访问网址 → 会自动打开 qa.html
   - 或访问 `https://你的网址/qa.html` → 用户问答页面
   - 或访问 `https://你的网址/admin.html` → 管理后台

3. **分享给员工**:
   ```
   【智能问答系统上线通知】

   访问地址: https://你的网址.vercel.app

   使用方法：
   1. 点击链接打开
   2. 输入问题或点击快捷按钮
   3. 立即获得答案

   支持手机和电脑浏览器访问！
   ```

---

## 常见问题

### Q1: 部署后打开是空白页面？
**A:** 清除浏览器缓存，或使用无痕模式打开

### Q2: 网址太长，能自定义吗？
**A:** 可以！在 Vercel 项目设置中：
- 点击 "Settings" → "Domains"
- 点击 "Edit" 修改项目名称
- 或绑定自己的域名

### Q3: 修改了文件后如何更新？
**A:**
- 如果通过 GitHub 部署：推送新代码到 GitHub，Vercel 会自动重新部署
- 如果通过 CLI 部署：再次运行 `vercel` 命令
- 如果是网页上传：重新上传新的压缩包

### Q4: 完全免费吗？
**A:** 是的！Vercel 个人用户完全免费，流量足够使用

---

## 🎉 完成！

现在你的智能问答系统已经在互联网上了！

**网址格式**: `https://qa-system-[随机字符].vercel.app`

有任何问题随时问我！
