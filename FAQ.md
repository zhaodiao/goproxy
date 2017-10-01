## 常见问题

- GoProxy和GoAgent的关系？
> GoProxy是Phus Lu对GoAgent的重写，设计理念和使用习惯一脉相承。

- 需要重新上传服务端吗?
> 需要，老服务端不兼容。

- GoProxy的原理？
> ![image](https://cloud.githubusercontent.com/assets/195836/4602738/ac950aba-5149-11e4-8976-a2606ba08e05.png)

- 安全性如何 ？
> GoProxy使用[MITM](https://zh.wikipedia.org/zh-cn/%E4%B8%AD%E9%97%B4%E4%BA%BA%E6%94%BB%E5%87%BB)来代理HTTPS请求，其明文暴露给GAE。
> 设置gae.user.json的SSLVerify为true可以抵御网关的MITM。
