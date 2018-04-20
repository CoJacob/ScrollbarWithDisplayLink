# ScrollbarWithDisplayLink (Use Objective-C)
A iOS scrollBarWithDisplayLink 
(一个评论滚动的小组件,已解决CADisplayLink引起的内存泄漏问题)

Used

   1. init (初始化)
   - (GScrollBar *)scrollBar {
   if (!_scrollBar) {
   _scrollBar = [[GScrollBar alloc] initWithFrame:CGRectMake(15, 77,CGRectGetWidth(self.view.bounds)-60, 28)];
   }
   return _scrollBar;
   }
  
  2. SetUpData  (配置数据)
 self.scrollBar.contents = @[@"说初八之后会大瀑布的都是失去独立思考的…",@"今天的演唱会很好看",@"明天是晴天",@"一起去野炊"];
 self.scrollBar.images   = @[[UIImage imageNamed:@"wscn_default"],
 [UIImage imageNamed:@"wscn_user"],
 [UIImage imageNamed:@"wscn_default"],
 [UIImage imageNamed:@"wscn_user"]];
 
   3. Use (使用)
      [self.scrollBar startAutoScroll];


  4. Preview (预览)
  
       ![image](https://github.com/Winerywine/ScrollbarWithDisplayLink/blob/master/ScrollBar_record.gif)
