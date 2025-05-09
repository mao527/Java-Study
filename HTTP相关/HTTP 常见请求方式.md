# HTTP 常见请求方式

HTTP 提供多种请求方式，用于客户端与服务器之间的不同交互目的。

##  请求方式列表

| 方法        | 说明                                                         |
| ----------- | ------------------------------------------------------------ |
| **GET**     | 请求获取资源，参数通常在 URL 中，无请求体，**只读不改动数据**。 |
| **POST**    | 向服务器提交数据，用于**创建新资源**，数据在请求体中。       |
| **PUT**     | 提交完整资源，用于**更新资源**（整体覆盖）。                 |
| **PATCH**   | 提交资源的部分字段，用于**局部更新资源**。                   |
| **DELETE**  | 请求删除指定资源。                                           |
| **HEAD**    | 类似 GET，但不返回正文，只获取响应头。                       |
| **OPTIONS** | 查询服务器允许的 HTTP 方法，常用于 CORS 跨域预检。           |
| **TRACE**   | 回显请求内容，用于调试（较少使用）。                         |
| **CONNECT** | 建立隧道连接，主要用于 HTTPS 通信。                          |

---

##  常用方法应用对比

| 场景               | 推荐方法        |
| ------------------ | --------------- |
| 获取网页数据       | `GET`           |
| 提交表单或注册信息 | `POST`          |
| 修改用户信息       | `PUT` / `PATCH` |
| 删除某个资源       | `DELETE`        |
| 验证接口是否存在   | `HEAD`          |

---

##  RESTful API 中的用法建议

- `GET` → 读取数据
- `POST` → 新增数据
- `PUT` / `PATCH` → 修改数据
- `DELETE` → 删除数据