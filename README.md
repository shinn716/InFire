# WS-Studio
WS-Studio（Worship Studio）是一個用於敬拜的簡報軟體，在延伸螢幕中同時顯示影片、歌詞及歌詞選單，同時也支援快速修改歌詞，包含文字大小、顏色、外框、字型...等功能。  
  
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/demov2.gif" /></a>  

## 下載連結
https://github.com/shinn716/WS-Studio/releases

## 環境
 - 支援平台：Windows
 - 支援語言：中文
 - 限制：需使用延伸螢幕（至少外加一螢幕）
 - 限制：只支援以下字體（英文為系統預設）：  
    微軟雅黑體 / Microsoft YaHei、  
    微軟正黑體 / Microsoft JhengHei、  
    標楷體 / DFKai-SB、  
    細明體 / MingLiU、  
    新細明體 / PMingLiU、  
    宋体 / SimSun、  
    台北黑體 / Taipei Sans TC Beta  

## 安裝
1. 解壓縮後 WS-Studio.zip
2. 確定延伸螢幕已運作（主顯示器為1、副顯示器為2）
3. 執行 WS_Studio.exe

## 操作
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/Snipaste_2021-10-31_15-55-32.png" width=50% height=50% /></a>  
上方畫面為副顯示器、下方為主顯示器  

## 控制
1. 鍵盤右鍵，下一頁、左鍵，前一頁。
2. 鍵盤上鍵，Dashboard 捲軸向上捲動、捲軸向下捲動。

## 新增/更換歌詞
1. **修改歌詞（xxx.txt）**  
  a. 開啟文字檔  
從路徑開啟文字檔，``.../WS_Studio/WS_Studio_Data/StreamingAssets/lyrics/歌名1.txt``  
右鍵開啟（Windows使用Note開啟或任何文字編輯軟體）  
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/Snipaste_2021-10-31_15-39-53.png" width=50% height=50% /></a>  
(照片為MAC OS系統，建議使用 Windows 環境下修改)  
  b. 修改或新增歌詞  
依照以下照片規則新增歌詞  
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/Snipaste_2021-10-31_15-48-40.png" width=50% height=50% /></a>  
  c. Dashboard 文字外框提示  
顯示在主畫面的 Dashboard，提示：副顯示會自動把歌詞中的 V、C、B、P，這幾個文字過濾，不會顯示在螢幕上  
**V**表示為主歌（綠色）、**Ｃ**表示為副歌（紅色）、**B**表示為Bridge（藍色）、**P**表示為PreC（青色）  
  d. 設定歌詞順序  
在檔名部分標頭加入數字，讓系統自動排序，如下圖：  
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/Snipaste_2021-10-31_16-46-17.png" width=20% height=20% /></a>  
勿使用[1]歌名、（1）歌名、1_歌名，命名方式只能使用 **1歌名**，系統會自動抓取檔名（並去除數字）顯示在主、副顯示器中。  
  
2. **修改設定檔（xxx.json）**  
  a. 開啟設定檔  
從路徑開啟文字檔，``.../WS_Studio/WS_Studio_Data/StreamingAssets/lyrics/歌名1.json``  
右鍵開啟（Windows使用Note開啟或任何文字編輯軟體）  
<img src="https://github.com/shinn716/WS-Studio/blob/main/img/Snipaste_2021-10-31_16-13-13.png" width=50% height=50% /></a>  
  b. 修改設定檔
  設定檔只能修改內容數值，不可修改參數名稱
 ```
  {
  "VideoUrl": "Navidad 3.mp4",      // 影片路徑
  "Font": "Taipei Sans TC Beta",    // 字型
  "FontStyle": "Bold",              // 字體加粗（歌詞和歌名）
  "ShowName": "TRUE",               // 是否顯示名稱（只能填入TRUE/FALSE）
  "NameSize": 75,                   // 歌名大小
  "FontSize": 120,                  // 歌詞大小
  "FontColorHex": "#FFFFFF",        // 歌詞顏色 
  "NameColorHex": "#FFFFFF",        // 歌名顏色
  "Outline": "TRUE",                // 是否顯示外框
  "OutlineSize": "3",               // 外框大小
  "OutlineColor": "#000000"         // 外框顏色
}
```
顏色修改為 hex color，請參考以下網址：  
https://www.w3schools.com/colors/colors_picker.asp. 
  
**4. 新增影片**
1. 將影片複製至 ``.../WS_Studio/WS_Studio_Data/StreamingAssets/videos/``
2. 設定檔 VideoUrl 修改成對應名稱（注意副檔名，.mp4 / .mov）
  
**5. 新增歌詞**
1. 只需將 ``1歌名1.txt``、``1歌名1,json`` 複製，並將檔名修改即可 ``2歌名2.txt``、``2歌名2,json``。
    
## LICENSE
[Apache 2.0 license](LICENSE)
