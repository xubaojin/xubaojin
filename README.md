# 徐保金 | 个人简历网站

资深运维开发专家 / 资深 SRE 专家的个人简历主页，纯静态 HTML + CSS，零依赖、零构建。

**在线访问**：<https://xubaojin.com>

## 特性

- 纯静态，无 JS 框架依赖，加载极快
- 响应式设计，适配桌面 / 平板 / 手机
- 微信内置浏览器专项兼容
- SEO 友好：Open Graph + JSON-LD 结构化数据
- 入场动画与卡片悬浮交互

## 项目结构

```
├── .github/workflows/deploy.yml  # GitHub Actions 自动部署
├── css/abao.css                  # 全部样式（含响应式 & 动画）
├── images/                       # 头像、微信二维码
├── .nojekyll                     # 跳过 Jekyll
├── .gitignore
├── CNAME                         # 自定义域名
└── index.html                    # 简历主页面
```

## 本地预览

直接用浏览器打开 `index.html`，或启动本地服务器：

```bash
python -m http.server 8080
```

## 部署

通过 GitHub Actions 自动部署到 GitHub Pages，推送 main 分支即触发：

```bash
git push origin main
```

域名通过 `CNAME` 文件绑定，DNS 需配置 A 记录指向 GitHub Pages 服务器 IP（`185.199.108.153` ~ `185.199.111.153`），`www` 用 CNAME 指向 `xubaojin.github.io`。

## 维护

- **内容更新**：编辑 `index.html` 对应板块
- **配色调整**：修改 `css/abao.css` 顶部 `:root` CSS 变量
- **图片替换**：覆盖 `images/` 下同名文件
