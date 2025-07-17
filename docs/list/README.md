# 接口列表

| 接口名称 (API Name) | 描述 (Description) | 调用方法 (Method) | URL 路径 (Endpoint) | 返回数据 (Response Example) |
| :------------------ | :----------------- | :---------------- | :------------------ | :-------------------------- |
| **用户信息查询** | 获取指定用户的基本信息。 | `GET` | `/api/v1/users/{id}` | ```json { "id": "123", "name": "张三", "email": "zhangsan@example.com" } ``` |
| **订单创建** | 创建一个新的订单记录。 | `POST` | `/api/v1/orders` | ```json { "orderId": "ORD-20250619-001", "status": "pending" } ``` |
| **商品列表** | 获取所有可售商品的信息。 | `GET` | `/api/v1/products` | ```json [ { "productId": "P001", "name": "极速API套餐", "price": 99.00 }, { "productId": "P002", "name": "高级数据接口", "price": 199.00 } ] ``` |
| **短信发送** | 发送验证码或通知短信。 | `POST` | `/api/v1/sms/send` | ```json { "success": true, "message": "短信已发送" } ``` |
| **天气查询** | 查询指定城市的天气信息。 | `GET` | `/api/v1/weather/{city}` | ```json { "city": "北京", "temp": "25°C", "condition": "晴" } ``` |

