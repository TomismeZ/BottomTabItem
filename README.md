# BottomTabItem

### 介绍
    平常开发的应用中，有很多都是底部导航栏(tabitem)，目前我知道的大体有四种方法实现

    1、LinearLayout中包裹ImageView和TextView（处理起来应该是最麻烦的）

    2、design包中的TabLayout（如果要是添加角标或者其他什么view的时候就变得……）

   `3、一些其他的开源库如`[Android-ViewPagerIndicator][2]`等等（功能很齐全，但是为了这么一个小功能引入这些库，有点小题大做)

    4、则是在我看微博，微信，QQ等应用是看到的自定义控件（这种方式实现最好，但是我在网上没有搜到类似的开源库，可能是太简单的过，没人弄所以自己实现了一个）`

### UI
   ![1](https://github.com/zhangxuyang321/BottomTabItem/blob/master/ui/1.png)

### Gradle
    compile 'com.xyz.tabitem:tabitem:1.0.2'

### 代码
```
    BottmTabItem tab1 = (BottmTabItem) findViewById(R.id.tab1);
    tab1.setSelectState(true);//true 选中状态 false未选中状态

```

### Layout
``` xml
    <com.xyz.tabitem.BottmTabItem
            android:id="@+id/tab1"
            style="@style/bottomitem"
            android:paddingBottom="5dp"
            app:xyzIcon="@mipmap/tab_my"
            app:xyzIconHeight="30dp"
            app:xyzIconWidth="30dp"
            app:xyzSelectIcon="@mipmap/tab_my01"
            app:xyzSelectState="false"
            app:xyzTitle="我的"
            app:xyzTitleSelectColor="#FE7105"
            app:xyzTitleSize="12dp"
            app:xyzTitleTop="5dp" />
```

### 属性介绍
    属性 | 介绍 | 类型 | 默认 | 是否必须
    --- | --- | --- | --- | ---
    xyzSelectState | 是否为选中状态 | boolean | false | 否
    xyzIcon | 默认图片 | reference | null | 是
    xyzSelectIcon | 选中图片 | reference | null | 是
    xyzIconWidth | 图片宽度 | dimension | 0 | 否 
    xyzIconHeight | 图片高度 | dimension | 0 | 否
    xyzTitle | 图片标题 | string | null | 是
    xyzTitleColor | 默认颜色 | color | Color.GRAY | 否
    xyzTitleSelectColor | 选中时颜色 | color | Color.BLACK | 否
    xyzTitleSize | 文字大小 | dimension | 15 | 否
    xyzTitleTop | 图片与文字间距 | dimension | 0 | 否
    
### 注意
    凡是为必须的属性必须有值否则会报错
    
    titleTop 与 PaddingBottom 同时使用时可能会相互影响，调数值就好


### LICENSE 开源协议

    Apache License Version 2.0
    
    
[2]:https://github.com/JakeWharton/ViewPagerIndicator
