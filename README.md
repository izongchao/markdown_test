### 请求地址
```url
/product/category/lists
```
### 返回说明
###### 正确情况下的返回JSON数据包结果如下
```json
{
    "error": null,
    "result": [
        {
            "ID": 144,
            "ShopID": 56,
            "ShopAreaID": 1,
            "ShopTypeID": 13,
            "Name": "水果",
            "Number": 1,
            "ShowSW": 1,
            "DayShow": 0,
            "DaySW": 0,
            "TimeSW": 0,
            "TimeShow": "",
            "UID": 43,
            "IsShow": 1,
            "CreateTime": "2017-07-18 13:59:31",
            "DayShowList": []
        }
    ]
}
```
###### 错误情况下的返回JSON数据包结果如下
```json
{
    "error": {
        "errorcode": "3",
        "message": "该店铺暂无商品分类"
    },
    "result": null
}
```
|参数     | 描述                              |
|:--------|:----------------------------------|
|error    | 是否有错误，不是null表示没有错误  |
|errorcode| 错误码                            |
|message  | 错误信息                          |
|result   |返回结果,有时候有有时无，看具体结果|

