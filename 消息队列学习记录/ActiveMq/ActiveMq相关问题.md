# ActiveMq相关问题

## 启动和配置

#### 1.activemq.bat启动报错：

![](D:\files\消息队列学习记录\ActiveMq\image-20200615175144808.png)

##### 解决方案：

conf/avtivemq.xml配置文件中找到<transportConnector name="amqp" uri="amqp://0.0.0.0:5672?maximumConnections=1000&amp;wireFormat.maxFrameSize=104857600"/>这一行，直接将其中的端口号改掉(改成一个生疏的端口，楼主改成6111)。改完之后，到activemq.bat的根目录下的cmd中运行./activemq start命令。

