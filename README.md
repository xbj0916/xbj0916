# 通过Github实现URL转发
有时，你注册了一个域名，但是你没有搭建服务器。你希望这个域名能指向你的主页/博客/微博等。但是，很多域名注册商不提供这种服务，或者这是一项收费服务。这时你可以使用GitHub来实现这一功能。

第一步，创建一个空的repo，并把这个repo导入其中。

第二步，在你域名的dns中添加如下的`CNAME`记录:
```
主机名: 按你的需求设置，比如"www"或者“@”
记录值: your_username.github.io.
TTL: 10 分钟
```

如果你不想使用`CNAME`记录，你也可以按如下方式添加`A`记录
```
主机名: 按你的需求设置，比如"www"或者“@”
记录值: 185.199.108.153
       185.199.109.153
       185.199.110.153
       185.199.111.153
TTL: 10 分钟
```

第三步，将[CNAME](./CNAME)文件的内容改为你的域名。

第四步， 在[index.html](./index.html)文件中，将URL改为你希望跳转的地址。

这个repo也有[英文版本](https://github.com/y2l/URL-Redirect/)。