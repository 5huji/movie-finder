# 🎬 影视评分助手

一个简洁优雅的电影/美剧评分查询工具，聚合多个权威平台的评分数据。

## ✨ 功能特点

- 🔍 **智能搜索**：支持中英文搜索电影和美剧
- ⭐ **多平台评分**：整合 TMDb、IMDb、烂番茄评分
- 📊 **分类浏览**：热门、高分、动作、剧情、喜剧、科幻
- 📱 **响应式设计**：完美适配手机、平板、电脑
- 🌙 **深色主题**：护眼舒适的视觉体验
- 🎯 **详细信息**：海报、简介、类型、时长等

## 🚀 快速开始

### 方法一：本地预览（5分钟）

1. **双击打开 `movie-finder.html` 文件**
   - 用浏览器打开即可看到界面

2. **申请免费API密钥**

   **TMDb API（必需）：**
   - 访问：https://www.themoviedb.org/signup
   - 注册账号 → 进入设置 → API → 申请密钥（选择Developer）
   - 复制 **API Key (v3 auth)**

   **OMDb API（可选，用于IMDb和烂番茄评分）：**
   - 访问：http://www.omdbapi.com/apikey.aspx
   - 选择 FREE（每天1000次请求）
   - 填写邮箱 → 激活 → 复制API Key

3. **配置密钥**
   - 在浏览器打开工具后，按 **F12** 打开开发者工具
   - 切换到 **Console** 标签
   - 粘贴以下代码并替换为你的密钥：

   ```javascript
   localStorage.setItem('tmdb_key', '你的TMDb密钥');
   localStorage.setItem('omdb_key', '你的OMDb密钥');
   location.reload();
   ```

4. **开始使用**
   - 刷新页面，配置提示消失即表示成功
   - 现在可以搜索或浏览电影了！

---

### 方法二：部署到GitHub Pages（永久在线）

#### 第一步：创建GitHub仓库

1. **登录GitHub**
   - 访问：https://github.com
   - 如果没有账号，点击 Sign up 注册（免费）

2. **创建新仓库**
   - 点击右上角 **+** → **New repository**
   - Repository name：`movie-finder`
   - 选择 **Public**
   - 勾选 **Add a README file**
   - 点击 **Create repository**

#### 第二步：上传文件

1. **上传HTML文件**
   - 在仓库页面点击 **Add file** → **Upload files**
   - 将 `movie-finder.html` 拖进去
   - 重命名为 `index.html`（重要！）
   - 点击 **Commit changes**

#### 第三步：启用GitHub Pages

1. **进入设置**
   - 点击仓库顶部的 **Settings**

2. **配置Pages**
   - 左侧菜单找到 **Pages**
   - Source 选择：**Deploy from a branch**
   - Branch 选择：**main** → **/ (root)**
   - 点击 **Save**

3. **等待部署**
   - 刷新页面，会看到：
     ```
     Your site is live at https://你的用户名.github.io/movie-finder/
     ```
   - 点击链接即可访问（首次可能需要等待1-2分钟）

#### 第四步：配置API密钥

- 访问你的网站
- 按照"方法一"中的步骤3配置密钥
- **注意**：密钥保存在浏览器本地，每个设备需要配置一次

---

## 📖 使用说明

### 搜索功能
- 在搜索框输入电影或美剧名称（中英文均可）
- 按回车或点击"搜索"按钮
- 点击卡片查看详细信息

### 分类浏览
- **正在热播**：当前最受欢迎的影片
- **高分推荐**：评分最高的经典作品
- **分类标签**：按类型快速筛选

### 查看详情
- 点击任意电影卡片
- 查看完整评分、剧情、类型等信息
- 点击弹窗外侧或×关闭

---

## ⚙️ 技术说明

- **纯前端**：无需服务器，直接在浏览器运行
- **API来源**：
  - TMDb：电影数据库、海报、简介
  - OMDb：IMDb评分、烂番茄评分
- **完全免费**：所有API都是免费套餐

---

## 🔧 常见问题

**Q: 为什么看不到评分？**
A: 请确保已正确配置TMDb API密钥，OMDb密钥是可选的。

**Q: GitHub Pages访问很慢？**
A: 国内访问GitHub Pages可能较慢，建议：
- 使用Cloudflare Pages（速度更快）
- 或者使用Vercel部署

**Q: 如何更新部署的网站？**
A: 修改本地HTML文件后，在GitHub仓库中上传替换即可。

**Q: API免费额度够用吗？**
A: TMDb每天可请求数千次，个人使用完全够。OMDb免费版每天1000次。

---

## 📝 自定义建议

如果你想修改样式或功能，可以编辑HTML文件：

- **修改配色**：搜索 `:root` 部分的CSS变量
- **调整布局**：修改 `.results` 的 `grid-template-columns`
- **添加分类**：在 `genreMap` 对象中添加更多类型

---

## 📄 开源协议

MIT License - 随意使用和修改

---

## 🙏 致谢

- 数据来源：[TMDb](https://www.themoviedb.org)、[OMDb](http://www.omdbapi.com)
- 图标：Emoji原生支持

---

**享受观影时光！🍿**
