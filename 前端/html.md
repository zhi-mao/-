# HTML

1. DTD 的作用是什么？什么是怪异模式？什么是标准模式？二者有什么差别（举例）？产生的历史原因是什么？使用时需要注意什么？
    - DTD即Document Type Definition（文档类型定义），是一套关于XML标记符的语法规则，也是用来验证XML文件格式的验证机制，是XML的一部分；
    - 在早期网络中，页面通常有两种版本，一种是为网景（Netscape）的Navigator准备的版本，以及为微软（Microsoft）的Internet Explorer准备的版本。当W3C创立网络标准后，为了不破坏当时既有的网站，因此，浏览器采用了两种模式，用以把能符合新规范的网站和老旧网站区分开；
    - 在怪异模式(Quirks mode)下，排版会模拟Navigator4 和 Internet Explorer5的非标准行为，在标准模式(Standards mode)下，行为即由HTML与CSS的规范描述的行为
    - 浏览器根据HTML文件开头的DOCTYPE来决定使用哪种模式，HTML5通常使用&#60;!DOCTYPE html&#62;

2. HTML5 是什么？有哪些新特性？新增了哪些语义化标签？新增了哪些表单元素？和 H5 有啥关系？
    - HTML5是构建web内容的一种语言描述方式，是互联网的下一代标准，是构建以及呈现互联网内容的一种语言方式；
    - 语义化标签、增强型表单、视频和音频、Canvas绘图、SVG绘图、地理定位、拖放API、WebWorker、WebStorage、WebSocket
    - 语义化标签
      标签 | 描述
      :-:|:-:
      &#60;header&#62;|定义了文档的头部区域
      &#60;footer&#62;|定义了文档的尾部区域
      &#60;nav&#62;|定义文档的导航
      &#60;section&#62;|定义文档中的节
      &#60;article&#62;|定义文章
      &#60;aside&#62;|定义页面以外的内容
      &#60;details&#62;|定义用户可以看到或隐藏的细节
      &#60;summary&#62;|标签包含details的标题
      &#60;dialog&#62;|定义对话框
      &#60;figure&#62;|定义自包含内容，如图表
      &#60;main&#62;|定义文档主内容
      &#60;mark&#62;|定义带有记号的文本
      &#60;time&#62;|定义日期/时间
    - 增强型表单
      - html5修改一些新的input输入特性，改善更好的输入控制和验证
        输入类型 | 描述
        :-:|:-:
        color | 主要用于选取颜色
        date | 选取日期
        datetime | 选取日期(UTC时间)
        datetime-local | 选取日期（无时区）
        month | 选择一个月份
        week | 选择周和年
        time | 选择一个时间
        email | 包含e-mail地址的输入域
        number | 数值的输入域
        url | url地址的输入域
        tel | 定义输入电话号码和字段
        search | 用于搜索域
        range | 一个范围内数字值的输入域
    - 新增了5个表单元素
      标签 | 描述
      :-: | :-:
      &#60;datalist&#62; | 用户会在输入数据时看到预定义选项的下拉列表
      &#60;progress&#62; | 进度条，展示连接、下载进度
      &#60;meter&#62; | 刻度值，用于某些计量，如温度、重量等
      &#60;keygen&#62; | 提供一种验证用户的可靠方法，生成一个公钥和私钥
      &#60;output&#62; | 用于不同类型的输出
    - 新增表单属性
      属性 | 描述
      :-:|:-:
      placeholder | 输入框默认提示文字
      required | 要求输入的内容是否可为空
      pattern | 描述一个正则表达式验证输入的值
      min/max | 设置元素最小/最大值
      step | 为输入域规定合法的数字间隔
      height/width | 用于image类型&#60;input&#62;标签图像高度/宽度
      autofocus | 规定在页面加载时，域自动获得焦点
      multiple | 规定&#60;input&#62;元素中可选择多个值
    - 和h5关系
      html5是web开发的HTML规范，h5可以说是移动端的ppt

3. 你是如何理解 HTML 语义化的
    - 在没有css的情况下，页面也能呈现出很好的页面结构
    - 增强用户体验
    - 有利于SEO
    - 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）

4. meta viewport是做什么用的？怎么写？
    - meta标签可以提供有关页面的元信息
    - 使用meta viewport可以很方便的在不同屏幕尺寸的手机上对内容和布局进行控制
    - ```
      <meta name="viewport" content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">	
      ```
    - device-width是设备最理想的viewport宽度，user-scalable是指是否允许用户手动缩放页面initial-scale指初始化缩放比例

5. HTML和XHTML有什么区别？
    - XHTML 元素必须被正确地嵌套。
    - XHTML 元素必须被关闭。
    - XHTML 标签名必须用小写字母。
    - XHTML 文档必须拥有根元素。

6. 使用data-*属性有什么用
    - 可以嵌入自定义数据，使用dataset或getAttribute获取值

7. &#60;script&#62;、&#60;script async&#62;&#60;script defer&#62;的区别
    - 直接使用script的话，HTML会按照顺序来加载并执行脚本，会阻塞dom渲染
    - async会异步执行
    - defer会在页面加载完毕后执行

8. 白屏和FOUC是什么？为什么通常推荐将CSS &#60;link&#62;放置在&#60;head&#62;&#60;/head&#62;之间，而将JS &#60;script&#62;放置在&#60;/body&#62;之前？有没有例外的情况？
    - Chrome浏览器的加载机制会出现白屏情况，在所有css文件加载完毕之前，会显示白屏
    - Firefox浏览器的加载机制会出现FOUC现象，每加载一个css文件，页面的样式都会发生变化
    - 将link放在head之间可以让页面逐步渲染，避免呈现给用户没有样式的内容
    - 将script放在body尾部不会阻塞页面渲染

9. 浏览器渲染机制？什么是回流（reflow）？什么是重绘（repaint）？
    - https://zhuanlan.zhihu.com/p/163013732
    - 回流是某个位置的布局发生了变化，浏览器会重新从根部开始计算该节点的布局
    - 重绘是只改变页面元素的颜色、字体等不影响布局的属性

10. 什么属性能让浏览器直接使用ES6 Module？
    - &#60;script type="module"/&#62;
