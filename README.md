# simple-acme

申请ssl证书简单化

# 使用

单次使用(稳定版)：

```shell
bash <(curl -L https://github.com/tdjnodj/simple-acme/releases/latest/download/simple-acme.sh)
```

最新版:

```shell
bash <(curl https://raw.githubusercontent.com/tdjnodj/simple-acme/main/simple-acme.sh)
```

多次使用(稳定版):

```shell
wget https://github.com/tdjnodj/simple-acme/releases/latest/download/simple-acme.sh && bash simple-acme.sh
```

最新版:

```shell
wget https://raw.githubusercontent.com/tdjnodj/simple-acme/main/simple-acme.sh && bash simple-acme.sh
```


此后运行
```shell
bash simple-acme.sh
```
即可

# 特性

- 自动安装一些依赖（不会耗费太多时间）
- 使用 http 模式申请时，自动检测 80 端口是否占用
- 自动拷贝证书
- 可生成自签证书
- 支持多种网页服务器申请
- 支持ipv6
- 对错误的提示不足
- 界面简洁
- 可申请 ECC 证书
- 可使用 DNS 手动模式申请证书

# 计划

暂时都实现了

# 常见问题

Q: 为什么证书没有自动续签？/为什么手动续签失败？

A: 你需要确保续签的时候80端口占用情况跟申请的时候一样。比如你使用 standalone 模式申请证书，那你续签的时候就不能有 nginx、apache 之类的占用80端口。**所以，建议如果你之后要用网页服务器，那就先安装网页服务器，再使用对应模式申请。**

# Credits

主要代码来源: [taffychan-acme](https://github.com/taffychan/acme)

调用脚本: [acme.sh](https://acme.sh/)

特别感谢: [Let's Encrypt](https://letsencrypt.org/)
