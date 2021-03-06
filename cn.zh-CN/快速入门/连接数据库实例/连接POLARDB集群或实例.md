# 连接POLARDB集群或实例 {#concept_n2f_4mq_tdb .concept}

本文介绍如何通过DMS和客户端连接到POLARDB集群或实例。

## 使用DMS登录POLARDB {#section_wxq_bql_v2b .section}

[数据管理](https://account.aliyun.com/login/login.htm?oauth_callback=https%3A%2F%2Fdms-rds.aliyun.com)（Data Management Service，简称DMS）是一种集数据管理、结构管理、访问安全、BI图表、数据趋势、数据轨迹、性能与优化和服务器管理于一体的数据管理服务。支持对关系型数据库（MySQL、SQL Server、PostgreSQL等）和NoSQL数据库（MongoDB、Redis等）的管理，同时还支持Linux服务器管理。

**前提条件**

已创建数据库集群的初始账号或普通账号。具体操作请参见[创建数据库集群的初始账号](https://help.aliyun.com/document_detail/68508.html)。

**操作步骤**

1.  进入集群列表或实例列表，找到目标集群或实例。
2.  单击集群或实例的ID，或者单击**操作**列中的**管理**。
3.  单击页面右上角的**登录数据库**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3019/15347328522084_zh-CN.png)

4.  在数据库登录页面，输入集群的VPC连接串和端口号（以英文冒号隔开），以及初始账号或普通账号的用户名和密码，然后单击**登录**。

    -   如果您从集群详情页跳转到数据库登录界面，系统默认为您填写集群的VPC连接串和端口号。

    -   如果您从实例详情页跳转到数据库登录界面，系统默认为您填写该实例的VPC连接串和端口号。

    关于如何查看连接串和端口号，请参见[查看数据库连接串](https://help.aliyun.com/document_detail/68510.html)。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3019/15347328522085_zh-CN.png)

    **说明：** 

    -   若您希望浏览器记住该账号的密码，可以先勾选**记住密码**，然后再单击**登录**。

    -   若出现以下提示，单击**设置所有实例**或者**设置本实例**，以将DMS服务器的IP段加入到所有实例或当前实例的IP白名单中，否则将无法登录。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3019/15347328522087_zh-CN.png)


## 使用客户端登录POLARDB {#section_pfm_qmq_tdb .section}

您可以使用任何标准的MySQL客户端连接POLARDB集群或实例。本文以MySQL-Front客户端为例。

单击[此处](http://www.mysqlfront.de/)下载MySQL-Front。

**操作步骤**

1.  将要访问POLARDB实例的客户端IP地址加入POLARDB白名单中。关于如何设置白名单，请参见[设置白名单](https://help.aliyun.com/document_detail/68506.html)。
2.  启动MySQL-Front客户端。
3.  在**打开登录信息**窗口，单击**新建**，如下图所示。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3020/15347328522088_zh-CN.png)

4.  输入连接信息：
    -   **名称**：MySQL-Front连接数据库的任务名称。若不填，则默认与Host一致。

    -   **Host**：输入连接串。关于如何查看连接串，请参见[查看实例连接串](cn.zh-CN/快速入门/连接数据库实例/查看数据库连接地址.md)。

        （**注意：**输入的连接串不包括端口号。连接串示例：abc.mysql.polardb.cnsh.rds.aliyuncs.com）

    -   **端口**：连接串后面的4个数字。

    -   **用户**：POLARDB集群的账号名称。

    -   **密码**：POLARDB集群的账号密码。

5.  单击**确定**。
6.  在打开**登录信息**窗口，选中刚才创建的连接，单击**打开**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3020/15347328522090_zh-CN.png)

    若连接信息无误，即可成功连接实例。


