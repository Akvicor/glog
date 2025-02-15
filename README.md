# glog

自用的golang日志库

[![GoReport](https://goreportcard.com/badge/github.com/Akvicor/glog)](https://goreportcard.com/report/github.com/Akvicor/glog)
[![Gitea Release](https://img.shields.io/gitea/v/release/gomod/glog?gitea_url=https%3A%2F%2Fgithub.com)](https://github.com/Akvicor/glog/releases/latest)
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
[![Go.Dev reference](https://img.shields.io/badge/go.dev-reference-blue?logo=go&logoColor=white)](https://pkg.go.dev/github.com/Akvicor/glog?tab=doc)

```go
import "github.com/Akvicor/glog"
```

# 类型

使用`SetMask(m int)`设置每种消息是否输出

- `Unknown(format string, values ...any)`: 写入`os.Stdout`
- `Debug(format string, values ...any)`: 写入`os.Stdout`
- `Trace(format string, values ...any)`: 写入`os.Stdout`
- `Info(format string, values ...any)`: 写入`os.Stdout`
- `Warning(format string, values ...any)`: 写入`os.Stdout`
- `Error(format string, values ...any)`: 写入`os.Stderr`
- `Fatal(format string, values ...any)`: 写入`os.Stderr`

# 前缀

支持添加时间、类型、调用位置，使用`SetFlag(f int)`设置前缀。

# 文件

支持在显示在控制台的同时写入文件，通过`SetLogFile(path string) error`设置文件，设置后会自动写入此文件。

通过`CloseFile()`关闭文件，关闭后不再写入文件

