# Bopomo_Ligasystem

- 注音合字架構系統
- 授權：免費個人使用，需註明引用出處。商用請聯繫另洽授權方式。

---

# 參考諺文作法結構

參考韓語諺文[作法](https://glyphsapp.com/learn/creating-a-hangeul-font)，將符號分為初聲、中聲、終聲（前中後）
</br>
<img src="https://cdn2.glyphsapp.com/media/pages/learn/creating-a-hangeul-font/baed15ae07-1624987025/hangul-character-1280x-q80.webp" width="450">

---

# 字型使用－輸入法選擇

- 注音輸入法：以漢字為主，注音符號只能輸入大顆。
- 英文輸入法（最終使用）：英文數字符號輸出，符號間組合自由度高。

---

# 字型使用－輸入效果

- 輸入時以鍵盤上的注音符號位置為準，一聲時不必按空白鍵。
- 小寫模式輸入為標音模式，按住shift輸入時為單顆模式。
- 文字方向橫排為上標，直排為側標模式。

---

# 檔案結構－字符名稱

- `m-bopomofo`：原始注音字符位置（造型編輯處，紅色標籤）
- `A`：單顆造型
- `a`：上標一聲造型
- `a.vert`：側標一聲造型
- `a_j`：組合上標造型
- `a_j_three`：組合上標加聲調造型（三聲）

---

# 檔案結構－位置

原始位置、第二位置（`Pos2`）和第三位置（`Pos3`）

<table width="100%">
  <tr>
  <td width="33%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/023.png'></td>
  <td width="33%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/024.png'></td>
  <td width="34%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/025.png'></td>
  </tr>
</table>

標籤顏色：黃色、綠色、橘色

---

# 檔案結構－聲母、介音和韻母

<img src="" width="450">

ㄅㄧㄠ（聲母－介音－韻母）
標籤顏色：淺藍色、紫色、藍色

---

# 檔案結構－橫排和直排

<table width="100%">
  <tr>
  <td width="33%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/013.png'></td>
  <td width="33%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/014.png'></td>
  <td width="34%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/015.png'></td>
  </tr>
</table>

後綴`.vert`為直排用字符，在左側搜尋框輸入可單獨過濾出直排字符。
[Glyphs論壇關於.vert和.vrt2的討論](https://forum.glyphsapp.com/t/position-of-the-component-in-vert-glyph/2915/1) 

---

# 檔案結構－聲調

- 原聲調字符用紅色標籤標記。
- 觀察聲調位置都在最末字符右上處，因此將聲調統一與韻母組合。
- 基於規則統一，輕聲亦先與韻母組合。

---

# 檔案結構－Pos3的輕聲位置

<table width="100%">
  <tr>
  <td width="50%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/025.png'></td>
  <td width="50%"><img src='https://language.moe.gov.tw/001/Upload/files/site_content/M0001/juyin/html_ch/images/026.png'></td>
  </tr>
</table>

- 無論直橫排都有輕聲讓位的狀況
- Pos3聲母多製作一個輕聲專用的後縮版本，後面字符以錨點吸附便可自動跟隨後縮。

---

# 有用腳本（批次組件編輯）

mekkablue：尋找取代組件、移動組件、刪除組件
Mark2Mark：停用組件自動就定位
Toshi Omagari：拆開組件

