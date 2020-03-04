---
title: 關於搭建Blog的前前後後。
date: 2020-02-06 22:19:33
updated: 2020-02-06 22:19:33
categories: "Odds&Ends 雜談"
---

# <span style='color:purple'>&#9856;</span> &nbsp; 「Blog 架 構」

> 終於結束了。

<escape><!-- more --></escape>

- Blog這個東西本來源起上學期期末開始用Markdown寫筆記。

- 回來最開始就用Hexo+Gitpages的方式搭起來。後來因為GitHub服務器太慢遂廢棄 (其實是因為當時懶得設置Hexo的主題)。

- 後來因為 *2019-nCov* 的原因待在家中。熱血沸騰就搞了Tencent的服務器。搭Wordpress。因為服務器直接裝的Centos+Wordpress鏡像。相當方便地建站了。但因為Wordpress比較臃腫（其實是沒有Active的文檔blog幫助等等不會修改

- 最後決定回歸Hexo

  - 用Git的Hook實現Git-Centos上傳再用Nginx完成自動化部署。

  - 但這中間因為對ssh概念Nginx功能ip端口亂七八糟的知識不熟悉。折騰了相當長時間。這簡直是我繼剛接觸代碼時CS100給我帶來的絕望之後最大絕望…

    > 这部分主要是有三个问题
    >
    > 1. 腾讯云安全组虽然Default是开放所有端口，但在我设置完开放Port：443/80(常用端口)後，Nginx就可以正常工作了（IP地址顯示 “*Welcome to Nginx！* ）。
    >
    > 2. 關於Nginx 「 Address already in use」這個問題，我最開始檢查了所有端口占用情況，發現存在Nginx master進程自己占用自己的情況。最後一直沒有解決這個問題。但是發現并不影响Nginx工作。這裡請注意[Stackoverflow: Nginx will not start (Address already in use)](https://stackoverflow.com/questions/14972792/nginx-nginx-emerg-bind-to-80-failed-98-address-already-in-use) 此解決方案問題描述是沒有任何進程占用Port ：80 。所以我認為並不適用。By the way , all methods which requires to kill the process may not solve this problem since unless `pkill -f nginx`  can kill the pid, which actually Nginx itself, other command may not work. You can use `grep -r listen /etc/nginx/*` to check which process has occupied the Port : 80.
    >
    > 3. 關於Git-Hook的問題。在按照網上教程執行完建立「裸倉 --bare」及設置好Hexo相關文件真正放置的位置後 **一定一定要確認涉及到Hook操作的文件的用戶組權限 `Git:Git`** 可以使用 `ll`去檢查所屬。
    >
    > 4. 接著上面的繼續，在設置 **ssh** 連接時要注意服務器默認的登錄方式，可以在`\etc\ssh\sshd.conf` 中修改。注意ssh粘貼公钥`.pub` 文件時「Vim」下非插入模式粘貼會少一個字符。用`git@xx.xx.xx.xxx(Your ip)` 去檢查時候可以以「git」用戶身份登錄服務器。
    >
    > 5. 最後Hexo方面的部署就不贅述了。如果出現問題先檢查服務器 「git」用戶`~/xx.git` 下Hexo文件是否成功上傳，如果沒有請檢查 「ssh」設置是否正確。如果「git」成功上傳但實際存放Hexo文件的地方為空請檢查「Hook」文件是否正確。
    >
    > 6. 如果以上兩者都ok。可以退回去檢查「Nginx」。我這裡是重新啟動了 防火墻并开放了Port：80
    >
    >    ```bash
    >    systemctl stop firewalld
    >    systemctl mask firewalld
    >    yum install iptables-services
    >    systemctl enable iptables
    >    iptables -A INPUT -p tcp -m state --state NEW -m tcp --dport 80 -j ACCEPT
    >    service iptables save
    >    service iptables restart
    >    ```
    >
    >    最后就可以正常使用了。「這裡不太確定是否是這個因素引起的，但是之前排查『Nginx』時也有人Mention到了這個問題。」

    

  - 最後還聯系了theme的作者並嘗試Repo自己寫的（亂抄的 .ejs文件 實現Category功能。

    

    

總的來說，整個過程雖然非常「Suffering」 但還是有很多幫助…
（起碼知道怎麽退出Vim了 （x

就這樣。

