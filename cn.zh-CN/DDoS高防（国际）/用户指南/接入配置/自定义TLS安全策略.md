# 自定义TLS安全策略 {#task_960830 .task}

DDoS高防（国际）支持TLS安全策略自定义功能，您可以根据实际业务需要选择合适的TLS协议。

-   网站配置已关联增强功能套餐的DDoS高防（国际）实例。
-   已添加网站接入配置（具体操作请参见[网站业务接入DDoS高防（国际）防护](intl.zh-CN/DDoS高防（国际）/快速入门/网站业务接入DDoS高防（国际）防护.md#)）且网站支持HTTPS协议。
-   已上传对应的HTTPS证书（具体操作请参见[上传HTTPS证书](intl.zh-CN/DDoS高防（国际）/用户指南/接入配置/上传HTTPS证书.md#)）。

如果您的业务需要通过PCI DSS 3.2认证，需要禁用TLS1.0协议；同时，您的另一个业务的访问终端仅支持TLS1.0协议，需要兼容TLS1.0协议。这种情况，您可以通过TLS安全策略自定义功能为不同业务灵活配置所需的TLS安全策略。

1.  登录[DDoS高防（国际）管理控制台](https://yundun.console.aliyun.com/?p=ddosdip)。
2.  在左侧导航栏，单击**接入配置** \> **网站接入**。
3.  选择已添加的网站业务配置，单击其证书状态列中的**TLS安全策略**。
4.  在**TLS安全策略配置**对话框中，选择**TLS版本**和**加密套件**。 

    -   **TLS版本**：默认为**支持TLS1.0及以上版本，兼容性最好，安全性较低**。您可以根据安全需要选择仅支持TLS1.1或TLS1.2以上版本。
    -   **加密套件**：
        -   **仅支持强加密套件，安全性较高，兼容性较低** 

            仅支持以下强加密套件：

            -   ECDHE-ECDSA-AES256-GCM-SHA384
            -   ECDHE-RSA-AES256-GCM-SHA384
            -   ECDHE-ECDSA-AES128-GCM-SHA256
            -   ECDHE-RSA-AES128-GCM-SHA256
            -   ECDHE-ECDSA-WITH-CHACHA20-POLY1305
            -   ECDHE-RSA-WITH-CHACHA20-POLY1305
            -   ECDHE-RSA-AES256-CBC-SHA
            -   ECDHE-RSA-AES128-CBC-SHA
            -   ECDHE-ECDSA-AES256-CBC-SHA
            -   ECDHE-ECDSA-AES128-CBC-SHA
        -   **全部加密套件，安全性较低，兼容性较高** 

            除上述强加密套件外，还支持以下四种弱加密套件：

            -   RSA-AES256-CBC-SHA
            -   RSA-AES128-CBC-SHA
            -   ECDHE-RSA-3DES-EDE-CBC-SHA
            -   RSA-3DES-EDE-CBC-SHA
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/776342/156436734850665_zh-CN.png)


