# rime_tyhgb_stroke
fcitx + ibus 筆畫輸入法Linux版; 包含五碼, 六碼; 以及臺灣, 大陸筆畫, 基於Rime


一. fcitx 安裝

0x01. 輪入法基於fcitx-rime(中州韻), 如果系統未安裝, 請先下載安裝ibus-rime

	Ubuntu Studio: 

	sudo apt install fcitx-rime

0x02. 激活 fcitx

	開始菜單 - 設定値 - 語言支援 (或開始菜單直接搜㝷: 語言支援) - 鍵盤輸入法系統 - 選擇fcitx

0x03. 添加輸入法

	開始菜單 - 設定値 - fcitx設定 (或開始菜單直接搜㝷: fcitx設定) - 輸入法 - 若無中州韻, 新增輸入法 - 中州韻

0x04. 配置中州韻

	選擇中州韻 - 設定 - Fcitx Rime Config

	shortcut: 快捷鍵管理

	schema: 輸入方案管理

0x05. 複製文件
	
	打開檔案管理員 - 進入 home/<user>/.config/ibus/rime, 俢改 default.custom.yaml(若沒有往下直接複製):

  schema_list:  # 按需添加, 詳情看後文, 不需要的在前面加#
筆順筆畫
    - {schema: cns}               # 五碼筆順(臺灣)
    - {schema: g6code}            # 六碼筆畫(香港)
    - {schema: stroke5_cn}        # 五碼筆順(大陸)
    - {schema: stroke5}           # 五碼筆畫(香港)
    - {schema: t9}                # T9筆順(大陸)
    - {schema: one_hand}          # 單手筆順輸入法(原作者字典, 改鍵盤輸入)

Ibus 自帶 (位於 /usr/share/rime-data/)
    - {schema: luna_pinyin_tw}			# 朙月拼音·臺灣正體
    - {schema: luna_pinyin}			# 朙月拼音
    - {schema: luna_quanpin}			# 全拚
    - {schema: luna_pinyin_simp}       # 朙月拼音簡體字版
    - {schema: luna_pinyin_fluency}	# 朙月拼音·臺灣正體
    - {schema: bopomofo}				# 註音
    - {schema: bopomofo_tw}			# 註音臺灣
    - {schema: cangjie5}               # 倉頡五代
    - {schema: stroke}                 # 五筆
    - {schema: terra_pinyin}           # 地球拼音（帶音調輸入，四聲用符號 -/<\ 或者 ;,/> 置於音節末尾）

    複製相關文件至 home/<user>/.config/ibus/rime

0x06. 部署
	
	點擊系統面板的Rime輸入法標記, 選擇“㞢（之）”圖標的“中州韻”Rime輸入法, 在彈出的菜單中選擇“重新部署”。看到有一個“Rime 準備好了”的提示後，就可以調用筆順輸入法打字了

0x07. Ctrl + ~ 或者 F4 快速調出輸入法 設置, 或在第0x04步設置

以上步驟有任何問題請重新登入系統

二. ibus安裝

0x01. 輪入法基於ibus-rime(中州韻), 如果系統未安裝, 請先下載安裝ibus-rime

	Ubuntu Studio: 

	sudo apt install ibus-rime

0x02. 激活 Ibus

	開始菜單 - 設定値 - 語言支援 (或開始菜單直接搜㝷: 語言支援) - 鍵盤輸入法系統 - 選擇Ibus

0x03. 添加輸入法

	開始菜單 - 設定値 - Ibus偏好設定 (或開始菜單直接搜㝷: Ibus偏好設定) - 輸入法 - 若無Rime, 加入 - 中文 - Rime

0x04. 複製文件
	
	打開檔案管理員 - 進入 home/<user>/.config/ibus/rime, 俢改 default.custom.yaml(若沒有往下直接複製):

  schema_list:  # 按需添加, 詳情看後文, 不需要的在前面加#
###筆順筆畫
    - {schema: cns}               # 五碼筆順(臺灣)
    - {schema: g6code}            # 六碼筆畫(香港)
    - {schema: stroke5_cn}        # 五碼筆順(大陸)
    - {schema: stroke5}           # 五碼筆畫(香港)
    - {schema: t9}                # T9筆順(大陸)
    - {schema: one_hand}          # 單手筆順輸入法(原作者字典, 改鍵盤輸入 + 12345)

###Ibus 自帶 (位於 /usr/share/rime-data/)
    - {schema: luna_pinyin_tw}			# 朙月拼音·臺灣正體
    - {schema: luna_pinyin}			# 朙月拼音
    - {schema: luna_quanpin}			# 全拚
    - {schema: luna_pinyin_simp}       # 朙月拼音簡體字版
    - {schema: luna_pinyin_fluency}	# 朙月拼音·臺灣正體
    - {schema: bopomofo}				# 註音
    - {schema: bopomofo_tw}			# 註音臺灣
    - {schema: cangjie5}               # 倉頡五代
    - {schema: stroke}                 # 五筆
    - {schema: terra_pinyin}           # 地球拼音（帶音調輸入，四聲用符號 -/<\ 或者 ;,/> 置於音節末尾）

    複製其餘文件至 home/<user>/.config/ibus/rime

0x05. 部署
	
	點擊系統面板的Rime輸入法標記, 選擇“㞢（之）”圖標的“中州韻”Rime輸入法, 在彈出的菜單中選擇“部署”。看到有一個“Rime is Ready”的提示後，就可以調用筆順輸入法打字了

0x06. Ctrl + ~ 或者 F4 快速調出輸入法 設置, 或在第0x04步修改重新部署設置

以上步驟有任何問題請重新登入系統

三. 鍵盤説明

一		QWERT
丨		YUIOP
丶		ASDFG
丿		HJKL
𠃌		ZXCVB
*?		NM

註: NM 目前未處理

四. 輸入法説明

0x01. cns	-	五碼筆順(臺灣)

	字典基於: 中文全字庫 https//:www.cns11643.gov.tw 

	鍵入方式: 按筆順順序輸入, 更多參考官方: 筆順基本法則說明.pdf


0x02. g6code	-	六碼筆畫(香港)
	
	字典基於: 香港城市大學電子工程學系布禮文博士開發團隊 六碼筆畫 http://www.miniapps.hk/g6code/

	鍵入方式: 前3 + 後3 (單字最多6筆), 更多參考官方

0X03. stroke5_cn	-	五碼筆順(大陸)
	
	字典基於: 五笔字型超大字符集编码数据库 https://github.com/CNMan/UnicodeCJK-WuBi/issues

	鍵入方式: 按筆順順序輸入, 更多參考官方

0X04. stroke5	-	五碼筆畫(香港)
	字典基於:  香港長者資訊天地 Hong Kong Seniors IT Advocates 筆順五碼中文輸入法 http://sf.net/projects/stroke5input

	鍵入方式: 前4 + 後1 (單字最多5筆)

0X05. t9	-	T9筆順(大陸)

	字典基於: T9 輸入法 https://github.com/microcai/ibus-t9 by microcai

	鍵入方式: 按筆順順序輸入, 更多參考官方

0X06. one_hand	-	單手筆順輸入法(原作者字典, 改鍵盤輸入 + 12345)
	
	字典基於: 单手笔顺输入法码表 stroke-seq_MB 2.0 版 https://github.com/YQ-YSY/stroke-seq_MB

	鍵入方式: 本版俢改按筆順順序輸入, 原版請使用官方

大陸 和 臺灣 區別, 如:丁:

	大陸: 一丨
	臺灣: 一𠃌

其他參考官方文檔
