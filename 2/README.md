# 🌌 专属恋爱网站（星空宇宙版）

## 怎么打开
直接双击 `index.html` 用浏览器打开即可，无需服务器。

## 怎么改成你们的信息
所有内容都集中在 **`config.js`** 一个文件里，用记事本/VS Code 打开修改：

| 想改什么 | 改哪里 |
|---|---|
| 你们的昵称 | `yourName` / `herName` |
| 在一起的日期 | `anniversary`（格式 YYYY-MM-DD） |
| 首页那句宇宙情话 | `universeLine` |
| 情书内容 | `loveLetter` |
| 摘星小游戏里的情话 | `starMessages` 数组 |
| 页脚小字 | `footer` |

## 怎么放照片
1. 把照片复制进 `images` 文件夹（如 `images/1.jpg`）
2. 在 `config.js` 的 `photos` 里取消注释并填写：
   ```js
   photos: [
     { src: "images/1.jpg", caption: "我们的第一次约会" },
     { src: "images/2.jpg", caption: "第一次一起看的电影" },
   ],
   ```
3. 不放照片时会显示占位卡片，不影响浏览。

## 想发给她变成公网链接？
两种简单方式：
- **Cloudflare Tunnel**（帖子里的方法）：
  在本目录运行 `npx serve .` 起本地服务，再 `cloudflared tunnel --url http://localhost:3000` 得到临时公网链接
- **Cloudflare Pages / Vercel / Netlify**：把整个文件夹拖上去，得到永久链接

需要的话我可以帮你一步步部署。
