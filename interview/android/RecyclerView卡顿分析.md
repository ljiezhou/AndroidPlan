RecyclerView卡顿的原因  
1.onBindViewHolder中进行了耗时操作。如加载图片。  
2.onCreateViewHolder重复设置背景，布局过深。  
3.没有固定高度。  
4.没有正确使用notifyDataSetChanged，notifyItemRangeInserted等函数。  

RecyclerView的卡顿，大都是以上几个原因导致的。而分析时间到底花在哪里了，就需要用到TraceView了。这里只做简单的说明，详细内容[参考这里](https://www.jianshu.com/p/7e9ca2c73c97)。  
TraceView都能看到那些成分？  
TraceView 是 Android SDK 中内置的一个工具，它可以加载 trace 文件，用图形的形式展示代码的执行时间、次数及调用栈，便于我们分析。  


