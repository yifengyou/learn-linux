# iptables基本应用

*   iptables：规则管理工具
    *   添加、修改、删除、显示等
    *   自动完成规则语法检查后送往内核netfilter，通过一个系统调用输入输出，如果精通规则可以直接调用系统调用。
    *   规则和链有计数器
        *   pkgs：由规则或链所匹配到的报文的个数
        *   bytes：由规则或链匹配到的所有报文大小之和







*   iptables命令
    *   定义规则的语法   **iptables [-t table]  SUBCOMMAND CHAIN CRITERIA  -j TARGET**

```
       iptables [-t table] {-A|-C|-D} chain rule-specification

       ip6tables [-t table] {-A|-C|-D} chain rule-specification

       iptables [-t table] -I chain [rulenum] rule-specification

       iptables [-t table] -R chain rulenum rule-specification

       iptables [-t table] -D chain rulenum

       iptables [-t table] -S [chain [rulenum]]

       iptables [-t table] {-F|-L|-Z} [chain [rulenum]] [options...]

       iptables [-t table] -N chain

       iptables [-t table] -X [chain]

       iptables [-t table] -P chain target

       iptables [-t table] -E old-chain-name new-chain-name
       
        [-t table] 说明可以省略，默认是filter
```



*   -t table 
    *   filter，nat,mangle,raw 
*   链管理
    *   -F：flush 清空规则链。省略链表示清空表上的所有链，也可以指定规则
    *   -N：new，创建新的自定义规则链
    *   -X：drop、delete，删除用户自定义的规则链，但是必须为空链才行，也就是说里面不能有规则
    *   -Z：zero，清零，置零规则计数器。重新开始计数
    *   -P：把指定链的默认处理方式修改为指定方式
        *   **iptables [-t table] -P chain target **
        *   对filter表而言默认策略通常有ACCEPT,DROP,REJECT
*   规则管理









