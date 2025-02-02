# TeamAssistantBot
## 專案報告書

### 概述
在需要跨領域合作的今天，我們時常需要與他人合作，但人與人之間的相處總是難免會遇到各種困難，例如：
* 專案剛開始找不到方向
* 小組報告task太多，不知道怎麼安排...
* 看到小組成員進度落後但不想扮黑臉催促大家
* 想罵某個組員卻太孬
* 組員在討論的時候我在睡覺，錯過討論想要大綱
* 大家討論開會時間，找不到共同有空時間
* 一直忘記小組代辦事項，又懶得自己記

你也有這種困擾嗎？森森，你的小組貓咪助理，幫你解決以上問題！

### 技術架構
- Linebot
    * Flex Message & Postback function
        * 使用Flex message搭配postback, uri event實作選單上各項按鈕部分
        
- 各項功能：基於 langchain 的架構結合 openAI 實作
    * Google Calender
        * 輸入行程名稱及希望加入該行程的時間，小組貓咪助理會協助引導將該行程加入 google 日曆
    * Meeting Arangement
        * 群組成員輸入可以開會的時間，記錄這些訊息到資料庫，並以「森森什麼時候開會」讓小組貓咪助理整理出所有成員皆有空的時間
    * Mood Tool
        * 判斷成員匿名訊息的情緒，在傳送訊息時會同時傳送一個描述匿名訊息情緒的貼圖
    * Reminder
        * 森森會將待辦事項的項目，透過語言模型，將剩餘任務以條列式發布到群組中
    * Schedule
        * 輸入專案主題及完成時限，貓咪助理會給出排程建議及甘特圖
        * 會自動切分子任務並分配合理負責人數
    * Search Info
        * 對langChain下指令，搜尋網路上的資料並整理網址給使用者
    * Summerize
        * 在每次收到成員訊息時將訊息資料(時間、發送訊息的用戶名稱、訊息內容)到本地端資料庫
        * 每次需要整理大綱時將資料提取出來，交給langChain執行summarize的指令
    * Todo List
        * 管理任務待辦清單，可以新增，完成和查看待辦清單

### Menu Demo

![](./SenSenMenu.png)

### More Detail

pleas refer to [Presentation](./黑客組_葛萊芬多加十分_簡報.pdf)

### Ref
[linebot-find-some](https://github.com/louis70109/linebot-find-some#readme)
