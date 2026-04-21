# 上海房贷与税费计算器

一个纯前端实现的上海购房贷款与税费计算工具，支持商业贷款、公积金贷款及组合贷款的等额本息/等额本金计算，并自动根据 2026 年上海最新购房政策计算契税。

## 在线访问

👉 **[点击这里在线使用](https://vrpolice.github.io/shanghai-mortgage-calculator/)**

（如果尚未部署，请参考下方【部署到 GitHub Pages】步骤）

## 功能特点

- **首付比例计算**：自动校验首付是否满足上海最低 15% 要求
- **组合贷款支持**：商业贷款 + 公积金贷款自动分配
- **利率自动切换**：根据首套房/二套房自动填充最新利率
- **还款方式对比**：等额本息 vs 等额本金，一键切换查看
- **契税自动计算**：依据 2026 年上海政策（≤140㎡ 1%，首套>140㎡ 1.5%，二套>140㎡ 2%）
- **纯静态页面**：无需后端，打开即用

## 新房楼盘分布图

本项目还包含一个**上海新房楼盘分布图**页面（`shanghai-new-houses.html`），可在计算器页面点击链接直接进入：

- 该页面主要展示**公寓类新房楼盘**（以三房户型为主）的地理位置分布
- **不包含纯粹的别墅新盘**，如有别墅需求请参考其他渠道
- 地图基于高德地图 JSAPI 实现，支持交互浏览

## 本地使用

直接在浏览器中打开 `index.html` 文件即可：

```bash
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

或者使用本地静态服务器：

```bash
# Python 3
python -m http.server 8080

# Node.js
npx serve .
```

然后在浏览器中访问 `http://localhost:8080`

## 部署到 GitHub Pages（推荐）

GitHub Pages 可以免费托管静态网站，步骤如下：

### 1. 创建 GitHub 仓库

1. 打开 [GitHub](https://github.com) 并登录
2. 点击右上角 **+** → **New repository**
3. 仓库名称填写：`shanghai-mortgage-calculator`
4. 选择 **Public**（公开）
5. 点击 **Create repository**

### 2. 上传代码到仓库

在终端中执行以下命令（确保你已安装 [Git](https://git-scm.com/downloads)）：

```bash
# 进入项目目录
cd shanghai-mortgage-calculator

# 初始化 Git 仓库（如果尚未初始化）
git init

# 添加文件
git add index.html

# 提交代码
git commit -m "Initial commit: Shanghai mortgage calculator"

# 添加远程仓库（请将 USERNAME 替换为你的 GitHub 用户名）
git remote add origin https://github.com/USERNAME/shanghai-mortgage-calculator.git

# 推送到 main 分支
git branch -M main
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入刚创建的仓库页面
2. 点击顶部菜单栏的 **Settings**
3. 左侧栏选择 **Pages**
4. **Source** 选择 **Deploy from a branch**
5. **Branch** 选择 `main`，文件夹选择 `/(root)`
6. 点击 **Save**

### 4. 访问你的网站

等待约 1-2 分钟后，你的计算器将通过以下链接访问：

```
https://USERNAME.github.io/shanghai-mortgage-calculator/
```

将 `USERNAME` 替换为你的 GitHub 用户名即可。

## 使用说明

1. **输入房屋信息**：填写房屋总价、首付金额、面积和购房类型
2. **调整贷款信息**：选择贷款年限，系统会自动分配公积金和商贷金额
3. **点击"开始计算"**：查看契税、月供、总利息等详细信息
4. **切换还款方式**：在"等额本息"和"等额本金"之间切换对比

## 技术栈

- HTML5
- CSS3（原生样式，无框架）
- JavaScript（原生 JS，无框架/库依赖）

## 政策依据

- 2026 年上海最新购房政策
- 首付比例：最低 15%
- 契税标准：
  - ≤140㎡：统一 1%
  - 首套 >140㎡：1.5%
  - 二套 >140㎡：2%
- 公积金贷款额度：首套最高 240 万，二套最高 200 万
- 公积金利率：首套 2.6%，二套 3.075%
- 商贷利率：首套 3.05%，二套 3.06%

## 许可证

MIT License - 可自由使用、修改和分发。
