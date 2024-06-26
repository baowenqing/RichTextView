Android 富文本支持表格，数学公式，图片，点击扩展 （原生和WebView两种模式）
## 使用方法
```


原生调用：
1.RichHtml.init(applicationContext)


2.<com.example.tablerichtext.table.HtmlTextView
            android:id="@+id/htmlTextView"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:padding="20dp"
            android:background="@color/white"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintLeft_toLeftOf="parent"
            app:layout_constraintRight_toRightOf="parent"
            app:layout_constraintTop_toTopOf="parent" />
            
            
 3.this.findViewById<HtmlTextView>(com.example.tablerichtext.R.id.htmlTextView)
 .setHtml(App.getSample(), HtmlCompat.FROM_HTML_MODE_LEGACY, null, null)   
 
 
H5调用：
   <com.example.tablerichtext.mathweb.MathView
        android:id="@+id/math_view"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        >
    </com.example.tablerichtext.mathweb.MathView>
    
this.findViewById<MathView>(R.id.math_view)
            .setDisplayText(App.getSample())        

```

## 主页
![RichText](/image/Home.jpg)


## WebView支持数学公式
![RichText](/image/WebViewMath.jpg)

## 原生支持标签 Supported HTML tags

### Tags supported by android.text.Html
- `<p>`
- `<div>`
- `<br>`
- `<b>`
- `<i>`
- `<strong>`
- `<em>`
- `<u>`
- `<tt>`
- `<dfn>`
- `<sub>`
- `<sup>`
- `<blockquote>`
- `<cite>`
- `<big>`
- `<small>`
- `<font color="..." face="...">`
- `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
- `<a href="...">`
- `< img src="...">`

### Extended support by html-text
- `<table>`
- `<ul>`
- `<ol>`
- `<li>`
- `<code>`
- `<center>`
- `<strike>`
- `<div>`[HTML contains two newline, there is one]
- `<font size="..." color="...">`[extend support size]
- `< img src="..." width="..." height="...">`[extend support width, height]


![RichText](/image/NativeMath.png)

```
<h2>Hello world</h2>
<p>
    <font
            size='6'
            color='#FF0000'>Font size
    </font>
</p>
<ul>
    <li><a href="https://github.com/wangchenyan">只是一个链接 A 标签</a>, welcome to star or fork,
        if you have issues, please tell me.
    </li>
</ul>
<br />
<ol>
    <li>first</li>
    <li>second
        <ol>
            <li>second - first
                <br />
                newline
            </li>
        </ol>
    </li>
</ol>
<br />
<h2>图片</h2>
<img
        width="200"
        height="200"
        src="https://cdn.pixabay.com/photo/2022/02/12/19/58/cat-7009836_1280.jpg">
<br />
<br />
<h2>数学函数</h2>
<p>已知函数 $$f ( x,y ) = x^{ 2 } + 2 y^{ 2 } + 2 xy + x + y+ 2 xy + x $$，则</p>
<br />
<h2>表格</h2>
<table>
    <tr>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">茶叶
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">水果
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">糕点
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">调味品
        </td>
    </tr>
    <tr>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">美佳
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">×
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
    </tr>
    <tr>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">新月
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">√
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
    </tr>
    <tr>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">海奇
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">√
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">√
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\"></td>
    </tr>
</table>


<table
        class=\"MsoNormalTable\"
        border=\"1\"
        cellspacing=\"0\"
        cellpadding=\"0\"
        style=\"margin-left:23.05pt;border-collapse:collapse;border:none\">
    \n
    <tr>
        <td
                width=\"339\"
                valign=\"top\"
                style=\"width:254.6pt;border:solid
                #231F20
                1.0pt;\r\n
                border-left:none;background:#DCDDDE;padding:0cm
                0cm
                0cm
                0cm;height:25.5pt\"><p
            class=\"TableParagraph\"
            align=\"center\"
            style=\"margin-top:6.95pt;margin-right:\r\n
            3.95pt;margin-bottom:0cm;margin-left:4.6pt;margin-bottom:.0001pt;text-align:\r\n
            center\">
        <span style=\"font-size:10.5pt;color:black\">账务处理</span>
        </p> </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">项目
        </td>
        <td
                colSpan=\"1\"
                rowSpan=\"1\">账务处理
        </td>
    </tr>
</table>

<p
        class=\"MsoBodyText\"
        style=\"margin-top:0cm;margin-right:120.65pt;margin-bottom:\r\n0cm;margin-left:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;\r\ncolor:black\">因自然灾害毁损设备时的账务处理为：（单位：万元） 设备转入清理：</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black;letter-spacing:.25pt\">借：固定资产清理 140</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">累计折旧</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">60</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">贷：固定资产</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">200</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">支付清理费用：</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">借：固定资产清理</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">5</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">贷：银行存款</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">5</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">收回设备的价款：</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">借：银行存款</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">100</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">贷：固定资产清理</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">100</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">结转设备发生的净损失：</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">借：营业外支出</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">45</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">贷：固定资产清理</span>
    <span
            lang=\"EN-US\"
            style=\"font-size:10.5pt;color:black\"></span>
    <span style=\"font-size:10.5pt;color:black\">45</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin-top:0cm;margin-right:112.55pt;margin-bottom:\r\n0cm;margin-left:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;\r\ncolor:black\">该公司因自然灾害毁损设备对当期损益的影响金额为－ 45 万元。故选 C。</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:#4F81BD\">【小鱼讲】</span>
</p>
<p
        class=\"MsoBodyText\"
        style=\"margin:0cm;margin-bottom:.0001pt\">
    <span style=\"font-size:10.5pt;color:black\">本题考查的是固定资产的处置，考生在做题时一定要看清题目要求，不同情况下净损益的处理不同。</span>
</p>
<table
        class=\"MsoNormalTable\"
        border=\"1\"
        cellspacing=\"0\"
        cellpadding=\"0\"
        style=\"margin-left:23.05pt;border-collapse:collapse;border:none\">\n
    <tbody>\n
        <tr>\n<td
                width=\"188\"
                valign=\"top\"
                style=\"width:141.1pt;border:solid
                #231F20
                1.0pt;\r\n
                background:#DCDDDE;padding:0cm
                0cm
                0cm
                0cm;height:25.5pt\"><p
                class=\"TableParagraph\"
                align=\"center\"
                style=\"margin-top:6.95pt;margin-right:\r\n
                60.0pt;margin-bottom:0cm;margin-left:60.6pt;margin-bottom:.0001pt;text-align:\r\n
                center\">
            <span style=\"font-size:10.5pt;color:black\">项目</span>
            </p> </td> \n<td
                    width=\"339\"
                    valign=\"top\"
                    style=\"width:254.6pt;border:solid
                    #231F20
                    1.0pt;\r\n
                    border-left:none;background:#DCDDDE;padding:0cm
                    0cm
                    0cm
                    0cm;height:25.5pt\"><p
                    class=\"TableParagraph\"
                    align=\"center\"
                    style=\"margin-top:6.95pt;margin-right:\r\n
                    3.95pt;margin-bottom:0cm;margin-left:4.6pt;margin-bottom:.0001pt;text-align:\r\n
                    center\">
            <span style=\"font-size:10.5pt;color:black\">账务处理</span>
            </p> </td> \n
        </tr>
        \n
        <tr>\n<td
                width=\"188\"
                valign=\"top\"
                style=\"width:141.1pt;border:solid
                #231F20
                1.0pt;\r\n
                border-top:none;padding:0cm
                0cm
                0cm
                0cm;height:79.5pt\">
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\"> </span>
            </p>
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\"> </span>
            </p>
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm;margin-right:19.1pt;margin-bottom:\r\n
                    0cm;margin-left:52.15pt;margin-bottom:.0001pt;text-indent:-32.3pt;line-height:\r\n
                    155%\">
            <span style=\"font-size:10.5pt;line-height:155%;color:black\">属于生产经营期间正常的处置损益</span>
            </p> </td> \n<td
                    width=\"339\"
                    valign=\"top\"
                    style=\"width:254.6pt;border-top:none;border-left:\r\n
                    none;border-bottom:solid
                    #231F20
                    1.0pt;border-right:solid
                    #231F20
                    1.0pt;\r\n
                    padding:0cm
                    0cm
                    0cm
                    0cm;height:79.5pt\"><p
                    class=\"TableParagraph\"
                    style=\"margin-top:6.95pt;margin-right:175.95pt;\r\n
                    margin-bottom:0cm;margin-left:4.2pt;margin-bottom:.0001pt;line-height:155%\">
            <span style=\"font-size:10.5pt;line-height:155%;color:black\">产生清理净损失：</span>
            </p> <p
                    class=\"TableParagraph\"
                    style=\"margin-top:6.95pt;margin-right:175.95pt;\r\n
                    margin-bottom:0cm;margin-left:4.2pt;margin-bottom:.0001pt;line-height:155%\">
            <span style=\"font-size:10.5pt;line-height:155%;color:black\">借：资产处置损益</span>
            </p> <p
                    class=\"TableParagraph\"
                    style=\"margin-top:.05pt;margin-right:136.75pt;\r\n
                    margin-bottom:0cm;margin-left:4.6pt;margin-bottom:.0001pt;text-align:justify;\r\n
                    text-justify:inter-ideograph\">
            <span style=\"font-size:10.5pt;color:black\">贷：固定资产清理</span>
            </p> <p
                    class=\"TableParagraph\"
                    align=\"center\"
                    style=\"margin-top:6.45pt;margin-right:\r\n
                    139.45pt;margin-bottom:0cm;margin-left:4.6pt;margin-bottom:.0001pt;\r\n
                    text-align:center\">
            <span style=\"font-size:10.5pt;color:black\">产生净收益，则做相反分录</span>
            </p> </td> \n
        </tr>
        \n
        <tr>\n<td
                width=\"188\"
                valign=\"top\"
                style=\"width:141.1pt;border:solid
                #231F20
                1.0pt;\r\n
                border-top:none;padding:0cm
                0cm
                0cm
                0cm;height:79.5pt\">
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\"> </span>
            </p>
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\"> </span>
            </p>
            <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm;margin-right:9.9pt;margin-bottom:\r\n
                    0cm;margin-left:56.75pt;margin-bottom:.0001pt;text-indent:-46.15pt;\r\n
                    line-height:155%\">
            <span style=\"font-size:10.5pt;line-height:155%;color:black\">自然灾害等非正常原因形成的净损益</span>
            </p> </td> \n<td
                    width=\"339\"
                    valign=\"top\"
                    style=\"width:254.6pt;border-top:none;border-left:\r\n
                    none;border-bottom:solid
                    #231F20
                    1.0pt;border-right:solid
                    #231F20
                    1.0pt;\r\n
                    padding:0cm
                    0cm
                    0cm
                    0cm;height:79.5pt\"><p
                    class=\"TableParagraph\"
                    style=\"margin-top:6.95pt;margin-right:0cm;margin-bottom:\r\n
                    0cm;margin-left:4.2pt;margin-bottom:.0001pt\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\">产生清理净损失：</span></p> <p
                    class=\"TableParagraph\"
                    style=\"margin-top:6.5pt;margin-right:130.45pt;\r\n
                    margin-bottom:0cm;margin-left:24.0pt;margin-bottom:.0001pt;text-indent:-19.8pt;\r\n
                    line-height:155%\">
            <span style=\"font-size:10.5pt;line-height:155%;color:black\">借：营业外支出——非常损失贷：固定资产清理
            </span>
            </p> <p
                    class=\"TableParagraph\"
                    style=\"margin-top:0cm;margin-right:0cm;margin-bottom:\r\n
                    0cm;margin-left:4.2pt;margin-bottom:.0001pt\"><span
                    style=\"font-size:10.5pt;\r\n
                    color:black\">若产生清理净收益，则贷记营业外收入</span></p> </td> \n
        </tr>
        \n
    </tbody>
    \n
</table>

<p></p>
<p>
    With billions of Android devices around the world, Android has surpassed our wildest
    expectations. Today at Google I/O, we showcased a number of ways we’re pushing
    Android forward, with the
    <a href="https://developer.android.com/preview/index.html">O Release</a>, new
    tools for developers to help create more performant apps, and an early preview of a
    project we call Android Go -- a new experience that we’re building for entry-level
    devices.
</p>
```


