## Eugene Goostman 程式真的通過了圖靈測試嗎？ (作者：陳鍾誠)

### 前言

2014 年 6 月 9 日，我看到 inside 網站中有人發布了一個訊息 [「電腦首度通過圖靈測試(36kr.com)」](http://share.inside.com.tw/posts/5079)。 我的直覺反應是，這件事情勢必有假，於是一路追了下去。

Inside 的訊息其實是轉貼自 36氪這個來自中國的網站， 36氪網站的文章標是 [「计算机首次通过图灵测试」](http://www.36kr.com/p/212680.html) 。

不仔細看文章的人，很可能會被誤導，認為電腦已經可以成功得欺騙人類，讓人以為他是一個真人，而且比率達到和真人一樣的水準，也就是「人類已經無法正確區分文字交談的對象到底是電腦還是人類了」。

但是、這樣的想法是錯的，文章中所說的 Eugene Goostman 這個軟體其實並沒有達到「完全能欺騙人類」的水準，因為他們所說的圖靈測試，和我所認知的圖靈測試，根本就是不同的東西。

### 圖靈測試是甚麼？

36氪文章中所說的 [「图灵测试」](http://baike.baidu.com/view/94296.htm) ，其實有連結到百度百科。百度百科裏對圖靈測試的描述如下：

> 图灵测试是测试人在与被测试者(一个人和一台机器)隔开的情况下，通过一些装置（如键盘）向被测试者随意提问。问过一些问题后，如果被测试者超过30%的答复不能使测试人确认出哪个是人、哪个是机器的回答，那么这台机器就通过了测试，并被认为具有人类智能。

但是、我所認知的圖靈測試，並不是採用 30% 誤判率為基準的，而是應該達到「和人類被誤判為電腦」一樣的水準。換句話說，假如程式偽裝的和真人一樣好的話，那麼應該要符合下列的表格要求。

判斷者的決定    交談對象為人類                    交談對象為電腦
--------------  -----------------------------     -------------------------------------
判斷為人        比率為 P   (正確判斷)             比率大於或等於為 P (欺騙成功)
判斷為電腦      比率為 1-P (誤判人為電腦)         比率小於或等於為 1-P (欺騙失敗)

因此、對於上述新聞中所說的，[「计算机首次通过图灵测试」](http://www.36kr.com/p/212680.html) 這件事情，其實是採用 30% 的欺騙成功率，這是我們認為該宣稱有問題的關鍵原因。

### 測試單位的英文公告

36氪的 [「计算机首次通过图灵测试」](http://www.36kr.com/p/212680.html) 一文中指出了訊息來源為「英國雷丁大學的新聞稿」，網址如下：

* <http://www.reading.ac.uk/news-and-events/releases/PR583836.aspx>

該新聞稿提到 Eugene Goostman 這個程式通過圖靈測試的語句如下：

> The 65 year-old iconic Turing Test was passed for the very first time by supercomputer Eugene Goostman during Turing Test 2014 held at the renowned Royal Society in London on Saturday.

但新聞稿的後面有寫出測試方法的描述：

1. Simultaneous tests as specified by Alan Turing
2. Each judge was involved in five parallel tests - so 10 conversations
3. 30 judges took part
4. In total 300 conversations
5. In each five minutes a judge was communicating with both a human and a machine
6. Each of the five machines took part in 30 tests
7. To ensure accuracy of results, Test was independently adjudicated by Professor John Barnden, University of Birmingham, formerly head of British AI Society

我對這個測試方法的解讀如下：

1. 圖靈測試：電腦程式是否能成功的透過文字交談欺騙人類，偽裝自己是個人。
2. 每個「判斷者」都會分別判斷五組「人+電腦」的配對，也就是總共進行 10 次的對話。
3. 總共有 30 位判斷者參與。
4. 總共有 30*10=300 場的交談。
5. 在五分鐘內，「判斷者」會與一組「人和機器」分別交談。
6. 五組「電腦程式」都會與 30 位「判斷者」談過一次。
7. 為了確認「判斷者」判斷結果為正確或錯誤， John Barnden 教授會監控並確認結果。

### 我的感想

我認為「英國雷丁大學發布的新聞稿」用詞有欠妥當，主要是因為下列語句實在是太過強烈：

> The 65 year-old iconic Turing Test was passed for the very first time by supercomputer Eugene Goostman during Turing Test 2014 held at the renowned Royal Society in London on Saturday.

雖然新聞稿後面有交代 Eugene Goostman 程式成功的欺騙過 33% 的判斷者，但是沒有看完全文的人還是很容易被誤導的。

> If a computer is mistaken for a human more than 30% of the time during a series of five minute keyboard conversations it passes the test. No computer has ever achieved this, until now. Eugene managed to convince 33% of the human judges (30 judges took part - see more details below) that it was human.

而 36氪網站直接把 [「计算机首次通过图灵测试」](http://www.36kr.com/p/212680.html) 拿來當標題，則是進一步的誤導了大家， 雖然 36氪有超連結指向 [百度的圖靈測試定義](http://baike.baidu.com/view/94296.htm)  ，但是這個定義顯然與一般人的認知不同，應該要強調一下才對，不應該企圖用聳動性的標題吸引目光。

最後、 inside 的轉載 [「電腦首度通過圖靈測試(36kr.com)」](http://share.inside.com.tw/posts/5079) 這篇，雖然有指出來源的 36氪網站文章，不過我想轉貼的人或許沒有仔細想過到底文章中的「通過圖靈測試」到底是甚麼意義，也沒想過這樣可能會誤導讀者，造成錯誤科學訊息的傳播問題。

從這個案例中，我們可以看到在網路訊息發達的今天，要能夠不被誤導，恐怕必須要有很強的判斷力與追根究柢的精神，但是在這個訊息多如牛毛的世界中，錯誤與聳動的訊息往往傳播的特別快，這恐怕是網路世界亟待解決的問題之一啊！

最後、我上 [g0v 的新聞小幫手](http://newshelper.g0v.tw/) 去檢舉了這個新聞，希望能讓誤導的情況稍微降低一下！


