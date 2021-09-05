## neko-relay-land

[Neko Neko Relay](https://relay.nekoneko.cloud) 隧道落地后端

## 安装后端

下载: (其他OS请自行替换下载连接: https://github.com/nkeonkeo/neko-relay-land/releases/tag/v1.0)

```bash
wget https://github.com/nkeonkeo/neko-relay-land/releases/download/v1.0/neko-relay_linux_amd64 -O /usr/bin/neko-relay
chmod +x /usr/bin/neko-relay
```

初始化服务: `neko-relay -g init`

菜单引导: `neko-relay -g menu`

## 添加转发

1. 首先在面板添加转发
   
   选择支持自定义隧道的节点
   
   选择 `ws_tunnel_client_tcp+udp` 类型

2. 在目标服务器(隧道落地端)新增规则

   ```bash
   neko-relay -g add
   ```
   
   1. 选择类型:
      
      WS隧道加密端(TCP+UDP) 对应 面板 `ws_tunnel_client_tcp+udp` 类型

      WSS隧道加密端(TCP+UDP) 对应 面板 `wss_tunnel_client_tcp+udp` 类型
   
   3. 规则ID: 
   
      填写面板添加后提示的`规则ID`(如果忘记可以在面板上点击规则状态复制规则ID)
   
   4. 本机端口:
   
      面板添加规则时你填写的目标端口
   
   5. 目标地址、目标端口: 
   
      隧道要转发的目标

## 其他功能

菜单引导: `neko-relay -g menu`

初始化服务: `neko-relay -g init`

重启服务: `neko-relay -g restart`

停止服务: `neko-relay -g stop`

更新后端: `neko-relay -g update`

查看规则列表: `neko-relay -g list`

添加规则: `neko-relay -g add`

删除规则: `neko-relay -g del`
