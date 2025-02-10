# 陌生人聊天软件 API (Stranger Chat API)

一个基于RESTful架构的陌生人社交聊天应用后端API服务。
A RESTful backend API service for a stranger social chat application.

## 功能特性 (Features)

- 用户认证与授权 (User Authentication & Authorization)
  - 短信验证码登录 (SMS verification code login)
  - JWT token认证 (JWT token authentication)
  
- 用户管理 (User Management)
  - 用户注册 (User registration)
  - 用户资料管理 (Profile management)
  - 用户列表获取 (User listing)

- 社交功能 (Social Features)
  - 发布帖子 (Post creation)
  - 帖子互动(点赞、评论、分享) (Post interactions - like, comment, share)
  - 帖子收藏 (Post favorites)
  - 帖子加热系统 (Post warming system)
  
- 通知系统 (Notification System)
  - 互动通知 (Interaction notifications)
  - 状态通知 (Status notifications)
  - 礼物通知 (Gift notifications)
  - 系统公告 (System announcements)

- 文件上传 (File Upload)
  - 支持图片上传 (Image upload support)

## API 文档 (API Documentation)

API遵循OpenAPI 3.0.3规范，详细的接口文档请参考 `openapi.yaml`。

主要接口路径：

- `/sms_verification_codes` - 短信验证码相关
- `/users` - 用户相关
- `/posts` - 帖子相关
- `/upload` - 文件上传
- `/notifications` - 通知相关

## 技术规范 (Technical Specifications)

### 认证 (Authentication)

使用Bearer JWT token进行API认证：

```http
Authorization: Bearer <token>
```

### 请求头要求 (Required Headers)

每个请求需要包含以下头部：

- `User-Agent` - 客户端信息
- `X-Device-ID` - 设备唯一标识
- `X-Request-ID` - 请求唯一标识

### 错误处理 (Error Handling)

API使用标准HTTP状态码指示请求状态，错误响应格式：

```json
{
  "code": "ErrorCode",
  "message": "Error message"
}
```

## 开发环境 (Development Environment)

### 服务器配置 (Server Configuration)

- 主机: 127.0.0.1
- 端口: 8080
- 基础路径: /v1

## 联系方式 (Contact)

- 开发者: 高少祥 (gaosx6991)
- GitHub: https://github.com/gaosx6991
- Email: dev@gaosx.top
