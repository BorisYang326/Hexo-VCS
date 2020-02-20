---
title: Covid-19 Deployment
mathjax: true
categories: "Deploy 計劃"
date: 2020-02-06,22:17
updated: 
---

# 「 假 期 自 救  」

> Affected by the Catastrophe-epidemic **『Covid-19』**. The semester IV (2020 Spring) will delay to March 2^nd^.  This blog will give a deployment for the next three weeks.

<!-- more -->

<!--more-->

之前本來是有寫過的，因為 `reinstall hexo` 的原因丟失了。今天終於用 `Hexo+Nginx ` 實現了自動化部署 *blog* 所有也是終於閒下來去寫一些東西了。今天主要統計一下整體的 WorkLoad 。

- 首先是關於Semester IV的課程任務。

  - CS110 「 Computer Architecture 」

    這方面主要還是希望重點去做。目前的準備有

    - CMU的[15-231-fall 15](http://www.cs.cmu.edu/afs/cs/academic/class/15213-f15/www/schedule.html) 「視頻 / 課件」
    - 「**CSAPP**」0-500 page
    - Other Useful Link [*小土刀的Blog*](https://wdxmzy.com/categories/CSAPP/page/2/)
  
  - CS151「 Machine Learning & Optimization 」
  
    這部分原本是準備了 ***Coursera*** 的[Machine Learning](https://www.coursera.org/learn/machine-learning?) 。現在申請了Financial Acid，所以還是要每天學習希望能拿到證書。

- 然後是關於『**VRVC-Lab**』 的問題。
  - 主要還是先熟悉 「深度學習 & 視覺 & 卷積神經網絡」等概念。這裡還是採用網課的形式。執行 **Stanford CS231n** .
  - 「Optional」熟悉 「Pytorch」可以进行简单地「張量 Tensor」運算。搭建簡單的 CNN。

- 最後是學生會組織聯絡部。
  - 文檔「標準化 Standardization」
  - 社團大會電子手冊
  - 人事變動  / 其他事宜 「To Be Determined」

------
This deployment will be「**Revised** **& Updated**」 by everyday 11:59 UTC+8 .

截至每晚11：59之前會匯總當天完成量並進行下一次部署。

-----

> Updated at 2020-02-09 12:56 UTC+8

&#x2718; 『**CSAPP**』p133 

&#x2756;  CMU [課件][cmu] 「Lec I / II / III 」「Revise」
<!-- &#x2611/12/13/14/17/18; Main-Style「2610 2714 2718 2756」 -->

&#x2718;  [Coursera][ml] 「Week 1 Introduction 」

&#x2714; ~~組織聯絡部預會議~~

------
> Updated at February 10, 2020 at 10:52:11 AM GMT+8 

&#x2718; 『**CSAPP**』p133  

&#x2718;   CMU [課件][cmu] 「Lec I / II / III 」「Revise」

&#x2718;   [Coursera][ml] 「Week 1 Introduction 」  ~~<span style ='color : red'>『DDL Today！』</span>~~ 「Delay」

> 因為突然購置「Bandwagon CN2 GIA-E」服務器一台然後就開始轟轟烈烈地 『Torjan』之旅。<span style='color:rgb(88, 70, 10)'> 「 We do Cause we can.  」 </span>

-----

> Updated at February 11, 2020 at 4:25:21 PM GMT+8 

<span style='color:green'> &#x2714;</span> 「疫情期」第一次工作會議記錄整理  + Modify PDF

<span style="color:red">&#x2718;</span>     <span style='color:red'>[Coursera][ml] &#9873;&#9873;</span>「Week 1 Introduction」

<span style="color:red">&#x2718;</span>   優先看「CSAPP」「P0-P133」

-----
> Updated at February 14, 2020 at 12:44:31 AM GMT+8

<span style='color:green'> &#x2714;</span>  15-213 「視頻」Lec 02 Quarter.
<span style='color:green'> &#x2714;</span> Modified Blog
<span style='color:FIREBRICK'>&#9874;</span> Sub-categories Implementation 
<span style='color:FIREBRICK'>&#9874;</span> Table CSS Custom
<span style='color:FIREBRICK'>&#9874;</span> Tencent COS picture bed
因為上述 「递归式 Support」時間太長導致很多Tasks沒有完成。

-----
> Updated at February 16, 2020 at 2:11:19 PM GMT+8

<span style="color:green">&#x2714;</span> 完成「Solid State Drive」配置

------
> Updated at February 20, 2020 at 3:27:09 PM GMT+8 

反省一下最近都在做些什麼。
首先就是無休無盡的  **『 Support Time 』**。涉及到東西很多，也學到了很多。但是浪費了很多時間。有時候生活就是這樣。在面對<span style='color:rgb(88, 70, 10)'>「Exploitation & Exploration Dilemma」</span>我正如失敗的上個學期一樣選擇了 「Exploration」這往往意味著失去更多。就這樣隨機下去探索我永遠無法達到我的目標。
反正不管怎麼說，先 **List** 出來吧。

- Blog 
  - 因為忍受不了 **Typora**「WYSIWYG」模式的一些奇怪Bug.(已向維護開發者Post相關Issues，至今未得到解決。）所以開始轉向<span style='color:darkblue'>「Visual Studio Code」</span>，但這僅僅是個「作死」的開始。
  - 首先是配置 Vscode Plugins - [Markdown Preview Enhance](https://github.com/shd101wyy/markdown-preview-enhanced).這個東西確實功能非常強大。支持很多擴展語法，後來發現Preview時支持但是Hexo本身的渲染引擎並不支持這些非常<span style='color:coral'>「Awesome」</span>的擴展語法。
  - 然後就是開始更換 Hexo的 **Render**，這東西簡單說就是負責如何將你的 ```Markdown``` 語法轉為 ```Html```.用了網上比較流行的 ```markdown-it-rendered```.安裝好以後就進行測試上下標。諸如 ```Fe~3~O~4~``` Fe~3~O~4~ | ```1^th^``` 1^th^ 等等。然後又覺得插件自帶的CSS樣式太丑。開始客製化Theme，非常邪門的是我在他規定的模板區域內寫入CSS居然沒有反應。最後直接粗暴的Cover掉它自帶的一個Theme才奇效。這一切都沒什麼問題，直到我發現了 some thing really wired。那就是我的CSS在Vscode內嵌預覽下顯示大片大片的灰白。
   <img src="https://boris-bucket-1301199068.cos.ap-shanghai.myqcloud.com/vscode-markdown/20200220161613-{date}.png" alt="20200220161613-{date}.png" style='zoom:33%'/>
   這件蹊蹺的事情令我花了整整兩天在上面。甚至有苟且忍受淺色主題下去的想法，但是因為實在是受不了沒有靈魂的淺色系主題。最後大量閱覽網頁後嘗試著修改 CSS 文首的全局配置，加入```color: #000;``` 強制覆蓋 vscode 提供的參數最終得以解決。最後又對相關的參數進行了設置，以達到Vscode中預覽效果與最終 Git Deploy 一致。「有些極少量區別是由於拓展功能MPE不支持導致的」。
  - 在這之後安裝了```markdown-it-*```「這裡指該係列插件」在這裡又碰見非常棘手的問題。在常規用 ```npm```安裝後，在文檔裡 Usage 寫的是一段 Js 代碼。這讓我著實摸不著頭腦。這一次我查遍了有關詞條，還是還是不知道怎麼用。起初我以為有一個接口Js文件負責總成整個 Render 的插件開閉情況，但我還沒有找到那個文件。後來我發現```npm```之後那個插件是在工作的，只是我沒有設置相應的css，這件事才最終作罢。在那之后我的blog便支持了「container」的用法
  :::info
  诸如此类的 客製化區域，在以後更新計劃時效果更好。
  :::
  - 最後就是昨晚上安裝的「Prism.js」。之前所有代碼高亮都是依靠 『hexo-prism』的插件集成化管理。但是因為這個插件很久沒有維護了，對於 ```<pre>``` 中 class 支持不是很好。乾脆就直接在 [Prism](https://prismjs.com/) 網站上定制了相關的css和js文件，並在ejs中調用。這裡面還出現了關於調用css文件不能cover本地端的 style.css.天知道我打開了多少次Chrome Development Mode.最後還是折騰好了。
- Netflix 
  - 起源是老爹以他的老程序員的作風感染了我，於是自己折騰了一塊1T大小的移動硬盤。（這裡不得不Respect老爹扎實的代碼能力，作為業餘選手且非科班出身真的非常熟練了。對於代碼的封裝性與通用性真的不是我能所力及的。不愧是買軟件的人XD）。對於這塊硬盤最開始拿到的時候還不太滿意，因為有些塵土痕跡，最關鍵是他1w+小時的通電時長。不過還好讀寫量只有3T，還是很耐用的。
  - 某天早上就突然看到電報群裡有人在談論Netflix的事情。然后 <span style='background:yellowgreen'>「 脑 子 一 热 」</span>就上了车。最愚蠢的事情是上車以後發現自己的 ip 並不能看 Netflix 。於是開始一貫的做法。<span style='color:rgb(88, 70, 10)'>「折騰」.</span>先是確定 CN2-GIA-E 是否可以通過換 ip 的方式去解鎖 Netflix 。後來通過購置 [STEAMSV](https://steamsv.com/) 服務進行「DNS解鎖」。這樣一來就可以看 Netflix 了。但是還是有些貴，主要是 Netflix Ipad OS的app中只有 Netflix Origin 劇集集成了中文字幕。然後 Mac 端通過 Chrome 看限制在 720P.最後又跑去 Windows 端折騰 Edge，最後一本滿足的上了4k。
  - 關於 「4k」。當時購入電腦的時候現在看來最值得就是這塊屏幕。Netflix 不愧是「流媒體 Streaming Media」領域的巨頭。優化確實做得沒話說。但是之前不是提到了移動硬盤的事情。這下又開始琢磨怎麼樣將4k下載下來。最後還是衝動消費訂購了某個4k站點的資源，有了torrent種子開始摩拳擦掌準備下載。但是文件的大小還是令我「裂裂裂烈烈開」。最後還是幾經周折放到115網盤上再離線下載。差不多 5M/s 的速度也要動輒下5，6個小時。簡直夢回小學時代。
    >這裡值得一提的是之前依託油猴插件無所不能的「Aria2」 面對 Torrent 文件也無力回天。但還是強烈推薦「Aria2」「多線程<span style='color:darkorange'>爆裂</span>下載程式」.
- 备案
  - 就在前天 终于完成了备案。腾讯云这边备案还是蛮方便的。速度也比我想象中的快多了。印象中就填完资料某天下午午睡接到了确认信息的客服电话，之后没过多久就接到了备案完成的邮件。然后 ssh 上服务器修改了 ```nginx.conf``` 这里还出现了一点小问题，Nginx 又又又又出现了端口占用的情况。我真的自闭，一怒之下```kill -9``` 杀光了所有占用 80 端口的进程，重启 Nginx 服务居然就解决了，实在是不太理解玄学 Nginx。
  - 备案后域名为 `*.boris-tahiti.zone`

写的乱七八糟。大概就是这么多了。以后还是每天列一下自己的 「 To do list 」。毕竟人还是要活的有点仪式感。 
那么下面是最近要做的事情。
:::danger
CA cmu-15-213 Catch Up
:::
:::warning
Re-start Coursera ML
:::
:::info
Latex ShanghaiTech Clubs Rules
:::
明天Update.

[cmu]: http://www.cs.cmu.edu/afs/cs/academic/class/15213-f15/www/schedule.html  "「CMU 15-231-fall 15」"
[ml]: https://www.coursera.org/learn/machine-learning "「 Machine Learning  -Stanford Prof. Andrew Ng」"