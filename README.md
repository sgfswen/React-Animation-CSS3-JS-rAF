
##网页动画介绍 
CSS3：sacle  transform rotate animation transition
JS模拟：$(...).animate()  $(...).show()  setInterval  setTimeout
rAF:(requestAnimationFrame):优化后的setInterval和setTimeout
SVG:animate
canvas:canvas

|名称|优点|缺点|
|---|---|
|CSS3|高性能、易于使用|兼容性差，无法实现复杂效果|
|JS模拟动画|兼容性强|性能差、难以调试|
|rAF动画|兼容性一般、性能较高|将被CSS3替代|
|SVG|高性能、能实现复杂效果|编写难度较大|

##React中CSS3的使用
实例如下：
><ReactCSSTransitionGroup transitionName="example">
>{items}
></ReactCSSTransitionGroup>

当在父组件中加入子组件，则进入.example-enter状态，并且紧接着进入.example-enter.example-enter-active状态，持续0.5s，然后动画效果消失，组件以opacity=1显示：
>.example-enter{
    opacity:0.01;
    transition:opacity .5s ease-in;
}
>.example-enter.example-enter-active{
    opacity:1;
}
当从父组件中删除子组件，则进入.example-leave状态，并且紧接着进入.example-leave.example-leave-active状态，持续0.5s，然后动画效果消失，组件以opacity=0.01显示
>>.example-leave{
    opacity:1;
    transition:opacity .5s ease-in;
}

>>.example-leave.example-leave-active{
    opacity:0.01;
}

注意：使用ReactCSSTransitionGroup插件，可能需要为动画的对象，添加`key`属性

##React中JS的使用
>主要是setTimeout和setInterval

##React中rAF的使用
>rAF=requestAnimationFrame 直译：请求动画帧
>优化过的js模拟动画
>出现背景：由于JS动画使用广泛但是性能差，因此提出rAF标准，用于优化性能
>兼容性差（支持IE10+），用法和js差不多，都是使用`this.state`改变状态"# React-Animation-CSS3-JS-rAF" 
