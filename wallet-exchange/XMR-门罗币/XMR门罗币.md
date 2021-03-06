POW为共识机制，区块奖励平稳变化，挖矿难度目标为60秒
## 白皮书：
https://zh.masteringmonero.com/Mastering-Monero-Chinese.pdf

## git
https://github.com/monero-project

## 浏览器
https://xmr.tokenview.com

## 水龙头：
https://monerofaucet.info

## 网络类型
主网、测试网（Testnet）和Stagenet
如果你想使用真实的门罗区块链，请选择主网（默认选项）。测试网和Stagenet是两个独立的网络，供开发者开发和测试新代码。这两个网络中的门罗币没有任何实质价值，也无法转移至主网上。

##开发资料
《精通门罗币》
https://github.com/YinXinCryp/monero_book
wallet-rpc文档
https://web.getmonero.org/resources/developer-guides/wallet-rpc.html
daemon-rpc文档
https://web.getmonero.org/resources/developer-guides/daemon-rpc.html

## 隐私保护技术
环形机密交易（RingCT）隐藏交易金额

环形签名（Ring signatures）通过混淆真实的输出来隐藏发送者身份 

隐蔽地址（Stealth address）隐藏接收者身份 Kovri通过 混淆广播源头和隐藏门罗的网络活动痕迹，来阻止他人通过交易 跟踪到你的物理地址。

环形机密交易：

承诺：当你发送门罗币的时候，你以一种私密的方式来进行“承诺”：你只需透露部分的信息，足以让网络确认交易的正当性即可而不用透露具体的交易金额。一个有效的承诺保证交易无法被伪 造，门罗币无法被双花。 

范围证明：是环形机密交易的另一项重要机制。它确保承诺的值介 于0和特定值时间。这有助于防止发送者承诺一个为负或极高的 值。承诺和范围证明结合起来，确保门罗币的供应真实，不会被伪 造或超发。

## 交易解锁时间
一种特殊的交易，在这种交易中，收件人只能在将来某个日期之后才可以使用资金，这是由发送者设定的。
解锁时间允许您向某人发送一笔交易，而接收者就必须在一定数量的区块之后才能使用该笔资金，或者直到某一时间。

## 引导节点
运行在本地节点上的守护进程必须与其他（远程）节点们同步。虽然没有完全同步，但钱包可能仍然连接到本地节点。因此，钱包无法访问本地节点上尚未同步的区块。
为了允许钱包立即可用，本地节点上的守护进程使用 RPC 请求代理到的引导节点，从而访问丢失的区块。

## 账户的地址关系
账户只是地址的分组，本身并没有地址。
在门罗币中，资金并不真正位于账户或公共地址上。从概念上讲，公用地址是网关或路由机制。资金来自交易未支出的产出。

## 交易所对接方案
方案一：观察钱包+子地址
子地址生成

方案二：paymentid+集成地址
参考：https://www.xmr-zh.com/accepting.html