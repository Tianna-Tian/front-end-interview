# 了解交换机、路由器、网关的概念，并知道各自的用途

### 交换机

> **在计算机网络系统中，交换机是针对共享工作模式的弱点而推出的。交换机拥有一条高带宽的背部总线和内部交换矩阵。交换机的所有的端口都挂接在这条背部总线上，当控制电路收到数据包以后，处理端口会查找内存中的地址对照表以确定`目的MAC`（网卡的硬件地址）的`NIC（网卡）`挂接在哪个端口上，通过内部 交换矩阵迅速将数据包传送到目的端口。目的MAC若不存在，交换机才广播到所有的端口，接收端口回应后交换机会“学习”新的地址，并把它添加入内部地址表中。**

> **交换机工作于`OSI`参考模型的第二层，即数据链路层。交换机内部的`CPU`会在每个端口成功连接时，通过`ARP`协议学习它的`MAC`地址，保存成一张 `ARP`表。在今后的通讯中，发往该`MAC`地址的数据包将仅送往其对应的端口，而不是所有的端口。因此，交换机可用于划分数据链路层广播，即冲突域；但它不 能划分网络层广播，即广播域。**

> **交换机被广泛应用于二层网络交换，俗称“`二层交换机`”。**

> **交换机的种类有：`二层交换机`、`三层交换机`、`四层交换机`、`七层交换机`分别工作在`OSI`七层模型中的第二层、第三层、第四层盒第七层，并因此而得名。**

### 路由器

> **`路由器（Router）`是一种计算机网络设备，提供了路由与转送两种重要机制，可以决定数据包从来源端到目的端所经过 的路由路径（host到host之间的传输路径），这个过程称为路由；将路由器输入端的数据包移送至适当的路由器输出端(在路由器内部进行)，这称为转 送。**

> **路由工作在OSI模型的第三层——即网络层，例如网际协议。**

> **路由器的一个作用是连通不同的网络，另一个作用是选择信息传送的线路。 路由器与交换器的差别，路由器是属于OSI第三层的产品，交换器是OSI第二层的产品(这里特指二层交换机)。**

### 网关

> **`网关（Gateway）`，网关顾名思义就是连接两个网络的设备，区别于路由器（由于历史的原因，许多有关TCP/IP 的文献曾经把网络层使用的路由器（Router）称为网关，在今天很多局域网采用都是路由来接入网络，因此现在通常指的网关就是路由器的IP），经常在家 庭中或者小型企业网络中使用，用于连接局域网和Internet。 网关也经常指把一种协议转成另一种协议的设备，比如语音网关。**

> **在传统`TCP/IP`术语中，网络设备只分成两种，一种为`网关（gateway）`，另一种为`主机（host）`。网关能在网络间转递数据包，但主机不能 转送数据包。在主机（又称终端系统，end system）中，数据包需经过TCP/IP四层协议处理，但是在网关（又称中介系 统，intermediate system）只需要到达网际层（Internet layer），决定路径之后就可以转送。在当时，`网关 （gateway）`与`路由器（router）`还没有区别。**

> **在现代网络术语中，`网关（gateway）`与`路由器（router）`的定义不同。`网关（gateway）`能在不同协议间移动数据，而`路由器（router）`是在不同网络间移动数据，相当于传统所说的`IP网关`（IP gateway）。**

> **网关是连接两个网络的设备，对于语音网关来说，他可以连接PSTN网络和以太网，这就相当于VOIP，把不同电话中的模拟信号通过网关而转换成数字信号，而且加入协议再去传输。在到了接收端的时候再通过网关还原成模拟的电话信号，最后才能在电话机上听到。**

> **对于以太网中的网关只能转发三层以上数据包，这一点和路由是一样的。而不同的是网关中并没有路由表，他只能按照预先设定的不同网段来进行转发。网关最重要的一点就是端口映射，子网内用户在外网看来只是外网的IP地址对应着不同的端口，这样看来就会保护子网内的用户。**

**参考资料：**

[题目来源](https://www.nowcoder.com/ta/review-network/review?page=11)
