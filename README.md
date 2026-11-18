# Pole-photo

線路定位地圖(line-map)的電桿照片與文字備註庫,透過 GitHub Pages 公開。

- `p/` 照片(標準長邊 1024)
- `t/` 縮圖(長邊 480)
- `i/<分片>.json` 照片索引 `{"線路#桿號":[{"f","at","t"}]}`
- `n/<分片>.json` 文字備註 `{"線路#桿號":[{"id","at","x"}]}`

分片 = 線路名稱(UTF-8)的 FNV-1a 32 位元雜湊 & 0xfff,三位小寫十六進位。
網頁直接用 GitHub API 寫入;紀錄網頁的照片每月由 line-map/tools/sync_photos.py 同步。
