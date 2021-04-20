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


3. 你是如何理解 HTML 语义化的
