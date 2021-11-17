# galaxy-time

根据经纬度坐标查询天文时间和银河最佳观测时间

## 可用方法

### 查询天文时间
```javascript
SunCalc.getTimes(/*日期*/ date, /*纬度*/ latitude, /*精度*/ longitude)
```

返回一个具有以下属性的对象(每个都是一个“Date”对象):

| 属性        | 描述                                                              |
| --------------- | ------------------------------------------------------------------------ |
| `sunrise`       | 日出(太阳的顶端出现在地平线上)|                                               |
| `sunriseEnd`    | 日出结束(太阳的底部边缘触到地平线)                                            |
| `goldenHourEnd` | 清晨黄金时间(柔和的光线，拍摄的最佳时间)结束了         |
| `solarNoon`     | 太阳正午(太阳在最高点)                              |
| `goldenHour`    | 傍晚黄金时间开始                                               |
| `sunsetStart`   | 日落开始(太阳的底部边缘触到地平线)               |
| `sunset`        | 日落(太阳消失在地平线下，傍晚民用暮色开始) |
| `dusk`          | 黄昏(航海黄昏开始)                                  |
| `nauticalDusk`  | 航海黄昏(天文黄昏开始)                     |
| `night`         | 夜晚开始(足够暗，可以进行天文观测)                 |
| `nadir`         | 最低点(夜晚最黑暗的时刻，太阳在最低的位置)       |
| `nightEnd`      | 夜晚结束(晨光开始)                        |
| `nauticalDawn`  | 航海黎明(航海黎明开始)                         |
| `dawn`          | 黎明(航海黎明结束，民用黎明开始)     |

```javascript
SunCalc.addTime(/*Number*/ angleInDegrees, /*String*/ morningName, /*String*/ eveningName)
```