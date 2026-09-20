# GitHub 注册 + QtCourse 仓库推送 · 手把手步骤

> 本地仓库已经帮你建好了（分支 `main`，已经有 1 次提交）。
> 你只需要做两件事：**① 注册账号并建仓库**；**② 把下面最后一条命令粘到终端里跑一遍**。

---

## 第一步：注册 GitHub 账号（约 5 分钟）

1. 浏览器打开 <https://github.com> → 点右上角 **Sign up**
2. 填 **邮箱** → **密码**（至少 8 位，含数字和小写字母）→ **用户名**
   - 用户名只能用 字母 / 数字 / 连字符，建议用 `chenxuanxin` 或 `chenxuanxin2023`
   - ⚠️ 用户名记下来，后面要用
3. 过一下人机验证（拼图 / 旋转图片）
4. 邮箱会收到一封 GitHub 邮件，里面是 **8 位数字验证码**，填进去完成验证
5. 注册完成后登录，能看到自己的主页就 OK 了

## 第二步：创建 QtCourse 仓库（1 分钟）

1. 登录后点右上角 **+** → **New repository**（或直接访问 <https://github.com/new>）
2. **Repository name** 填：`QtCourse`
3. **Description** 随便写，例如：`Qt 课程作业仓库`
4. 可见性选 **Public**（公开）
5. ⚠️ **不要勾任何初始化选项**（Add a README file / Add .gitignore / Choose a license 全部留空）
6. 点绿色按钮 **Create repository**

## 第三步：推送代码（复制粘贴就行）

创建完仓库后，把下面这条命令里的 `<你的用户名>` 换成你注册时的用户名，然后粘到终端里执行：

```bash
git remote add origin https://github.com/<你的用户名>/QtCourse.git
git push -u origin main
```

> 两种更省事的方式（推荐）：
> 1. 直接在项目文件夹 `C:\Users\chenxuanxin\Desktop\samp2_4App` 上右键 → **Open Git Bash here**，把上面两行粘进去回车；
> 2. 或者把用户名告诉我，我帮你把命令生成好，你复制一次就行。

第一次 `git push` 时，Windows 会弹出一个 **GitHub 登录窗口**：

- 选 **Sign in with your browser**
- 浏览器里点 **Authorize** 授权
- 授权成功后终端会显示 `* [new branch] main -> main`，说明推送成功 🎉

以后再推送就不需要重复登录了。

## 第四步：截图交作业

推送成功后，刷新 `https://github.com/<你的用户名>/QtCourse`，你会看到仓库里已经有这些文件：

```
samp2_4.pro   qwmainwind.cpp   qwmainwind.h   qwmainwind.ui
res.qrc       main.cpp         images/        screenshots/
README.md     .gitignore
```

把下面两张图截下来，贴进《第2周作业-陈萱欣.docx》里 3.5 节的两个占位位置：

| 要截的图 | 截图要求 |
| --- | --- |
| GitHub 仓库页面 | 要能看到地址栏 `github.com/<用户名>/QtCourse` + 文件列表 + 提交记录 |
| 推送成功的终端 | 要能看到 `* [new branch] main -> main` 那一行 |

---

## 常见问题

**Q：推送时提示 `remote: Support for password authentication was removed`？**
说明你在弹窗里手输了密码。GitHub 早就不允许用账号密码推送了，走浏览器登录（Sign in with your browser）即可。

**Q：提示 `remote origin already exists`？**
说明已经加过远程地址了，跳过 `git remote add` 那句，直接跑 `git push -u origin main`。

**Q：`git push` 一直转圈 / 连不上？**
GitHub 在国内偶尔会抽风，多试两次；还不行的话挂个梯子或者在 hosts 里加 GitHub 的 IP。

**Q：用户名填错了怎么办？**
改一下远程地址就行：`git remote set-url origin https://github.com/正确的用户名/QtCourse.git`
