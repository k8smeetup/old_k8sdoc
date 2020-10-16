

生成所有 bootstrap token 配置并生成一个初始 token



### 概要



Bootstrap tokens 用来建立加入集群的节点和 master 节点间的双向互信。

此命令生成所有生成 bootstrap tokens 的所需配置并生成一个初始 token。

Alpha 免责声明：此命令处于 alpha 阶段。

```
kubeadm alpha phase bootstrap-token all
```


### 例子

```
  # 生成所有 bootstrap token 配置并生成一个初始 token
  # 功能上等价于 kubeadm init 生成的。
  kubeadm alpha phase bootstrap-token all
```





### 选择项

```
      --cert-dir string      证书存储路径（默认值 "/etc/kubernetes/pki"）
      --config string        kubeadm config 文件路径（警告：配置文件的使用是实验性的）
      --description string   人性化描述如何使用 token（默认值 "The default bootstrap token generated by 'kubeadm init'."）
      --groups stringSlice   使用这个 token 进行身份认证的额外组。必须符合 "system:bootstrappers:[a-z0-9:-]{0,255}[a-z0-9]"（默认值 [system:bootstrappers:kubeadm:default-node-token]）
      --skip-token-print     跳过打印 bootstrap token
      --token string         token 用来建立节点和 master 间的双向互信
      --ttl duration         token 在被自动删除前的持续时间（如 1s, 2m, 3h）。如果设为'0'，token将永不时效（默认值 24h0m0s）
      --usages stringSlice   描述token 可以使用的方式。您可以多次传递 --usages 或用逗号分隔开多个选择项。有效的选择项: [signing,authentication]（默认值 [signing,authentication]）
```




### 继承于父命令的选择项

```
      --kubeconfig string   与集群对话时用到的 KubeConfig 文件（默认值 "/etc/kubernetes/admin.conf"）
```