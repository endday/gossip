# Gossip 1.0 使用教程

这里会花10到20分钟，教大家用 Gossip 从0到1完成一个简单的 PPT 案例。涉及 Gossip 使用技巧的方方面面，让你从此开启制作幻灯片的新方式。该教程可以在 Gossip 的导航中的 `案例 -> 教程` 查看。

现在点击导航栏中的 `新建` 按钮新建一个新文件，结果如图所示。

![WX20200326-131219@2x.png](https://i.loli.net/2020/03/26/liqbw6uzcRYVCfU.png)

我们先大概看看 Gossip 的界面。Gossip 主要是由7个面板构成：

- `想法面板`：添加、删除、编辑想法。
- `大纲面板`：编辑幻灯片的大纲。
- `缩略图`：所有幻灯片的缩略图。
- `幻灯片面板`：预览每一页幻灯片。
- `元素面板`：当前选中幻灯片所包含的元素。
- `样式面板`：当前选中元素的样式。
- `变量面板`：添加、删除、编辑变量。

其中右上角有关闭按钮的面板都是可以折叠的。

## 确定主题

做 PPT 的第一步就是确定演讲的主题了，我选择了一个比较简单和有趣的主题，就是如何实现下面的效果：当你的鼠标移动上去的时候，会出现类似蛇一样残影的效果。

![Mar-25-2020 11-03-29.gif](https://i.loli.net/2020/03/25/MGnariKg3pD5QEL.gif)

## 收集想法

和写文章一样，当确定了主题之后，我们也不太清楚到底要讲些什么：头脑中只有一些零散的想法。比如现在我的想法有这些：

- 这个作品的效果可以取名为“笔走龙蛇”。
- 演讲者的名字必不可少。
- 需要添加一些代码片段的图片。
- 这个作品的核心就是对数组进行移动。
  
对于传统的软件，也许需要额外的地方存储我的这些想法，但是在 Gossip 中却不需要。在最下面的**想法面板**中点击 ➕ 添加两段文字和三张图片。

然后分别修改两段文字的内容如下：

- `MiniPear`
- `这个作品的核心就是对数组进行移动。`

之后分别修改三张图片的网络地址如下：

- `https://i.loli.net/2020/03/25/n9bS6mrRslZXfaO.png`
- `https://i.loli.net/2020/03/25/JkL9fUu3d5NHRmA.png`
- `https://i.loli.net/2020/03/25/tO6SfaoYnJdRksq.png`

目前**想法面板**就会变成下面这个样子，这样想法就收集完成了。

![QQ20200325-114903@2x.png](https://i.loli.net/2020/03/25/lJH2Ms4yURdXfAO.png)

## 构建约定式大纲

随着想法收集得越来越多，演讲的思路也越来越清晰，最后行文逻辑梳理成了下面的这段大纲：

- 笔走龙蛇
  - 大体思路
  - 效果演示
  - 代码讲解
    - 获得画布
    - 监听事件
    - 移动数组
  
同样我也不用借助其他思维导图软件来梳理思路，可以直接在 Gossip 的左边的**大纲面板**直接构建大纲。使用方式也很简单：当鼠标移动到大纲上的每一个节点的时候，会出现两个 ➕ ，点击分别会创建低一级别和相同级别的节点，如下图所示。

![Mar-25-2020 11-32-09.gif](https://i.loli.net/2020/03/25/qKI9gO6MSkP4mR1.gif)

接下来大家就可以按照上面说的，对大纲进行构建了，结果如下图所示。细心的同学可能发现，当前大纲和预期不太一样，有以下几个错误：

- “效果演示”和“代码讲解”并应该是并列关系，但现在却变成了父子关系。
- “获得画布”和“监听事件”顺序反了。

![QQ20200325-113637@2x.png](https://i.loli.net/2020/03/25/AK1SlXcirgskOBa.png)

难道需要重新构建大纲？完全不用，**只需要简单地拖拽就可以调整大纲的结构**，如下图所示。

![Mar-25-2020 11-44-35.gif](https://i.loli.net/2020/03/25/sMLyE1chvbtkOgf.gif)

接下来简单解释一下“约定式”的意思：“我们来做一个约定，你负责编辑大纲，Gossip 帮你创建和调整幻灯片”。现在点击**大纲面板**右上角的切换按钮，会进入**缩略图面板**，你会发现大纲中的每一个节点都有一张幻灯片所对应！

![QQ20200325-113926@2x.png](https://i.loli.net/2020/03/25/9HfxmeoXCrquEAl.png)

就在即将准备进行下一阶段的创作的时候，我突然想把“效果展示”调整到最后，也就是希望大纲如下。

- 笔走龙蛇
  - 大体思路
  - 代码讲解
    - 获得画布
    - 监听事件
    - 移动数组
  - 效果演示

在不移动“效果演示”的位置的前提下，是不是意味着要分别移动“代码讲解”、“获得画布”、 “监听事件”、“移动数组”所对应的幻灯片？当然不是，简单将“代码讲解”拖拽到“效果演示”的后面，并且进入**缩略图面板**，你会发现这4张幻灯片的顺序都发生了变化！

## 制作每一张幻灯片

当确定了大纲之后，就需要对每一张幻灯片进行设计了。这个阶段的任务是添加一些视觉元素（文字、图片等），并且对它们进行布局和样式的调整。**这部分和传统的软件有极大的区别，有一定的学习成本，希望大家仔细阅读**。

目前 Gossip 只是支持四种元素组成：`容器`、`文字`、`图片`、和 `画布`。一个元素是由**内容**和**样式**构成的，比如一段文字的内容就是它的文本，样式就是字体大小、颜色这些。

对于每一个元素，在**预览面板**中：

- 鼠标点击，如果当前元素没有被选中，会选择该元素。
- 鼠标点击，如果当前元素被选中，那么进入编辑模式。
- 鼠标移走，如果当前元素在编就模式，就会退出编辑模式。

### （1）笔走龙蛇

每一页幻灯片都是一个**容器：容器里面可以添加容器、文字、图片和画布**。容器主要用于元素的布局，容器中两个属性值得注意：

- 排列方式：指定容器中元素排列的方式，有竖直和水平两种方式。
- 比例：指定容器中元素占据的比例。

比如第一张幻灯片就是一个**竖直的容器**，里面有两个元素：两段文字。

下面把放在**想法面板**里面的一段文字：“MiniPear” 直接拖进“伟大的创造者”所在的区域，会发现“MiniPear”直接替代了“伟大的创造者”！**这里不仅仅支持文字替换，也支持图片替换，后面会用到。**

![gifhome_640x453.gif](https://i.loli.net/2020/03/25/O7kbtqWIoLhaXRn.gif)

目前第一张幻灯片就制作完成了。

### （2）大体思路

现在开始制作第二张幻灯片。

第一步在**样式**面板将两段文字设置成水平居中和竖直居中。

![gifhome_640x367.gif](https://i.loli.net/2020/03/25/jSCKAMhvs31VXZz.gif)

第二步在**结构面板**点击**竖直的容器**，并且在**样式面板**将它的排列**排列方式**从**竖直**变成**水平**，之后再调整**比例**，最后将之前准备好的文字从**想法面板**拖入。

![gifhome_640x367 _1_.gif](https://i.loli.net/2020/03/25/Vyop18hnNsXgzB2.gif)

### （3）代码讲解

接下来我们开始制作第三章幻灯片。

首先我们将下面这段文字复制进入下面的**文字**。

```plain text
- 获得画布
- 监听事件
- 移动数组
```

这时你会发现每一行开头的 **-** 变成了 **•** ，这是 Gossip 目前对**无序列表**进行简单的支持。
  
接下来希望在文字左边添加一张图片，将鼠标移动到**元素面板**的**获得画布...**节点。这时它下面会出现一个 ➕ ，点击该加号，并且选择图片，这时幻灯片中就会出现一张图片。

但是现在图片和文字是竖直排列的，在**结构面板**找到包含这段文字和图片的**容器**，将其**排列方式改**成**水平**即可。这之后修改一下**比例**，然后调整一下文字的**对齐方式**。

同时修改图片的网络地址为：`https://i.loli.net/2020/03/25/etBq4Gmg5ikdUsa.png`

![Mar-25-2020 14-44-23.gif](https://i.loli.net/2020/03/25/o8ZhqSsXtELrPQT.gif)

现在如果希望**文字**调整到**图片**的右边，有两种方法：

- 在**结构面板**将**图片**拖动到**文字**的前面，幻灯片中的两者也会改变位置。
- 在**幻灯片**里面直接拖动**图片**，并且将它移动到**文字**里面，两者的位置会进行交换。

![Mar-25-2020 14-49-31.gif](https://i.loli.net/2020/03/25/6TMJwlsur9m14h3.gif)

这里对**图片元素**进行一点简单的说明，图片有两种上传方法：

- 本地图片：直接上传本地图片。
- 网络图片：需要提交图片网络链接。

### （4）获得画布/监听事件/移动数组

接下来开始制作“获得画布”、“监听事件”和“移动数组”三张幻灯片。这里会涉及到**变量的概念，这也是和传统软件有很大区别的地方，有一定的学习成本。**

这三张幻灯片因为是并列的观点，所以我希望它们的标题的颜色是一样的：红色。

首先我在**变量面板**创建一个类型为**颜色**的变量，并且将它名字改为`代码标题颜色`，同时设置为红色。

![Mar-25-2020 14-56-24.gif](https://i.loli.net/2020/03/25/MN9KixCY6tInvyH.gif)

准备工作做好之后，选择“获得画布”的标题，并且将这个变量直接拖进**样式面板**中的**字体颜色**，将该变量和该元素的该属性进行**绑定**，
这时可以发现**获得画布**这几个字已经从**黑色**变成了**红色**。

接下来分别将**代码颜色变量**拖进“监听事件”和“移动数组”的标题的**字体颜色**，这时发现它们的标题颜色也都从**黑色**变成了**红色**。

![gifhome_640x298.gif](https://i.loli.net/2020/03/25/zlA4GPkpEsnZyU9.gif)

这时发现红色看上去太耀眼了，希望将它们设置成蓝色。难道需要对三个标题的颜色都进行修改？当然不用，直接修改和它们字体颜色绑定的变量值即可！在**变量面板**找到**代码标题颜色**，修改它的值为蓝色。

![Mar-25-2020 15-35-57.gif](https://i.loli.net/2020/03/25/4vfsKdClADeOGbZ.gif)

这时会发现三张幻灯片的颜色都从红色变成了蓝色！这就是变量基本使用方法，**主要用于快速调整拥有相同属性的元素的样式。**

目前变量只有两种类型：`color` 和 `number`。创建一个变量后，首先可以修改名字（“字体大小”，“字体颜色”），然后可以通过拖动将其和选择的元素（文字、容器...）的样式绑定。

和变量绑定的样式后面会有一个**眼睛**和**垃圾桶**。在这个状态下，样式的值**不能直接改变**，需要修改与其绑定变量的值。点击**眼睛**会高亮该样式绑定的**变量**，点击**垃圾桶**会解除变量和该样式的绑定，这时可以直接修改该样式的值，同时修变量的值将不会影响该样式的值。

在**变量面板**已经预设了一些变量，大家可以自行修改。

现在将“获得画布”中的**文字**删除，在第二个**竖直容器**中插入一张图片，然后将**想法面板**中**第一张代码片段图片**直接拖入该图片，这之后调整一下字体的**对齐方式**。对剩下两张幻灯片重复上诉操作，注意拖入不同代码片段所对应的图片。

![gifhome_640x369.gif](https://i.loli.net/2020/03/25/Ng4CSw3Vu97vZJH.gif)

现在对**想法面板**进行一下说明：

- 将**想法面板**里面的内容拖入幻灯片之后，该**想法**不会被删除，删除需要手动删除。
- 将幻灯片里的元素删除之后，会将其包含的**非容器元素**添加进入**想法面板**，比如刚才删除的**两段文字**。当然如果**想法面板**里面有的元素进不会被添加，所以刚才虽然删除了两段文字，但是最后只保存了一段。

![WX20200325-154926@2x.png](https://i.loli.net/2020/03/25/EQWhbCwKtLVMNqG.png)
  
### （5）效果演示

现在来制作最后一张幻灯片：效果演示，**这里也是 Gossip 和普通幻灯片软件不同的地方，它可以赋予幻灯片生命**。

现在将**文字**删除，然后在**竖直容器**中的添加一个**画布**，点击画布进入编辑模式，并且将下面这段代码复制进去，点击保存。

```js
function draw(canvas, ctx, width, height) {
  function background(color) {
    ctx.fillStyle = color;
    ctx.fillRect(0, 0, width, height);
  }

  let mouseX = width / 2;
  let mouseY = height / 2;
  const size = width / 10;
  const cnt = 50;
  const circleArr = [];
  for (let i = 0; i < cnt; i++) {
    circleArr.push({
      x: mouseX,
      y: mouseX
    });
  }

  function update() {
    for (let i = 0; i < cnt - 1; i++) {
      circleArr[i].x = circleArr[i + 1].x;
      circleArr[i].y = circleArr[i + 1].y;
    }

    circleArr[cnt - 1].x = mouseX;
    circleArr[cnt - 1].y = mouseY;

    background("black");
    circleArr.forEach((item, index) => {
      const c = 255 - (cnt - index);
      ctx.fillStyle = `rgb(${c},${c},${c})`;
      ctx.beginPath();
      ctx.arc(item.x, item.y, index, 0, 2 * Math.PI);
      ctx.fill();
    });
  }

  canvas.onmousemove = e => {
    mouseX = e.offsetX;
    mouseY = e.offsetY;
  };

  const timer = setInterval(update, 30);
  return timer;
}
```

现在鼠标在画布上移动，就会出现和[这个网页]()相同的效果！这样你在给别人展示一些很酷的东西的时候，就不需要重新打开一个网页，一切都是一体的。

![gifhome_640x345.gif](https://i.loli.net/2020/03/25/XL264x7iFgWfQ9J.gif)

当然目前只支持 Canvas，后面会增加对 Svg 的支持，并且支持 Processing 和 P5.js 等。

## 保存/下载/上传

下面 PPT 就制作完成了，下一步当然是保存幸苦劳动的成果了。当前 Gossip 没有云存储能力，但是提供两种保存方式。

- **保存**：这种方式会把文件保存进入浏览器的本地存储。该方式很方便，并且当你访问 Gossip 的时候，会自动从浏览器本地存储读入文件。但有两个问题需要注意：
  - 浏览器的本地存储能力是有限的，不能存储太大的文件。所以较大的本地图片，建议先存储到[图床](https://zhuanlan.zhihu.com/p/35270383)上，然后上传图片链接。
  - 只能存储一份 PPT ，也就是说当你点击保存的时候会覆盖之前的文件。
  - Safari 浏览器需要在隐私中打开**阻止 Cookies**。
- **下载**：这种方式会下载得到一个后缀为 **.gsp** 的文件，当你需要这个文件的时候，直接点击上传按钮即可。这种方式较上一种方式麻烦一点，但是没有上面的限制。

**当前版本的 Gossip 没有撤销功能，所以使用的时候要小心一点，完成一张幻灯片就点击一下保存！！！**

## 演示

在制作好 PPT 之后，就是演示 PPT 了。

### 切换动画

点击幻灯片、按下空格以及方向键都能用来切换幻灯片。Gossip 的切换动画看上去很酷，但并不是华而不实，它能反映前后两张幻灯片的关系。

- 缩小：从大的观点进入小的观点。
- 旋转：并列的观点。
- 放大：从小的观点进入大的观点。

现在大纲如下：

- 笔走龙蛇
  - 大体思路
  - 代码讲解
    - 获得画布
    - 监听事件
    - 移动数组
  - 效果演示

从“笔走龙蛇”到“大体思路”就是缩小效果，从“大体思路”到“代码讲解”就是旋转效果，从“移动数组”到“效果演示”就是放大效果。

### 词云模式

**词云模式也是 Gossip 相对于普通幻灯片软件与众不同的地方**，提供一种一眼了解该 PPT 所有关键信息的模式，在演示过程中按下 `backspace` 进入**词云模式** 。

![WX20200325-160152@2x.png](https://i.loli.net/2020/03/25/ZdXp4xcMPLW7slF.png)

在大纲中层级越高的幻灯片会越大。目前大纲如下：

- 笔走龙蛇
  - 大体思路
  - 代码讲解
    - 获得画布
    - 监听事件
    - 移动数组
  - 效果演示

那么“笔走龙蛇”所对应的幻灯片是最大的，“大体思路”、“代码讲解”和“效果演示”其次，“获得画布”、“监听事件”、“移动数组”最小。

这样用户可以一眼看出演讲者想表达的故事最重要的部分，不需要一张张幻灯片地搜索。

同时，在演讲结束后往往会有一个提问环节，这时提问者会让演讲者不断滚动缩略图，从而找到想要提问的幻灯片。但是 Gossip 就不存在这个问题：在词云模式下，提问者可以直接一眼找到自己有问题的幻灯片，然后演讲者点击该幻灯片，该幻灯片会自动放大。效果如下。

![8jsIn1.gif](https://s1.ax1x.com/2020/03/25/8jsIn1.gif)

## API

这里介绍一下画布使用时候的 API。每一个画布的内容应该是一个回调函数，该函数的四个参数分别是：

- canvas 对象
- context 对象
- canvas 的 width 属性：会随着容器大小的变化而变化。
- canvas 的 height 属性：会随着容器的大小的变化而变化。

下面这个例子是在画布中间画一个边长为 100 的正方形。

```js
function(canvas, context, width, height){
  const size = 100,
    x = (width - size ) / 2 ,
    y = (height - size ) / 2;
  context.fillStyle = "#000000";
  context.fillRect(x, y, size, size);
}
```

目前动画方式只支持 `setInterval`，不支持 `requestAnimationFrame`。同时在回调函数中需要将 `timer` 返回，这样在组件销毁的时候会调用 `clearInterval(timer)` 清除该计时器。

使用方法如下。

```js
function(canvas, context, width, height){
  const animation = () => {
    // animation code here
  }
  const timer = setInterval(animation, 30)
  return timer;
}
```

## 总结

当然**笔走龙蛇**这个案例的教程就到此结束了，总一下 Gossip 的一些有特点的功能：

- `想法`：快速找到想讲的内容。
- `大纲`：高效确定演讲的逻辑结构。
- `布局`：更少拖拽和对齐的布局。
- `变量`：方便的调整拥有相同属性的元素的样式。
- `切换动画`：演示过程中提供上下文信息。
- `词云模式`：对 PPT 进行可视化。

当然只是一个比较简单的案例，每一页幻灯片都比较简单。了解复杂的案例可以看 Gossip 的介绍 PPT，该 PPT 可以在 Gossip 的导航中的`案例 -> 介绍`查看。
