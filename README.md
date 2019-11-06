# 小程序物流组件使用方法
### 使用前不需要引用任何组件了
## 
#### wxml示例    EMS.wxml
#### 接收参数   | 格式        | 备注|
##### address   |  object     |收货地址|
##### state     | string  |接口返回的 res.data.StateEx|
##### Traces    |接口返回的参数 res.data.Traces |.reverse()倒序 数组要倒序|
##### title     | item.AcceptStation|如果是接口返回的数据直接赋值不用变|
##### describe  |item.AcceptTime}|如果是接口返回的数据直接赋值不用变|
没写到的不用变

    <j-steps type='dot' direction='column' address="{{options.address}}" state="{{StateEx}}">
      <block wx:for="{{Traces}}">
        <!-- <j-step title="已支付" describe="11:30"></j-step> -->
        <j-step title='{{item.AcceptStation}}' describe='{{aitem.AcceptTime}}' />
      </block>
    </j-steps>
	
#### EMS.json
    {
      "usingComponents": {
        "j-steps":"/package/components/steps/index", //组件的位置 
        "j-step":"/package/components/step/index" //同上
      }
    }
#### 	

## 组件下载
https://github.com/535803710/xiaowo
