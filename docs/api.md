# API Reference

[简体中文](api.zh-CN.md) | [Docs Index](README.md)

This inventory is generated from `go doc -short` for the packages in this repository. It is a quick public-surface map; source files and tests remain the authority for exact semantics.

## Packages

### `gnalloy.org/codec-smtp`

Package name: `smtp`

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
