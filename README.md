## 说明

- 本项目是针对node环境的paas平台和游戏玩具而生，采用Argo隧道部署节点，集成哪吒探针v0或v1可选。
- node玩具平台只需上传index.js、index.html和package.json即可，paas平台需要docker部署的才上传Dockerfile。
- 不填写ARGO_DOMAIN和ARGO_AUTH两个变量即启用临时隧道，反之则使用固定隧道。
- 哪吒v0/v1可选,当哪吒端口为{443,8443,2096,2087,2083,2053}其中之一时，自动开启tls。

## 环境变量

| 变量名       | 是否必须 | 默认值                               | 说明                 |
| ------------ | -------- | ------------------------------------ | -------------------- |
| UPLOAD_URL   | 否       | -                                    | 订阅上传地址         |
| PROJECT_URL  | 否       | https://www.google.com               | 项目分配的域名       |
| AUTO_ACCESS  | 否       | false                                | 是否开启自动访问保活 |
| PORT         | 否       | 3000                                 | HTTP服务监听端口     |
| ARGO_PORT    | 否       | 8001                                 | Argo隧道端口         |
| UUID         | 否       | 6bf62ccf-f074-438b-b8fc-8ae7ff4167d5 | 用户UUID             |
| NEZHA_SERVER | 否       | -                                    | 哪吒面板域名         |
| NEZHA_PORT   | 否       | -                                    | 哪吒端口             |
| NEZHA_KEY    | 否       | -                                    | 哪吒密钥             |
| ARGO_DOMAIN  | 否       | -                                    | Argo固定隧道域名     |
| ARGO_AUTH    | 否       | -                                    | Argo固定隧道密钥     |
| CFIP         | 否       | saas.sin.fan                         | 节点优选域名或IP     |
| CFPORT       | 否       | 443                                  | 节点端口             |
| NAME         | 否       | Vls                                  | 节点名称前缀         |
| FILE_PATH    | 否       | ./tmp                                | 运行目录             |
| SUB_PATH     | 否       | sub                                  | 订阅路径             |

### 环境变量配置

可使用 `.env` 文件来配置环境变量运行

```bash
SUB_PATH="sub"
PORT=3000
ARGO_PORT=8001
CFIP="saas.sin.fan"
CFPORT=443
NAME="Base"
UUID="6bf62ccf-f074-438b-b8fc-8ae7ff4167d5"
ARGO_DOMAIN="argo.your-domain.com"
ARGO_AUTH="your-argo-auth"
NEZHA_SERVER="nz.your-domain.com"
NEZHA_PORT=8008
NEZHA_KEY="your-nezha-key"
ARGO_DOMAIN="argo.your-domain.com"
ARGO_AUTH="your-argo-auth"
FILE_PATH="./tmp"
UPLOAD_URL="https://your-merge-sub-domain.com"
PROJECT_URL="https://your-project-domain.com"
AUTO_ACCESS=false
```
