# HTTP 请求报文与响应报文

## 一、HTTP 请求报文（Request）

HTTP 请求由客户端发送给服务器，格式如下：

### 1. 报文结构

```
请求行（http版本、状态码和状态消息）
请求头部（Headers）
空行
请求体（Body，可选）
```

### 2. 示例

```
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html
```

### 3. 常见请求头字段

| 字段名            | 说明                                    |
| ----------------- | --------------------------------------- |
| `Host`            | 请求的主机名和端口                      |
| `User-Agent`      | 客户端软件信息                          |
| `Accept`          | 接受的数据类型                          |
| `Accept-Encoding` | 支持的压缩格式（如 gzip）               |
| `Content-Type`    | 请求体内容的类型（如 application/json） |
| `Content-Length`  | 请求体的长度                            |
| `Authorization`   | 认证信息                                |
| `Cookie`          | 客户端保存的 cookie 数据                |

---

## 二、HTTP 响应报文（Response）

HTTP 响应由服务器返回给客户端，格式如下：

### 1. 报文结构

```
状态行
响应头部（Headers）
空行
响应体（Body）
```

### 2. 示例

```
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1256
Set-Cookie: sessionId=abc123

<html>...</html>
```

### 3. 常见响应头字段

| 字段名                        | 说明                          |
| ----------------------------- | ----------------------------- |
| `Content-Type`                | 响应体的内容类型              |
| `Content-Length`              | 响应体长度                    |
| `Set-Cookie`                  | 设置 cookie 到客户端          |
| `Cache-Control`               | 缓存策略                      |
| `Location`                    | 重定向地址（用于 3xx 状态码） |
| `Server`                      | 服务器软件信息                |
| `Access-Control-Allow-Origin` | CORS 允许的跨域请求来源       |
