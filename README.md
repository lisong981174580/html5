## HTML5标签
> html5实际上html的增量式学习

### 一、学习能力要求
* 了解html基本知识
* 具备css基础
* 熟练使用js
* 耐心、毅力

### 二、发展历程
* 1993年诞生html(1.0)
* 2000年诞生（XHTML1.0）
* 2008年HTML和xhtml合并html5
* 2014html5定稿

### 三、影响
* web增强与垄断
> 如webapp html5增加了离线存储、更丰富的表单、js线程、sosocket、标准扩展embed、css3...
> 流媒体与多媒体引擎 Audio、Video、Canvas 、webgl等等
> 搜索引擎和无障碍领域
 * 移动互联网
 > 跨平台、快速迭代、减低成本、导流入口多、分发效率高
* web改变趋势
> 原生APP转向web app

### 四、准备
> 推荐谷歌浏览器

### 五、标签变化
* DOCTYPE声明

### 六、标签介绍
#### （1）、结构标签
```
 <article></article> 标记定义一篇文章
 <header></header>  页面头部
 <nav></nav>  导航标签
 <section></section> 标记定义一个区域
 <aside></aside> 定义侧边栏
 <hgroup><hgroup> 标记某一块相关元素
 <figure></figure> 多媒体元素
 <figcaption></figcaption> 多媒体元素的标题、或者相关元素的主题
 <footer></footer>底部
 <dialog><dialog>对话标签
 <main></main>页面主要内容

 ```
 #### (2)、多媒体标签

* audio
 ```
  <!--如果不需要转码-->
  <figure  style="display: flex;align-items: center">
      <figcaption style="margin-right: 8px">音乐</figcaption>
      <!--
          src:路径mp3格式等
          autoplay：自动播放
          loop:循环次数  如果是-1那就是无数次
          controls：显示控制器
      -->
      <audio src=""  autoplay="autoplay"   loop="1"  controls="controls">
           如果浏览器不支持则显示是这里的文字
      </audio>
  </figure>

  <!--如果需要转码-->
  <figure  style="display: flex;align-items: center">
      <figcaption style="margin-right: 8px">音乐</figcaption>
      <!--
          src:路径mp3格式等
          autoplay：自动播放
          loop:循环次数  如果是-1那就是无数次
          controls：显示控制器

          type:转码器  首先是audio标签  完了是mpeg转码

      -->
      <audio  autoplay="autoplay"   loop="1"  controls="controls">
          <source src="horse.mp3" type="audio/mpeg">
      </audio>
  </figure>

 ```
 * video 和上面的区别是他存在宽高

```

<!--如果不需要转码-->
<figure  style="display: flex;align-items: center">
    <figcaption style="margin-right: 8px">视屏</figcaption>
    <!--
        src:路径mp3格式等
        autoplay：自动播放
        controls：显示控制器
    -->
    <video src=""   autoplay="autoplay"   controls="controls"  width="200"  height="300">
        如果浏览器不支持则显示是这里的文字
    </video>
</figure>

<!--如果不需要转码-->
<figure  style="display: flex;align-items: center">
    <figcaption style="margin-right: 8px">音乐</figcaption>
    <!--
        src:路径mp3格式等
        autoplay：自动播放
        loop:循环次数  如果是-1那就是无数次
        controls：显示控制器
    -->
    <vidio src=""  autoplay="autoplay"   loop="1"  controls="controls">
        如果浏览器不支持则显示是这里的文字
    </vidio>
</figure>

<!--如果需要转码-->
<figure  style="display: flex;align-items: center">
    <figcaption style="margin-right: 8px">视屏</figcaption>
    <!--
        src:路径mp3格式等
        autoplay：自动播放
        controls：显示控制器

        type:转码器  首先是vidio标签  完了是mp4转码

    -->
    <video  autoplay="autoplay"   controls="controls">
        <source src="horse.mp3" type="vidio/mp4">
    </video>
</figure>

```
* canvas标签
> 标记定义图片
* embed标签
> 引入外部链接，其中最突出的就是引入flash文件时不需要浏览器再去下载flash插件
```
<embed src="../source.swf" type=""  width="1024" height="'1024">

```
#### （3）、状态标签
* meter 表示当前的状态

```
  <meter value="220" min="20" max="380" low="200" high="240" optimum="220"></meter>
  <meter value="0.75"></meter>

 ```
* progress  表示整体进度

```
<progress  value="30" max="100"></progress>

//下面会出现加载中的动画
<progress   max="100"></progress>
```
#### （4）、列表标签
* datalist  灵活的下拉标签
```
 <input placeholder="请选择你喜欢的手机品牌" list="phonelist">
  <datalist id="phonelist">
      <option value="手机1"></option>
      <option value="s手机2"></option>
      <option value="s手机3"></option>
      <option value="a手机4"></option>
      <option value="手机5"></option>
  </datalist>
```
* details 可折叠的列表标签
```
 <details  open="open">
       <summary>详细信息</summary>
       <p>
           这个标签details真好
       </p>
</details>

```

#### （5）、注释标签
* ruby 要注释的字段
* rt 注释符号
* rp 不支持的时候
```
<div>我们来 <ruby>聊 <rp>(</rp><rt> liao </rt> <rp>）</rp></ruby>一个话题</div>
```