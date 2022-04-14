
 **版本更新说明**

  **1.0.4**  

```
2022-01-09

1、修复日期类型组件在范围选择时回显问题。
2、属性配置中batch组件的属性，判断colWidth是否存在，不存在则填充属性。
3、预览的时候清空原来表单的数据
4、textarea组件去掉可清除的功能，element-ui在此不支持
5、修复添加空数据导致的重复key报错。

```



  **1.0.3**  

```
1、ng-form-build页面中reset方法重置数据后可以保留默认值。
2、日期时间类型的组件宽度适配。
3、修复弹性容器不可新增的问题。
4、axios版本升级。
4、代码优化。

```


  **1.0.2**  

```
1、表单绘制页面样式调整，不再拖着大大的滚动条。
2、日期、时间等组件在默认值输入now，初始化的时候可以替换为当前日期或者时间。
3、修复数字类型组件当默认值为0的时候不回显。
4、代码优化。

```


 **以下为之前的旧项目版本**

  **2.0.14**  

```
1、将vue、element等进行cdn引用，减小体积。
2、发布弹性容器组件，可以针对一整个面板上的组件进行弹性增加、复制、删除。
3、优化部分代码。

```

  **2.0.12**  

```
1、动态表格中外部显示的组件可以自定义每个组件的宽度,不指定则均分。
2、屏蔽默认H5的拖拽，可以在拖拽组件的时候滚动面板。
3、增加日期时间选择组件。
4、对于绘制面板上5个功能按钮增加prop来决定是否显示或者隐藏
5、优化部分代码。

```

  **2.0.9**  

```
1、修复自定义组件预览模式下渲染不正常的问题。
2、优化部分代码。

```

  **2.0.7**  

```
1、要素初始化的时候为当前models初始化值，去掉回调后强制整个表单重置的性能缺陷。
2、对外暴漏VueDragFormItem , 单个组件的渲染组件。
3、优化部分代码。

```

  **2.0.5**  

```
1、属性配置中给表单整体配置页和tabs上增加插槽，具体插槽名称：
extend-tab - tabs的扩展，使用方法：  <template slot="extend-tab" slot-scope="{data }">
                  <el-tab-pane label="扩展属性" name="select">
                    扩展测试插槽-加tab:: {{data}}
                  </el-tab-pane>
                </template>
form-extend-properties - 表单属性扩展配置,使用方法：
     <template slot="form-extend-properties" slot-scope="{ data}">
                    扩展测试插槽
                </template>


```

  **2.0.4**  

```
1、优化部分功能，规避动态回调和赋值当models中key不存在导致绑定数据不生效问题。
2、动态表格添加数据增加方式可配置，目前有： 弹出框和增加行方式（之前只有弹出框）。选择增加行之后，增加一条数据直接在当前table中展示，不再弹出一个弹出框进行添加，方便只有两三个字段的时候修改数据

```

  **2.0.3-beta**  

```
1、增加默认输出隐藏组件值功能（默认打开），关闭后隐藏的组件绑定数据将不输出。
2、增加组件联动功能（针对select、radio、checkbox），如果是静态数据则可以根据绑定的字段进行过滤，如果是远程方法返回的数据则支持根据绑定的字段进行远程重现请求数据，远程请求根据绑定数据带参查询。（此功能测试尚不完善，谨慎使用）

```

  **2.0.2-beta**  

```
1、优化针对动态远程获取数据的时候可以自定义请求头信息。
配置方法：

 <VueDragFormdesign ref="formDesign"  :config="formConfig">


data() {
  return {
    formConfig: {
      httpConfig: (config)=>{
        // 这里自定会议header的请求参数
        config.headers['aaaa'] = 'bbbb'
        return config
      }
    }

  }

}

预览组件中也需要加入: 
 <VueDragFormBuild ref="formbuild"  :config="formConfig"/>

```

  **2.0.1-beta**  

```
1、修改发布样式问题。
2、优化判断默认值方法，规避默认值为false的时候判断为没有默认值


```

  **2.0.0-beta**  

```
1、增加自定义组件，可以通过配置放入加入自定义组件，通过插槽来对自定义组件的属性进行配置。


```

  **1.0.14**  

```
1、修复checkbox、radio、select组件的远程方法调用问题，增加dataPath参数将远程请求的数据通过json的path取值来获取列表。
2、对栅格布局、表格布局、动态表格中点击复制后组件内部的子组件原样复制。
3、修复选择后回调的参数名称，以及静态数据也可以进行选择后回调。
4、选择后回调进行强制刷新，规避偶尔通过值等方式无法触发监听进行渲染页面。
5、对input的show-word-limit 显示条件进行修改，规避某些清空下配置未填写导致显示异常。

```
 