#README  
rime-jutjnyu_gaulaupin_dangjunbikwaa  
This is a schema for Rime Input Method Engine about jutjnyu gaulaupin. 这是一个Rime输入法的粤语沟漏片藤县白话输入方案。  
  
-----------------------------------  
#使用方法  
法一：  
- 1.安装Rime输入法 http://rime.im；  
- 2.下载“`jutjnyu_gaulaupin_dangjunbikwaa.dict.yaml`”和“`jutjnyu_gaulaupin_dangjunbikwaa.schema.yaml`” 两个文件，复制到“`【小狼毫】用戶文件夾`”下（Windows：`%AppData%\Rime`，Mac：`~/Library/Rime`，Linux：`~/.config/ibus/rime/`）（找不到？Windows的话，点击左下角开始按钮，搜索框输入`%AppData%\Rime`即可找到。）；  
- 3.“`【小狼毫】用戶文件夾`”内，找到`default.custom.yaml`，用文本编辑器打开，在	`schema_list:`下，添加一行：
`    - schema: jutjnyu_gaulaupin_dangjunbikwaa`  
- 4.重新部署，参见：https://github.com/rime/home/wiki/RimeWithSchemata#%E4%BD%88%E7%BD%B2-rime ；  
- 5. `<Ctrl>`+``<`>`` 切换到粤语沟漏片藤县白话输入方案。  
  
法二（只适用于Windows平台）：  
- 1.安装Rime输入法 http://rime.im；  
- 2.下载`jutjnyu_gaulaupin_dangjunbikwaa-1.0.0.2.exe` ；  
- 3.双击安装exe文件，即可。  
  
  
找不到下载地方？  
右中部，有`Download ZIP`按钮。  
或者，右键点击最上面的文件名，链接另存为，即可弹出下载对话框。  
  
  
-----------------------------------  
#方案说明：  
本拼音方案依据为《藤县志》所提供的声母韵母表。拼写方法借鉴《香港语言学学会粤语拼音方案》并稍作增删。读音参考母语和广府片标准音（cn.voicedic.com）。  
香港粤拼方案是“目前标准化程度最高也是最普遍的一种粤拼形式。”——维基百科。  
##声母：  
总共20(24)：b c d f g h j jn k l m n ng p s t th w z 0 (+ b d gw kw)  
香港粤拼方案：  
-  j：是普通话的'y'而非'jqx'。  
-  ng：表示鼻音[ŋ]，就如'ang','eng','ing,''ong'，故取ng作声母。  
本方案：  
-  th：对应于国际音标[θ],KK音标/θ/，取英语(think)前2字符th。例字：锁心想醒扫送就笑。  
-  jn：对应于国际音标[ɲ]（维基百科条目‘硬颚鼻音’），转写作'jn'。例字：抓闰鱼肉日饮入忍惹软儿热乳。读音类似于“Español”里的“ñ”。  
  
-  d:有两种音。做-堵，租-都，灶-到，糟-刀，早-倒 错例：倒上好。  
-  b:有两种音。悲-B  错例：悲超。更多对比：摆（bye），表嫖，宝23煲|1抱暴4，饼23冰|1并病4，崩朋，伯白，博薄。  
    为方便键盘输入，各合并成一个键。实际中请注意区分。  
-  gw：本人听不出跟g的区别。暂时将gw==g等同。以后有必要再用Regex进行批量修改或逐个修改。  
-  kw：本人听不出跟k的区别。暂时将kw==k等同。以后有必要再用Regex进行批量修改或逐个修改。
-----------------------------------  
##韵母：  
总共50(50)：aa aai aak aam aan aang aap aat aau ai ak am an ang ap at au e ek em en eng ep eu i ik im in ing ip it iu m ng o oe ok om on ong op ot ou u ui uk un ung ut yu  
在香港粤拼的基础上，删去（容错）：  
-  eoi=>ui eon=>an oeng=>eng eot=>at oek=>ek  
依据《藤县志》所列声、韵母表，加入：  
-  en：片，扁（头扁、压扁）。 om：含，感。 op：盒，鸽。  
等同：  
-  oi==oe yut==ut iaang==en iaau==eu  
容错：  
-  ei=>ai  
  
-----------------------------------  
#方案缺陷：  
- 缺少音调。  
- b1=b2，d1=d2，不区分。  
- gw=g，kw=k，不区分。  
- 缺少藤北音。  
- 参与征集读音的人少，可能导致错音、漏音、适用范围窄。  
- 经常使用本方案输入，可能会导致普通话生疏、不标准。  
  
-----------------------------------  
#本方案记忆技巧：  
（别问我为什么这么编码，我也不知道。这是粤拼Jyutping，香港佬弄的。可能与拉丁、罗马之类有关。）  
 aa   啊  
 aai  矮  
zaang 橙  
嘴都是开大口，且音长，故2个a，aa。  
  
ai  唉  
an  恩  
ang 哽  
开口小，故1个a。  
  
e 写  
嘴扁，像e。  
  
o 哦  
嘴圆，像o。  
  
aang 讲 长  
 ang 鹰 短  
 ing 应 i衣  
 ung 嗡 u像双手往外推“拱”  
 ong 讲 圆  
 eng 响 咧嘴  
  
j 是普通话的“y”，粤拼Jyutping /j yu t‘p ing/本身就是例子。  
  
ptk结尾  
分辨：短促发声的字，雅称“入声”。  
  
  
##科普下声调：  
  
诗史试 1 2 3 高昂，频率高，逐字降调。  
市时事 4 5 6 低沉。  
色勺食 7 8 9 短促，高中低，阳入中入阴入。  
  
-----------------------------------  
#参考文献：  
cn.voicedic.com 本人母语 藤县志 几篇期刊 www.zdic.net 网络。感谢所有！  