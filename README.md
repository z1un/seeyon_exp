# 致远OA综合漏洞利用脚本

覆盖漏洞

```
致远OA_A6_createMysql_数据库敏感信息泄露
致远OA_A6_DownExcelBeanServlet_用户敏感信息下载
致远OA_A6_initDataAssess_用户敏感信息泄露
致远OA_A6_setextno_SQL注入Getshell
致远OA_A6_test_SQL注入Getshell
致远OA_A8_htmlofficeservlet_RCE
致远OA_getSessionList_Session泄漏
致远OA_ajax_登录绕过_任意文件上传
致远OA_webmail_任意文件下载
致远OA_Session泄露_任意文件上传
致远OA_Fastjson_反序列化
```

其中致远OA_Fastjson_反序列化漏洞没有实现自动化，可利用工具：[JNDIExploit](https://github.com/feihong-cs/JNDIExploit)

```bash
java -jar JNDIExploit-1.2-SNAPSHOT.jar -i 0.0.0.0 -l 1389 -p 1289
```

先在vps运行以上JNDI反序列化漏洞利用工具，然后复制脚本提供的Payload，替换ldap链接到BurpSuite中发包测试发包，可回显。

![202108092129583](https://oss.zjun.info/zjun.info/202108092129583.png)

最后推荐一个关于致远OA数据库密码解码及相关笔记的项目：

https://github.com/jas502n/OA-Seeyou

参考：

http://wiki.peiqi.tech/

https://wiki.0-sec.org/

https://github.com/Summer177/seeyon_exp