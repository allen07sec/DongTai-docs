---
sidebar_position: 5
---
import Highlight from '@site/src/components/Highlight';

# 获取token

:::info 如何获取 sca-token

添加小助理，获取唯一token，若文档内容无法搜索和解决您的问题，我们会及时给您回复

* 添加企业微信小助理：小依

  <img src="/img/docs/getting-started/server/xiaoyi.png" width="18%"/>
:::

## docker形式
### 1.进入dtctl目录配置token

```bash
cd DongTai/deploy/docker-compose/
```

### 2.修改配置文件config-tutorial.ini

```bash
修改文件第39行替换为自己的token：

token = 121212121212-1234-1234-1234-123444444444
```

### 3.重新启动洞态iast

```bash
./dtctl remove
./dtctl install

ok ！
```
## Kubernetes
### 1.进入dtctl目录配置token

```bash
cd DongTai/kubernetes/helm
```

### 2.修改配置文件values.yaml

```bash
修改文件第43行替换为自己的token：

token = 121212121212-1234-1234-1234-123444444444
```

### 3.替换文件启动洞态iast

```bash
helm install project --create-namespace -n dongtai dongtai/dongtai-iast \
--values /tmp/my-values.yaml
```

### 4.覆盖单值启动
```bash
helm install project --create-namespace -n dongtai dongtai/dongtai-iast \  
--set storage.persistentVolumeClaim=pvc \  
--set sca.sca_token=XXXXXXXX
```
```






