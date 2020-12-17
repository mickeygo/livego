<p align='center'>
    <img src='./logo.png' width='200px' height='80px'/>
</p>

[livego](./README_2.md)

简单高效的直播服务器：
- 说明：该项目由 [livego 0.0.13](https://github.com/gwuhaolin/livego.git) fork 而来。

项目目录结构：
```bash
--/
  -- cmd
    -- api
  -- av
  -- configure
  -- container
    -- flv
    -- ts
  -- parser
    -- aac
    -- h264
    -- mp3
  -- protocol
    -- amf
    -- hls
    -- httpflv
    -- rtmp
  -- utils
    -- pio
    -- pool
    -- queue
    -- uid
- main.go
- livego.yaml
```

### 0.14 修改内容

#### 新增
1. 针对 HTTP-FLV 协议，指定一系列端口供外部调用（在内网中不需要使用反向代理；Chrome 浏览器 HTTP 协议针对同域请求，最大连接限制数量为 6）。

#### 调整
1. 新增 cmd 目录；
2. 原 protocol/api 目录移至 cmd/api 目录;
