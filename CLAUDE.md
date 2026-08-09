# hamradio-course

**`kansasray/gym-course`(自有框架 fork)的 clone,放一門課:`courses/hamradio/`「業餘無線電之路」。** 框架負責建置稽核驗證部署;課程內容全在 `courses/hamradio/`;`courses/gym/` 是上游對照範例不要動。

課程:台灣 NCC 三等考照導向,3 部 9 章(考照與法規/原理與操作/裝備天線與應用)、24 單元 53 支影片、8 小時 35 分。考照/法規/天線/車機章中文主軸(八雲無線、青溪無線電骨幹),原理與數位模式混語(英文系統性頻道+繁中導讀)。不建 citations、不宣告 grades(立場頁標籤直寫 evidence_grade)。

## 指令
```bash
COURSE=courses/hamradio make build audit verify
COURSE=courses/hamradio COOKIES_BROWSER= uv run python src/build/fetch_meta.py
```

## 這門課的特殊紀律(改動前必讀)

1. **管轄權是這門課的生死線。** 簡中頻道講的是中國工信部/CRAC 制度,與台灣 NCC 不通用:制度/考照/流程類簡中內容一律排除;**純技術操作**(設備/寫頻/物理原理)可收但標明。策展期間曾誤收「科技小汪」(中國頻道)的執照流程影片,經三個 agent 交叉比對後撤換 —— 判別法:頻道其他影片的計價幣別、呼號分區(中國 B+數字/台灣 BM-BX)、機型生態、用語(芯片/信道 vs 晶片/頻道)。
2. **三等的 HF 權限:1.8–29.7MHz 全頻段零配額,50MHz 起才有 25W。** CH8 策展時從全國法規資料庫下載《業餘無線電人員及電臺管理辦法》附表 PDF 實讀確認(FileId=0000273399)。片中的英國 Foundation/美國執照制度不可類比,導讀已標。
3. **舊制陷阱**:2007-05-14 起四等制改三等/二等/一等(已查證法規資料庫),此前的考照內容全部過時。
4. **留白 6/8**:NCC 考科「電磁相容性技術」「射頻干擾之預防及排除」中英文全網零教學影片(29 組關鍵字查證),CH3 大量留白導向題庫自讀;CH2 的頻段功率專門教學同樣查無。audit 的 3 個警告(留空/主課偏短/缺 why)全是留白的預期產物。
5. **刻意跨章共用 1 支**:`0Xz2v4eF9sU`(BV6LC)CH1 用考照時程段、CH3 用 Anki 記憶法段,因台灣管轄權確認的考照內容極稀。
6. 未考照前勿發射:發射類操作的導讀都標「考照後再做」,footer 有免責。

## 關鍵字污染清單(策展實測,補片時照抄)
`FT8`→撲克/Minecraft;`D-STAR`→歌台舞蹈;`中繼台`→棒球/WiFi 路由器;`防災 無線電`→日本市政廣播喇叭;`Q碼`→QR code;`天線`→電視/WiFi 天線;`CTARL`→動畫角色。查詢一律帶「業餘」或「無線電」或「ham」。

## 框架陷阱
同 atak/pilot/firstaid 的清單。新增一條:**資料檔的 tight/weak 欄位是健身課殘留,寫了不顯示**(CH4 曾誤用,已併回 assessment)。

## 狀態(2026-08-10 完成)
- **verify 53/53、audit 0 錯誤 3 警告(皆留白產物)、89 tests**;頻道最高佔比 9.4%
- **已上線 https://hamradio-course.pages.dev**(Pages 專案 hamradio-course)
- **GitHub**:kansasray/hamradio-course(public,Discussions 已開,giscus 已填待裝 App)
