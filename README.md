# images — 圖庫 Repo

這個 repository 作為**線上圖床／圖庫**使用。

把圖片檔案 push 上 GitHub 後，就能透過 `raw.githubusercontent.com` 取得每張圖的直接連結，方便貼到發文、文件、聊天或任何需要外部圖片網址的地方。

## 連結格式

```
https://raw.githubusercontent.com/nate0815/images/master/<資料夾>/<檔名>
```

- 中文檔名／資料夾名需經過 URL encode（例如「發文素材」→ `%E7%99%BC%E6%96%87%E7%B4%A0%E6%9D%90`）。
- **資料夾一旦改名，舊的連結就會全部失效（404）**，記得同步更新引用到這些網址的地方。

## 資料夾

- [`2026GameJam_asset/`](2026GameJam_asset/) — 2026 GameJam 發文素材，內含各圖的預覽與連結清單。

## 給 Claude 的固定流程 🤖

> 每次我請你上傳（push）新圖片之後，請自動幫我完成以下流程，不用再另外問：

1. 把新圖片 `git add` → `commit` → `push` 到 `master`。
2. 針對每張**新上傳**的圖，在該資料夾的 `README.md` 內依現有格式補上一個區塊：
   ```
   ![檔名(不含副檔名)](raw 連結)

   `raw 連結`

   ---
   ```
   - 連結用 `https://raw.githubusercontent.com/nate0815/images/master/<資料夾>/<檔名>` 格式。
   - 檔名／資料夾若含非 ASCII 字元，需 URL encode。
3. 把更新後的 `README.md` 一起 commit & push。
4. 回報每張圖的可用連結給我。
