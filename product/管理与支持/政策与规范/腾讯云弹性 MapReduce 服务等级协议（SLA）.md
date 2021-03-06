## 第一条 腾讯云弹性 MapReduce 服务
腾讯云弹性 MapReduce 服务是云上托管 Hadoop 集群服务。底层的存储与计算资源依赖于 CVM 与 COS，在此之上，为您提供 Hadoop 中各软件的安装、监控、运维等服务。目前支持的 Hadoop 软件包括但不限于：flink、ganglia、hadoop、hbase、hive、hue、oozie、presto、spark_hadoop2.7、sqoop、storm、tez、zookeeper。

腾讯云弹性 MapReduce 为企业及开发者提供了低成本的云上大数据处理方案，能够满足其大数据分析处理及应用服务。具体服务类别以腾讯云公开发布的相关服务信息为准。

## 第二条 服务保证指标
腾讯云为您所购买的服务制定服务等级指标，并向您承诺提供数据管理和业务质量方面最大程度的保障。同时，腾讯云有权根据变化适时对部分指标做出调整。若无特殊约定，本条款中的“月”均指 30 个自然日，按开通时间起算。

#### 1. 数据存储的持久性
若您的数据存储在 Hadoop 的 HDFS 中，弹性 MapReduce 服务默认为您开启数据三备份功能。同时，数据块的存储持久性依赖于您在购买弹性 MapReduce 服务时选择的存储介质，各存储介质及数据持久性说明如下：

##### 1.1 云服务器块存储
每月您申请实例的云服务器块存储的持久性为 99.999%。即每月每 100000 个云服务器的块存储实例，每月只有 1 个存储卷有数据丢失的可能性。
##### 1.2 云硬盘
每月您申请的 CBS 云硬盘的持久性 99.999999%。

若您的数据存储在对象存储中，数据可靠性请参见[《对象存储服务等级协议》](https://www.qcloud.com/document/product/436/6227)。

#### 2. 数据可销毁性
在您要求删除数据或设备在弃置、转售前，腾讯云将采取磁盘低级格式化操作彻底删除您所有数据，并无法复原，硬盘到期报废时将进行消磁。

#### 3. 数据迁移性
- 若您的数据存储在 HDFS 中，您可以通过 DistCp 工具将 HDFS 中的数据迁移至另一个 HDFS 中。
- 若您的数据存储在 COS 中，数据可迁移性请参见[《对象存储服务等级协议》](https://www.qcloud.com/document/product/436/6227)。

#### 4. 数据私密性
弹性 MapReduce 服务管理的 Hadoop 集群中，只会为 1 台 CVM 主机承载的 Master 节点开放外网 IP 端口，其他所有节点均只能在集群私有网络中访问。除用户的账户信息、云服务器内网IP等服务器基础信息外，腾讯云无权无途径查看用户的其他数据。以上信息的查询，内部查看系统有严格的权限控制和操作记录。

#### 5. 数据知情权
目前弹性 MapReduce 底层依托的用户云服务器部署在六大数据中心，分别是：上海数据中心、广州数据中心、北京数据中心、香港数据中心、新加坡数据中心、北美数据中心。
用户已知的数据中心均遵守的当地的法律和中华人民共和国相关法律。
用户所有数据不会提供给任意第三方，除政府监管部门监管审计需要。用户所有数据不会存在国外数据中心或用于国外业务或数据分析。
为保证用户数据安全性，腾讯云采用同时存储三份数据副本的存储方式，并定期进行数据冷备操作。

#### 6. 数据可审查性
腾讯云在依据现有法律法规体系下，出于配合政府监管部门的监管或安全取证调查等原因的需要，在符合流程和手续完备的情况下，可以提供云服务器相关信息，包括关键组件的运行日志、运维人员的操作记录、用户操作记录等信息。

#### 7. 业务功能
腾讯云弹性 MapReduce 服务，为用户提供 Hadoop 集群创建、Hadoop 软件安装部署、集群弹性伸缩、计算存储分离、监控运维支撑的功能。详细功能参见 [产品介绍页](https://www.qcloud.com/product/emr) 及 [产品文档](https://www.qcloud.com/document/product/589)。 

#### 8. 业务可用性
高 HA（高可用）集群的弹性 MapReduce 服务承诺 99.999999% 的业务可用性，非HA集群主要用于测试使用，不做可用性保障。弹性 MapReduce 软件运行在于 CVM 之上，CVM 可用性参见[《云主机服务等级协议》](https://www.qcloud.com/document/product/301/1973)。

#### 9. 业务资源调配能力
当您的集群节点计算和存储能力无法满足使用需求时，可以通过控制台或 API 的方式对集群进行扩容。单次扩容少于 20 个节点，可在 15 分钟内完成。如需申请大于 20 个节点的扩容需求，请通过工单方式联系我们。

#### 10. 故障恢复能力
高可用的弹性 MapReduce 服务可在 Master 节点出现故障时自动切换到备用节点。腾讯云云服务器具备故障迁移能力，可在母机故障发生时，无需用户参与，自动将云服务器迁移至新的母机，保证客户服务的连续性。同时，腾讯云提供专业团队 7x24 小时帮助维护。

## 第三条 网络接入性能
用户购买云服务器时，可自主选择每个云服务器的公网出口带宽，可配置范围为 0-100Mbps 或 0-200Mbps(不同资源带宽上限有差别，以官网展示为准),腾讯云采用 BGP 多线接入方式，全面覆盖超 20 线运营商接入，包括联通、移动、电信、网通、铁通、教育网、科技网、广电网等；提高用户的网络访问质量。

## 第四条 服务计量准确性
腾讯云服务的费用在用户的选购页面和订单页面均有明确展示，用户可自行选择具体服务类型并按列明的价格进行购买。具体价格以腾讯云官网公布的价格为准。腾讯云按照用户选购弹性 MapReduce 服务时列出的小时单价的使用时长进行收费。

## 第五条 补偿
#### 1. 适用范围
适用于由腾讯云故障原因导致用户的弹性 MapReduce 服务无法正常调度集群时，以及腾讯云故障导致的网站（开发者服务网站）无法访问时，用户要求腾讯云针对事故/故障而进行的补偿。

#### 2. 补偿标准原则
故障时间 = 故障解决时间 - 故障开始时间。按分钟计算故障时间，故障时间小于 1 分钟的按 1 分钟计算。
例如：故障时间为 1 分 01 秒，按 2 分钟算。

弹性 MapReduce 服务故障百倍赔偿：
- 预付费：赔偿方式是延长故障服务的使用时长，延长时间 = 故障时间 * 100。
- 后付费：赔偿方式是补偿现金券，现金券金额 = 故障弹性 MapReduce 服务每天费用 / 24 / 60 × 故障时间 × 100。

