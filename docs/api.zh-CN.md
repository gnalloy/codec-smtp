# API 参考

[English](api.md) | [文档索引](README.zh-CN.md)

本清单由本仓库 package 的 `go doc -short` 生成，用于快速查看公共面。精确语义以源码和测试为准。

## 包

### `gnalloy.org/codec-smtp`

包名：`smtp`

```text
var ErrInvalidLine = errors.New("gnalloy/codec/smtp: invalid line") ...
type Command string
    const CommandHELO Command = "HELO" ...
type Data struct{ ... }
    func LastData(payload buffer.ByteBuf) Data
    func NewData(payload buffer.ByteBuf) Data
type DataEncoder struct{}
    func NewDataEncoder() *DataEncoder
type Request struct{ ... }
    func NewRequest(command Command, params ...string) Request
type RequestEncoder struct{}
    func NewRequestEncoder() *RequestEncoder
type Response struct{ ... }
    func NewResponse(code int, details ...string) Response
type ResponseDecoder struct{ ... }
    func NewResponseDecoder(maxLineLength int) (*ResponseDecoder, error)
type ResponseEncoder struct{}
    func NewResponseEncoder() *ResponseEncoder
```
