# 🎂 生日祝福网页 - GitHub Pages 部署指南

## 📱 微信分享使用说明

完成以下步骤后，你就可以在微信中发送链接给朋友，他们点击即可直接打开这个生日祝福页面！

---

## 🚀 部署步骤（5分钟搞定）

### 第一步：创建 GitHub 仓库

1. 打开 [GitHub](https://github.com) 并登录你的账号
2. 点击右上角 **"+"** → **"New repository"**
3. 填写信息：
   - **Repository name**: `birthday-wish`（或你喜欢的名字）
   - **Description**: `生日祝福网页`
   - 选择 **"Public"**（公开）- 必须公开才能被微信访问
4. **不要勾选** "Add a README file"
5. 点击 **"Create repository"**

### 第二步：上传代码

**方法 A：使用命令行（推荐）**

```bash
# 在 birthday 文件夹中执行
cd d:\TRAE人物\birthday

# 添加远程仓库地址（替换 YOUR_USERNAME 为你的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/birthday-wish.git

# 推送代码到 GitHub
git branch -M main
git push -u origin main
```

**方法 B：手动上传**

1. 在 GitHub 仓库页面点击 **"uploading an existing file"**
2. 拖拽 `index.html` 和 `.gitignore` 文件到上传区域
3. 点击 **"Commit changes"**

### 第三步：开启 GitHub Pages

1. 进入仓库页面
2. 点击 **Settings**（设置）
3. 左侧菜单找到 **Pages**
4. 在 "Source" 部分：
   - 选择 **"Deploy from a branch"**
   - Branch 选择 **"main"**
   - Folder 选择 **"/ (root)"**
5. 点击 **"Save"**
6. 等待 1-2 分钟（页面会显示部署状态）

### 第四步：获取链接

1. 回到仓库主页面
2. 点击 **Code** 按钮（绿色）
3. 找到 **Pages** 区域显示的链接：
   ```
   https://YOUR_USERNAME.github.io/birthday-wish/
   ```

✅ **这就是你的微信分享链接！**

---

## 📲 微信中使用方法

### 发送给朋友

1. 复制上面的链接
2. 打开微信
3. 粘贴并发送给朋友
4. 对方点击链接即可直接打开！

### 分享到朋友圈

1. 在微信浏览器中打开链接
2. 点击右上角 **"..."**
3. 选择 **"发送给朋友"** 或 **"分享到朋友圈"**

### 自定义分享内容（可选）

微信会自动抓取网页的标题和描述。当前设置为：
- **标题**: 🎂 生日快乐 - 专属祝福
- **描述**: 点击开启专属生日惊喜！烟花绽放、美味蛋糕、温馨音乐...

如需修改，编辑 [index.html](index.html) 中的 meta 标签。

---

## ✨ 功能特性

- ✅ **烟花动画** - 多种爆炸效果（心形、星星、圆环）
- ✅ **背景音乐** - 生日快乐歌自动播放
- ✅ **蛋糕蜡烛** - 可交互点亮/熄灭
- ✅ **移动端适配** - 完美支持手机屏幕
- ✅ **微信兼容** - 触摸事件优化，防止误触滚动
- ✅ **无需服务器** - 免费托管在 GitHub Pages

---

## 🔧 自定义修改

### 修改默认名字

打开 [index.html](index.html)，搜索以下代码：

```javascript
// 第 941 行附近
var name = nameInput.value.trim();
if (!name) {
    // 可以在这里设置默认名字
    name = "小明"; // 改成你想要的名字
}
```

### 修改颜色主题

在 `<style>` 标签中搜索颜色值进行替换：
- 背景色: `#0a0a2e`（深蓝色）
- 金色主题: `#ffd700`
- 渐变色可自行调整

---

## ❓ 常见问题

### Q: 链接打不开？
A: 
- 确认仓库是 **Public**（公开）
- 检查 Pages 是否部署成功（Settings → Pages 查看 Status）
- 等待 2-3 分钟让部署完成

### Q: 音乐不播放？
A: 
- 微信限制自动播放音频
- 用户需要先点击页面任意位置才会播放音乐
- 这是微信的安全策略，无法绕过

### Q: 想要自定义域名？
A: 
- 在 Settings → Pages → Custom domain 中设置
- 需要有自己的域名并配置 DNS 解析

### Q: 如何更新内容？
A: 
- 修改本地文件后执行：
```bash
git add .
git commit -m "更新内容"
git push
```
- GitHub 会自动重新部署（约1分钟）

---

## 📞 技术支持

如有问题，请检查：
1. 浏览器控制台是否有错误（F12 → Console）
2. GitHub Pages 部署状态是否正常
3. 网络连接是否正常

---

**🎉 祝你和朋友们生日快乐！**

现在就去创建 GitHub 仓库吧！完成后把链接发给朋友，给他们一个惊喜！💝