## zinglabs-proxy

 研发跳板机，初步用于方便观看连接了阿里云的VPN的机器，端口转发
 
*golang 实现多平台交叉编译：*

### Mac 下编译 Linux 和 Windows 64位可执行程序

```shell
    CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build main.go
    CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build main.go
```
  
### Linux 下编译 Mac 和 Windows 64位可执行程序

```shell
    CGO_ENABLED=0 GOOS=darwin GOARCH=amd64 go build main.go
    CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build main.go
```

### Windows 下编译 Mac 和 Linux 64位可执行程序

```shell
    SET CGO_ENABLED=0
    SET GOOS=darwin
    SET GOARCH=amd64
    go build main.go
```

## 目前的代理：

```
    devEs     = "dev.es"
	devConsul = "dev.consul"
	devKong   = "dev.kong"
	devKonga  = "dev.konga"
	devMinio  = "dev.minio"

	prodEs     = "prod.es"
	prodConsul = "prod.consul"
	prodKong   = "prod.kong"
	prodKonga  = "prod.konga"
	prodMinio  = "prod.minio"

	globElk = "glob.elk"
```

未来想支持：内网代理，命令行模式，可配置的远程列表。