问题1
../bin/configtxgen -profile TwoOrgsChannel \
> -outputCreateChannelTx \
> ./channel-artifacts/channel.tx \
> -channelID mychannel
2018-02-05 14:02:16.648 CST [common/configtx/tool] main -> INFO 001 Loading configuration
2018-02-05 14:02:16.648 CST [common/configtx/tool/localconfig] Load -> CRIT 002 Error reading configuration:  Unsupported Config Type ""
2018-02-05 14:02:16.648 CST [common/configtx/tool] func1 -> ERRO 003 Could not find configtx.yaml. Please make sure that FABRIC_CFG_PATH is set to a path which contains configtx.yaml

解决1
export FABRIC_CFG_PATH=$PWD


ExecStart=/usr/bin/dockerd --dns=10.254.0.2 --dns-search org1.svc.cluster.local. --dns-search org2.svc.cluster.local. --dns-search default.svc.cluster.local. --dns-search orgorderer1.svc.cluster.local. --dns-search svc.cluster.local. --dns-search cluster.local.  --dns-opt ndots:2 --dns-opt timeout:2 --dns-opt attempts:2 --dns=192.168.1.29
