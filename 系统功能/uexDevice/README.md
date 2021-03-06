[TOC]

# 1、简介[![](http://appcan-download.oss-cn-beijing.aliyuncs.com/%E5%85%AC%E6%B5%8B%2Fgf.png)]() 
设备信息插件

## 1.1、说明
 本类封装了设备硬件参数相关信息和硬件状态相关信息。

## 1.2、UI展示
 ![](http://newdocx.appcan.cn/docximg/104339w2015d6d16t.jpg)

## 1.3、开源源码
插件测试用例与源码下载：[点击](http://plugin.appcan.cn/details.html?id=167_index) 插件中心至插件详情页 （插件测试用例与插件源码已经提供）

# 2、API概览

## 2.1、方法

> ### vibrate 开启设备震动

`uexDevice.vibrate(milliseconds)`

**说明:**
开启设备震动，iOS平台中，ipad，ipod不支持震动。

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| milliseconds | Number | 是 | 震动持续时长，单位毫秒 |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
3.0.0+

**示例:**

```
    uexDevice.vibrate(500);
```

> ### cancelVibrate 关闭设备震动

`uexDevice.cancelVibrate()`

**说明:**
关闭设备震动

**参数:**
  无

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
3.0.0+

**示例:**

```
    uexDevice.cancelVibrate();
```

> ### getInfo 获取设备信息

`uexDevice.getInfo(infoID)`

**说明:**

获取设备信息,回调方法[cbGetInfo](#cbGetInfo 获取设备信息的回调方法 "cbGetInfo")

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| infoID | Number | 是 | 设备信息类型，详见[CONSTANT](http://newdocx.appcan.cn/newdocx/docx?type=978_975 "CONSTANT")中设备信息类型。 |

**平台支持:**

Android2.2+
iOS6.0+

**版本支持:**

3.0.0+

**示例:**

```
    uexDevice.getInfo('1');//获取系统版本
```
> ### screenCapture 屏幕截图

`uexDevice.screenCapture(quality)`

**说明:**

获取当前屏幕截图,回调方法[cbScreenCapture](#cbScreenCapture 获取所截图片地址的回调方法 "cbScreenCapture")

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| quality | Number | 是 | 图片压缩质量，取值范围[0,1] 为0时压缩率最大|

**平台支持:**

Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.screenCapture(0.8);//获取屏幕截图
```


> ### setVolume 调整音量 

`uexDevice.setVolume(volume)`

**说明:**

设置系统音量值

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| volume | Number | 是 | 音量大小，取值范围[0,1] 为1时音量为最大 |

**平台支持:**

Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.setVolume(0.5);//设置系统音量
```
> ### getVolume 获取系统音量值

`uexDevice.getVolume()`

**说明:**

获取系统音量值,回调方法[cbGetVolume](#cbGetVolume 获取系统音量的回调方法 "cbGetVolume")


**参数:**

无

**平台支持:**

Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.getVolume();//获取系统音量值
```
> ### setScreenAlwaysBright 屏幕常亮控制 

`uexDevice.setScreenAlwaysBright(data)`

**说明:**

屏幕常亮控制（应用在前台时有效）

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| data | Number | 是 | 屏幕常亮控制值，0 为取消常亮控制；1为设置屏幕常亮|

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.setScreenAlwaysBright(1);//设置屏幕常亮
```

> ### getScreenBrightness 获取屏幕亮度

`uexDevice.getScreenBrightness(brightness)`

**说明:**

获取屏幕亮度值,回调方法[cbGetScreenBrightness](#cbScreenBrightness 获取系统音量的回调方法 "cbGetScreenBrightness")

**参数:**
 
无

**平台支持:**

Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.getScreenBrightness();//获取屏幕亮度
```

> ### setScreenBrightness 调整屏幕亮度

`uexDevice.setScreenBrightness(brightness)`

**说明:**

调整屏幕亮度

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| brightness | Number | 是 | 屏幕亮度值，取值范围[0,1] 为1时屏幕亮度最大 |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.setScreenBrightness(0.5);//设置屏幕亮度
```

> ### openWiFiInterface 打开WIFI设置页

`uexDevice.openWiFiInterface()`

**说明:**

打开WIFI设置页面

**参数:**
 
无

**平台支持:**
Android2.2+
iOS8.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+

**示例:**

```
    uexDevice.openWiFiInterface();//打开WIFI设置页面
```

## 2.2、回调方法

> ### cbGetInfo 获取设备信息的回调方法

`uexDevice.cbGetInfo(opId,dataType,data)`

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| opId | Number | 是 | 操作ID，在此函数中不起作用，可忽略 |
| dataType | Number | 是 | 数据类型，详见[CONSTENT](http://newdocx.appcan.cn/newdocx/docx?type=978_975 "CONSTENT")中Callback方法数据类型 |
| data | String | 是 | 返回设备的相关信息，json格式数据，参数说明详见[CONSTAN](http://newdocx.appcan.cn/newdocx/docx?type=978_975 "CONSTAN")T中设备信息类型 |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
3.0.0+

**示例:**

```
    uexDevice.cbGetInfo=function (opCode,dataType,data){
        alert(data);
    };
```


> ### cbScreenCapture 获取屏幕截图的回调方法

`uexDevice.cbScreenCapture(savePath)`

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| data | String | 是 | 返回屏幕截图本地存储地址 |


**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.cbScreenCapture =function(data){
    	var data = JSON.parse(data);
       alert(data.savePath);
    };
```


> ### cbGetVolume 获取系统音量值的回调方法

`uexDevice.cbGetVolume(data)`

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| data | String | 是 | 系统音量值信息，音量值范围为[0,1] |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+


**示例:**

```
    uexDevice.cbGetVolume=function(data){
    	var data = JSON.parse(data);
       alert(data.volume);
    };
```

> ### cbGetScreenBrightness 获取系统屏幕亮度值的回调方法

`uexDevice.cbGetScreenBrightness(data)`

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| data | String | 是 | 系统屏幕亮度值信息，值范围为[0,1] |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
iOS3.0.4+
Android3.0.1+

**示例:**

```
    uexDevice.cbGetVolume=function(data){
    	var data = JSON.parse(data);
       alert(data.brightness);
    };
```

## 2.3、监听方法

> ### onOrientationChange 屏幕旋转的监听方法

`uexDevice.onOrientationChange(mode)`

**参数:**
 
|  参数名称 | 参数类型  | 是否必选  |  说明 |
| ------------ | ------------ | ------------ | ------------ |
| mode | Number | 是 | 屏幕方向，1-正竖屏；2-左横屏；4-倒竖屏；8-右横屏。 |

**平台支持:**
Android2.2+
iOS6.0+

**版本支持:**
3.0.0+

**示例:** 

```
    uexDevice.onOrientationChange = function(mode){
        if(mode == 1){
            alert("正竖屏");
        }else if(mode == 2){
            alert("左横屏");
        }else if(mode == 4){
            alert("倒竖屏");
        }else if(mode == 8){
            alert("右横屏");
        }
    };
```

# 3、更新历史
API 版本：uexDevice-3.0.4(iOS) uexDevice-3.0.1（Android）
最近更新时间：2015-11-06

|  历史发布版本 | iOS更新  | 安卓更新  |
| ------------ | ------------ | ------------ |
| 3.0.4  |  新增屏幕截图、调节屏幕亮度、调节系统音量、屏幕常亮控制、跳转WIFI界面相关接口 |   |
| 3.0.3  |  设备列表更新 |   |
| 3.0.2  |  支持获取4G网络状态 |   |
| 3.0.1  | 修复在不显示状态栏时无法获取当前网络状态的bug  |新增屏幕截图、调节屏幕亮度、调节系统音量、屏幕常亮控制、跳转WIFI界面相关接口 |
| 3.0.0  | 设备能力功能插件  | 设备能力功能插件|
