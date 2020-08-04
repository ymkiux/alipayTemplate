# 支付标准sdk_demo
入坑支付宝支付

导入支付宝sdk aar库

> 根据官网文档aar导入 日志显示找不到当前aar库
>
> 问题思路:既然项目找不到 就直接把它当作maven库导入
>
问题方法:

- 点击【File>New>New Module】选择 【Import .JAR/.AAR Package

- 点击【Next】输入.arr文件所在路径并点击【finish】

- 点击【File>Project Settings 】(或者使用快捷键[Ctrl+Shift+Alt+S]（适用于Windows）)

- 在左侧菜单【Modules】栏目下，选择需要依赖.aar包的module（通常为app）.点击Dependencies分页点击右上角绿色的【+】选择【Module Dependency】选择你导入的ARR所在的【Module】

> 即可正常使用aar内的接口函数

使用支付宝开放平台

> 创建应用-签约app支付-通过开放平台助手生成对应的密钥
>

#### 基本使用

demo修改参数

- ```
  APPID					
  ```

- ```
  RSA2_PRIVATE	密钥
  ```

- ```
  PID	联系客服个人信息处可看
  ```

> 这样就实现了最基本的支付demo

#### 进阶使用

基本使用的三大参数

> 可通过云端返回的json字符串解析并赋值

请求参数

> 可以过OrderInfoUtil2_0这个类里面的buildOrderParamMap方法
>
> 调用支付活动使用buildOrderParamMap方法，可在其添加变量请求参数 total_amount 【价格】和subject【订单信息】