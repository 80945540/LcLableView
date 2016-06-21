#LablieView
- 第一次写的开源控件,大家如果有什么更好的意见可以一起参与完善
- 如果使用后有什么新的意见可以联系我
- 邮箱:80945540@qq.com
- [下载APK](http://fir.im/LcLableView)

## 效果图

<img src="/image/image1.png" style="width: 30%;">
<img src="/image/image2.png" style="width: 30%;">
<img src="/image/image3.png" style="width: 30%;">

### 使用说明

导入 lclablelibrary 到项目中

在 build.gradle 的 dependencies 添加:
```
	dependencies {
    compile fileTree(include: ['*.jar'], dir: 'libs')
    ....
    compile project(':lclablelibrary')
    }
```

#### 属性

| Attribute 属性          | Description 描述 |
|:---				     |:---|
| lv_text                | 设置文字内容           |
| lv_text_color         | 设置文字颜色,默认#ffffff       |
| lv_text_size         | 设置文字大小,默认11sp           |
| lv_text_bold         | 设置文字是否支持加粗,默认true    |
| lv_text_all_caps      | 设置文字是否支持全部大写,默认true |
| lv_background_color      | 设置背景颜色,默认"#FF4081" |
| lv_min_size      | 设置LabelView所在矩形最小宽高,默认35dp或50dp |
| lv_padding      | 设置文字上下padding,默认3.5dp |
| lv_gravity      | 设置LabelView方向  |
| lv_fill_triangle      | 设置是否填充三角区域,默认false  |
| lv_fill_size      | 设置是否浮嵌显示大小  |


### 实际使用代码

######使用空边标签时

```
 <FrameLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <View
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@drawable/bag"
        android:orientation="vertical"
        android:gravity="center">
    </View>
    <com.xiaochao.lclablelibrary.LabelView
        android:layout_width="60dp"
        android:layout_height="60dp"
        android:layout_gravity="bottom"
        lv:lv_background_color="#FF6666"
        lv:lv_gravity="BOTTOM_LEFT"
        lv:lv_text="十年经验"
        lv:lv_text_size="8dp"
        />
 </FrameLayout>
```

#####使用浮嵌标签时

要注意容器的android:layout_margin="3dp"必须和lv:lv_fill_size="3"值一样
```
<FrameLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <View
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_margin="3dp"
        android:background="@drawable/bag"
        android:orientation="vertical"
        android:gravity="center">
    </View>
    <com.xiaochao.lclablelibrary.LabelView
        android:layout_width="60dp"
        android:layout_height="60dp"
        lv:lv_background_color="#FF6666"
        lv:lv_gravity="TOP_LEFT"
        lv:lv_text="十年经验"
        lv:lv_text_size="8dp"
        lv:lv_fill_size="3"
        />
</FrameLayout>
```

