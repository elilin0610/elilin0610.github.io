**繁體中文** · [English](./README.md) · [日本語](./README.ja.md)

# 使用 Oak 框架製作的個人網站

這是依照作業 5 要求，以 Deno 和 Oak 製作的簡易個人網站。

## 環境需求

- 系統已安裝 Deno
- 能連上網路，以便從 deno.land 下載 Oak

## 執行方式

1. 在目前目錄開啟終端機。
2. 執行下列指令：

```
deno run --allow-net personalSite.js
```

3. 開啟瀏覽器，前往 `http://localhost:8000`。

## 功能

依照作業要求，不同路徑會顯示不同資訊：

- `/name`：姓名
- `/age`：年齡
- `/gender`：性別

其他路徑：

- `/`：首頁
- `/education`：學歷
- `/interests`：興趣
- `/skills`：技能
- `/all`：在同一頁顯示所有資訊

### 多語言支援

網站支援英文和中文：

- 網址後加上 `?lang=en` 可顯示英文版。
- 網址後加上 `?lang=zh` 可顯示中文版。
- 也可以使用各頁右上角的語言選單切換。

## 結構

- `personalSite.js`：主要應用程式檔案
- 使用樣板函式產生格式一致的 HTML 網頁。
- 每頁都包含導覽連結。
- 翻譯系統為每種支援的語言使用一份字典。

## 技術

- Deno
- Oak 網站框架
- HTML/CSS（網頁呈現）
