# EZMacDict
Generate the codes needed for  Dictionary Development Kit by Apple to create a very simple custumized Mac Dictionary.
產生給蘋果「Dictionary Development Kit」軟體所需要的檔案，製作客製化的字典
## Requirement
* Xcode 7 以上（我用 Xcode 8）
* Dictionary Development Kit
* Python 3.5 以及 Pandas 函式庫
Documents
* MS xlsx 格式試算表，裡面有「中文名稱」與「英文名稱」兩欄
#使用方法
1. 先用文字編輯器開啟 MakeMacDictXHTML.py 檔案，移到最下面更改上一節提到的客製化部分。
2. 將 MakeMacDictXHTML.py 放在你的 xlsx 相同資料夾下。
3. 執行 python 產生製造字典必要的檔案。
`python MakeMacDictXHTML.py`
4. 確定你的 DDK 在「/Developer/Extras/Dictionary Development Kit」路徑，否則請在產生的 Makefile 中更改「DICT_BUILD_TOOL_DIR」參數的位置。
5. 在完成的資料夾中，執行「`make`」指令，之後會產生一個「objects」的資料夾，生成的檔案會在這邊（如：*國家教育研究院地球科學名詞_NAER_Geology_Dictionary.dictionary*）。複製這個檔案到「`~/Library/Dictionaries`」即可使用。
    如果你想直接安裝到你的字典位置（`~/Library/Dictionaries`），你也可以用「`make install`」。

## Blog Articles
如果你想瞭解其他細節，可以參考 [這邊](https://lcarbon.idv.tw/py-%e8%87%aa%e8%a3%bdmac%e8%be%ad%e5%85%b8%ef%bc%88%e4%b8%8a%ef%bc%89/) 與[這邊](https://lcarbon.idv.tw/py-%e8%87%aa%e8%a3%bdmac%e8%be%ad%e5%85%b8%ef%bc%88%e4%b8%8b%ef%bc%89/)
