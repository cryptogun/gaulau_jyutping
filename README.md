# Intro 简介  
This is a Chinese input schema of Cantonese subdialect named Gaulaupin.  
Design is based on the [Jyutping](https://en.wikipedia.org/wiki/Jyutping) romanisation system.  
It can be used in [Rime](https://rime.im/), a universal cross platform Input Method Engine.  

这是一个勾漏粤拼输入方案。方言片区为粤语勾漏片，再细分则属于藤县白话。  
本方案可以在[Rime输入法](https://rime.im/)里导入并使用。  
此方案基于粤拼方案，以后可能另外开一个repo，设计一套基于普通话拼音的白话输入方案。  

更新的原因： 本方案的原[repo](https://github.com/cryptogun/rime-jutjnyu_gaulaupin_dangjunbikwaa)命名太长，与其他方案不统一，而且久不维护了。另起灶炉吧。
  
# 正名
`勾漏片`是正确的说法，`勾`没有三点水。以方言所在地命名。  
广西省北流市内的勾漏山、勾漏洞。《辞海》记载`溶洞勾曲穿漏，故名。` -[勾漏洞百科词条](https://baike.baidu.com/item/%E5%8B%BE%E6%BC%8F%E6%B4%9E)

-----------------------------------  
# 使用方法  
1. 安装Rime输入法
    - 前往官网下载输入法 http://rime.im  
1. 下载本输入方案的2个文件
    - [gaulau_jyutping_dangjun.dict.yaml](https://github.com/cryptogun/gaulau_jyutping/blob/master/gaulau_jyutping_dangjun.dict.yaml)
    - [gaulau_jyutping_dangjun.schema.yaml](https://github.com/cryptogun/gaulau_jyutping/blob/master/gaulau_jyutping_dangjun.schema.yaml)
1. 移动这2个方案文件到Rime输入法文件夹下面
    - Windows： 文件夹是 `%AppData%\Rime`
        + 打开文件夹的方法： 在文件管理器地址栏输入  
            `%AppData%\Rime`  
    - Mac： 文件夹是 `~/Library/Rime`
    - Linux： 文件夹是 `~/.config/ibus/rime/`）
1. 告知Rime输入法： 新输入方案已追加
    - 打开Rime的配置文件
        - Windows：`%AppData%\Rime\default.custom.yaml`
            + 打开文件的方法： 在文件管理器地址栏输入  
                `%AppData%\Rime\default.custom.yaml`  
        - Mac：`~/Library/Rime/default.custom.yaml`
        - Linux：`~/.config/ibus/rime/default.custom.yaml`）
    - 添加一行文字：
        ```yaml
        #文件路径是： %AppData%\Rime\default.custom.yaml
        patch:
          schema_list:
            #找到这一缩进的层，添加下面一行文字
            - {schema: gaulau_jyutping_dangjun}
        ```

1. 通知系统使用Rime输入法
    - 按`Ctrl`+`Shift`
    - 打字 测试现在用的是不是Rime输入法

1. 通知Rime输入法： 编译、重新部署
    - Windows: 在文件管理器地址栏输入`%programdata%\Start Menu\Programs\小狼毫輸入法\`  
    - 按`Enter`
    - 找到`【小狼毫】重新部署`并双击打开

1. 通知Rime输入法： 使用勾漏粤拼
    - 按`F4`打开Rime方案菜单
    - 按数字键选择`勾漏粤拼藤县白话`

1. 通知Rime输入法： 输出简体
    - 按`F4`打开Rime方案菜单
    - 按`2`： `西/半/汉/。`
    - 按`4`： `漢字 -> 汉字`可以在简繁之间切换
  
-----------------------------------  
# 方案说明  
![](https://raw.githubusercontent.com/cryptogun/gaulau_jyutping/master/%E7%B2%A4%E8%AF%AD%E6%B2%9F%E6%BC%8F%E7%89%87%20%E7%B2%A4%E6%8B%BC%E5%A3%B0%E9%9F%B5%E6%AF%8D%E8%A1%A8.PNG)  
本拼音方案完备性依据的是《藤县志》所提供的声母韵母表。  
拼写方法借鉴《香港语言学学会粤语拼音方案》并稍作增删。  
- 香港粤拼方案是“目前标准化程度最高也是最普遍的一种粤拼形式。”——维基百科。  

读音准确性参考母语和广府片标准音发音（主要来自cn.voicedic.com）。  
准确性有待集体的贡献，欢迎Fork和Pull request或者提issue。  

## 声母  
总共20(24)个：  
`b c d f g h j jn k l m n ng p s t th w z 0 (+ b d gw kw)`  
香港粤拼方案：  
-  j：
    + 是普通话的'y'而非'jqx'。  
-  ng：
    + 表示鼻音[ŋ]，就如'ang','eng','ing,''ong'，故取ng作声母。  
本方案：  
-  th：
    + 对应于国际音标[θ],KK音标/θ/，取英语(think)前2字符th
    + 例字： 锁心想醒扫送就笑  
-  jn：
    + 对应于国际音标[ɲ]（维基百科条目‘硬颚鼻音’），转写作'jn'
    + 例字： 抓闰鱼肉日饮入忍惹软儿热乳。
    + 读音类似于`Español`里的`ñ`。  
    + 读音类似于`canyon`里的`ny`，用藤县话标注是`砍人`。  
  
-  d: 有两种音

|d1|d2|
|---|---|
|做|堵|
|租|都|
|灶|到|
|糟|刀|
|早|倒|

错例：倒上好  
-  b: 有两种音

|b1|b2|
|---|---|
|悲|B|
|摆|单词bye|
|表|嫖|
|崩|朋|
|伯|白|
|博|薄|

又比如

|ā|á|ǎ|à|b|
|---|---|---|---|---|
|宝|2|3|煲|b1|
|1|抱|暴|4|b2|
|饼|2|3|冰|b1|
|1|并|病|4|b2|

错例：悲超  
为方便键盘输入，各合并成一个键。  
b1的字，发音时后上颚要用力收缩，说多了会很累。  
实际说话中是有区分的。个人感觉随着语言演化，这么细微的区分有消失的主观必要。  

-  gw：本人听不出跟g的区别。暂时将gw==g等同。以后有必要再用Regex进行批量修改或逐个修改。  
-  kw：本人听不出跟k的区别。暂时将kw==k等同。以后有必要再用Regex进行批量修改或逐个修改。

-----------------------------------  
## 韵母  
总共50(50)个：  
`aa aai aak aam aan aang aap aat aau ai ak am an ang ap at au e ek em en eng ep eu i ik im in ing ip it iu m ng o oe ok om on ong op ot ou u ui uk un ung ut yu`  
在香港粤拼的基础上：
- 等同：  
    + oi==oe
    + yut==ut
    + iaang==en
    + iaau==eu
- 容错：  
    + ei=>ai  
- 删去：  
    + eoi=>ui
    + eon=>an
    + oeng=>eng
    + eot=>at
    + oek=>ek
- 加入：
    依据《藤县志》所列声、韵母表加入：  
    + en：片，扁（头扁、压扁）。 
    + om：含，感。 
    + op：盒，鸽。  
  
-----------------------------------  
# 方案缺陷  
- 缺少音调  
- 一些音变不进行区分 有待语言学家探讨(本人不是)
    + b1=b2，d1=d2
    + gw=g，kw=k
    + vt=ut
- 缺少藤北音  
- 参与征集读音的人少，可能导致错音、漏音、适用范围窄  
- 经常使用本方案输入，可能会导致普通话生疏、不标准  
  
-----------------------------------  
# 本方案记忆技巧  
（别问我为什么这么编码，我也不知道。这是香港佬弄的粤拼 :)  
  
|音标|例子|
|---|---|
|aa|啊|
|aai|矮|
|zaang|橙|

嘴都是开大口，且音长，故2个a: aa。  
  
|音标|例子|
|---|---|
|ai|唉|
|an|恩|
|ang|哽|

开口小，故1个a。  
  
|音标|例子|
|---|---|
|e|写|

嘴扁，像e。  
  
|音标|例子|
|---|---|
|o|哦|

嘴圆，像o。  
  
|音标|例子|特征|
|---|---|---|
|aang|讲|长|
| ang|鹰|短|
| ing|应|i衣|
| ung|嗡|u像双手往外推“拱”|
| ong|讲|圆|
| eng|响|咧嘴|
  
|音标|例子|
|---|---|
|j|有|

是普通话的“y”，粤拼Jyutping `/j yut ‘ping/`首字母本身就是例子。  
  
|音标|例子|
|---|---|
|ptk结尾|鸭热甲|

入声调。分辨方法：短促发声的字。  
  
  
## 声调科普  
  
|例字|声调|解释|
|---|---|---|
|诗史试|1 2 3|高昂，频率高，逐字降调。|
|市时事|4 5 6|低沉。|
|色勺食|7 8 9|短促，高中低，阳入 中入 阴入。|

感觉像不像钢琴的同样是一个按键却有不同的音？这就叫音调。  
  
-----------------------------------  
# 参考资料  
cn.voicedic.com 本人母语 藤县志 几篇期刊 www.zdic.net  
感谢以上各项目  
