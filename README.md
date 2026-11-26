# Keigo's Pages

Keigo 的靜態網頁收藏。純 HTML / CSS / JavaScript，沒有建置流程、沒有外部依賴，任何靜態主機都能直接部署。

## 目錄結構

```
keigo-pages/
├── index.html              # 首頁，列出所有收錄頁面（深淺色自動跟隨系統，按 T 切換）
├── doomsday/
│   └── index.html          # 《復仇者聯盟：末日崛起》終極懶人包
└── README.md
```

每個頁面都是一個資料夾，入口固定為該資料夾的 `index.html`，因此網址就是 `/資料夾名稱/`。

## 新增頁面

1. 在根目錄建立新資料夾，例如 `my-page/`，把單頁 HTML 放成 `my-page/index.html`。
2. 在根目錄 `index.html` 的「收錄頁面」區塊複製一張 `.card`，把 `href` 改成 `./my-page/`，再改標題與描述。
3. commit 並 push，部署會自動更新。

## 部署到 Vercel

### 方式一：從 GitHub 匯入（推薦，push 後自動部署）

1. 登入 [Vercel](https://vercel.com)，按 **Add New… → Project**。
2. 選擇 **Import Git Repository**，授權並挑選 `keigoweiTW/keigo-pages`。
3. Framework Preset 選 **Other**，Build Command 與 Output Directory 都留空（純靜態檔，根目錄即輸出目錄）。
4. 按 **Deploy**。之後每次 push 到 `main`，Vercel 會自動重新部署。

### 方式二：用 Vercel CLI

```bash
npm i -g vercel
cd keigo-pages
vercel          # 預覽部署
vercel --prod   # 正式部署
```

## 本機預覽

```bash
python3 -m http.server 8000
# 開啟 http://localhost:8000/
```

## 授權

個人使用，內容為私人整理，版權素材（如電影劇照、角色名稱）權利歸原權利人所有。
