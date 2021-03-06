##features文件语法:
* '#'为注释符号
* 两个空格定义一层缩进
* '* [ ] yyyy-mm-dd Title' 定义一个新的feature
  * yyyy-mm-dd 理解为这个feature添加的时间
  * Title 是这个feature的简略描述
  * '[ ]'用来定义这个特性的状态，包括
    * '[ ]': new: 没有状态的特性(刚刚提出，没有来得及处理)
    * '[p]': planed: 计划中: 这个特性不错, 觉得可以开发，但是并没有进入开发状态
    * '[d]': developing: 开发中: 正在开发这个特性
    * '[f]': finished: 开发完成: 这个特性已经开发完成
    * '[r]': rejected: 这个特性被拒接，详见stat属性
    * '[?]': debated: 这个特性存在争议，尚未决定其状态
* 第0层缩进定义一个feature
* 第一层缩进定义一个feature的各种
* 为了文字对齐，所有属性使用4字母缩写
* 属性包括可选和必选两种，必选属性必须存在
  * desc: 必选，这个特性的详细描述, 可多行定义
  * tree: 可选，又称为目录(catalogue), 定义一个特性的分类目录
    * 使用"->"来连接父子关系
    * 目录可以和tree: 在同一行，这样的话此特性只属于这个分类目录
    * 或者可以另起一行，加一层缩进，这样的话此特性属于多个分类目录
  * tags: 可选，定义一个特性的所属标签，方便脚本分类整理
    * 使用","(半角字符)隔开
  * stat: 可选，此属性的状态流，格式为"yyyy-mm-dd status comment"
  * disc: 可选，关于此特性的讨论，下面可以有任意子特性，例如:
    * pros: 这个特性的优点
    * cons: 这个特性的缺点
    * comment: 关于这个特性其他的评论

完整的例子, 见feature_demo.txt
