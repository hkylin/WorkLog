### 7.17
* 早上随便从remedyorder表查了一补单记录，b->c,一直A004导致。
* 修改bizhttpserver，增加协议getsupplieraudstate，bizmanager.dll。o
### 7.18
* 今天开始梳理微众的加签验签流程。
* 中午出现延迟，正好排错语句也错误，select count(*) from md_pay_queue where consume_status!=2，应该用consume_status查，而不是status字段查，日了狗了。
* 但弹性和扩增的克隆机都存在host重复的问题，这会导致resin异常，可以认定今天的延迟是这个原因导致吧。
* 错误的shswp上线导致无法访问加大ngix负载，但奇怪的是影响到了交易这条线，也就是md_pay_queue的记录处理被堆积了，堆积只有一个原因就是mdfrontserver处理慢了。
* 明天整理微众银行文档。
### 7.19
> * 看错文档了，应该只看代收单业务文档即可。
> * 明天整理好接口文档和相关的demo示例以及修改点即可。本周重点完成文档梳理，下周排进度并开发。
> * php可能需要配合修改，php的子进程模式无法使用连接池，可能只能在驱动层去使用连接池才靠谱，操作系统应用层估计没戏。

### 7.20
> * 要么整理开发余婷的需求，要么开发webank验签接口。

### 7.21
> * 微众银行部分demo接口编写和日志整理等。
