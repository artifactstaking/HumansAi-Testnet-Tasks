# Restart your validator three times during Mission 2

### Restart 1 - May 16 11:42:23 UTC

~~~bash
validator@human-test-val1:~$ sudo systemctl restart humans && sudo journalctl -u humans -f
[sudo] password for validator:
May 16 11:42:23 human-test-val1 cosmovisor[242011]:   UNSAFE_SKIP_BACKUP: true
May 16 11:42:23 human-test-val1 cosmovisor[242011]:   DAEMON_PREUPGRADE_MAX_RETRIES: 0
May 16 11:42:23 human-test-val1 cosmovisor[242011]: Derived Values:
May 16 11:42:23 human-test-val1 cosmovisor[242011]:         Root Dir: /home/validator/.humansd/cosmovisor
May 16 11:42:23 human-test-val1 cosmovisor[242011]:      Upgrade Dir: /home/validator/.humansd/cosmovisor/upgrades
May 16 11:42:23 human-test-val1 cosmovisor[242011]:      Genesis Bin: /home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:42:23 human-test-val1 cosmovisor[242011]:   Monitored File: /home/validator/.humansd/data/upgrade-info.json
May 16 11:42:23 human-test-val1 cosmovisor[242011]:  module=cosmovisor
May 16 11:42:23 human-test-val1 cosmovisor[242011]: 11:42AM INF running app args=["start","humansd","start","--metrics","--evm.tracer=json","json-rpc.api","eth,txpool,personal,net,debug,web3,miner","--api.enable"] module=cosmovisor path=/home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:42:23 human-test-val1 cosmovisor[242011]: 11:42AM ERR failed to read error="lstat /home/validator/.humansd/cosmovisor/current/upgrade-info.json: no such file or directory" filename=/home/validator/.humansd/cosmovisor/current/upgrade-info.json module=cosmovisor
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Unlocking keyring
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF starting ABCI with Tendermint
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF starting node with ABCI Tendermint in-process
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start impl=EventBus module=events msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF ABCI Handshake App Info hash="2\x05�4L�J\x04���cw\u07bau1��~�7��X�\x16��>!�" height=72004 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF ABCI Replay Blocks appHeight=72004 module=consensus server=node stateHeight=72004 storeHeight=72004
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Completed ABCI Handshake - CometBFT and App are synced appHash="2\x05�4L�J\x04���cw\u07bau1��~�7��X�\x16��>!�" appHeight=72004 module=consensus server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF This node is a validator addr=266E3FA7B7034D61A646DD4FB0A5992A85E031D3 module=consensus pubKey=v2QlXKDGkgYfpghzl/wS3kVyhKDfgP3zEynQdqB0ESE= server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF P2P Node ID ID=d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e file=/home/validator/.humansd/config/node_key.json module=p2p server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Adding persistent peers addrs=[] module=p2p server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 11:42:24 human-test-val1 cosmovisor[242018]: 11:42AM INF Add our address to book addr={"id":"d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e","ip":"206.125.33.0","port":26656} book=/home/validator/.humansd/config/addrbook.json module=p2p server=node
~~~

### Restart 2 - May 16 11:44:59 UTC

~~~bash
validator@human-test-val1:~$ sudo systemctl restart humans && sudo journalctl -u humans -f
May 16 11:44:59 human-test-val1 cosmovisor[242101]:   UNSAFE_SKIP_BACKUP: true
May 16 11:44:59 human-test-val1 cosmovisor[242101]:   DAEMON_PREUPGRADE_MAX_RETRIES: 0
May 16 11:44:59 human-test-val1 cosmovisor[242101]: Derived Values:
May 16 11:44:59 human-test-val1 cosmovisor[242101]:         Root Dir: /home/validator/.humansd/cosmovisor
May 16 11:44:59 human-test-val1 cosmovisor[242101]:      Upgrade Dir: /home/validator/.humansd/cosmovisor/upgrades
May 16 11:44:59 human-test-val1 cosmovisor[242101]:      Genesis Bin: /home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:44:59 human-test-val1 cosmovisor[242101]:   Monitored File: /home/validator/.humansd/data/upgrade-info.json
May 16 11:44:59 human-test-val1 cosmovisor[242101]:  module=cosmovisor
May 16 11:44:59 human-test-val1 cosmovisor[242101]: 11:44AM INF running app args=["start","humansd","start","--metrics","--evm.tracer=json","json-rpc.api","eth,txpool,personal,net,debug,web3,miner","--api.enable"] module=cosmovisor path=/home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:44:59 human-test-val1 cosmovisor[242101]: 11:44AM ERR failed to read error="lstat /home/validator/.humansd/cosmovisor/current/upgrade-info.json: no such file or directory" filename=/home/validator/.humansd/cosmovisor/current/upgrade-info.json module=cosmovisor
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Unlocking keyring
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF starting ABCI with Tendermint
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF starting node with ABCI Tendermint in-process
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start impl=EventBus module=events msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF ABCI Handshake App Info hash="\u009eYkt]�8>B��g*����J��Q{X\x11\x05��\x1f&" height=72033 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF ABCI Replay Blocks appHeight=72033 module=consensus server=node stateHeight=72033 storeHeight=72033
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Completed ABCI Handshake - CometBFT and App are synced appHash="\u009eYkt]�8>B��g*����J��Q{X\x11\x05��\x1f&" appHeight=72033 module=consensus server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF This node is a validator addr=266E3FA7B7034D61A646DD4FB0A5992A85E031D3 module=consensus pubKey=v2QlXKDGkgYfpghzl/wS3kVyhKDfgP3zEynQdqB0ESE= server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF P2P Node ID ID=d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e file=/home/validator/.humansd/config/node_key.json module=p2p server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Adding persistent peers addrs=[] module=p2p server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Add our address to book addr={"id":"d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e","ip":"206.125.33.0","port":26656} book=/home/validator/.humansd/config/addrbook.json module=p2p server=node
May 16 11:44:59 human-test-val1 cosmovisor[242108]: 11:44AM INF Add our address to book addr={"id":"d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e","ip":"0.0.0.0","port":26656} book=/home/validator/.humansd/config/addrbook.json module=p2p server=node

~~~

### Restart 3 - May 16 11:46:32 UTC

~~~
validator@human-test-val1:~$ sudo systemctl restart humans && sudo journalctl -u humans -f
May 16 11:46:32 human-test-val1 cosmovisor[242141]:   UNSAFE_SKIP_BACKUP: true
May 16 11:46:32 human-test-val1 cosmovisor[242141]:   DAEMON_PREUPGRADE_MAX_RETRIES: 0
May 16 11:46:32 human-test-val1 cosmovisor[242141]: Derived Values:
May 16 11:46:32 human-test-val1 cosmovisor[242141]:         Root Dir: /home/validator/.humansd/cosmovisor
May 16 11:46:32 human-test-val1 cosmovisor[242141]:      Upgrade Dir: /home/validator/.humansd/cosmovisor/upgrades
May 16 11:46:32 human-test-val1 cosmovisor[242141]:      Genesis Bin: /home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:46:32 human-test-val1 cosmovisor[242141]:   Monitored File: /home/validator/.humansd/data/upgrade-info.json
May 16 11:46:32 human-test-val1 cosmovisor[242141]:  module=cosmovisor
May 16 11:46:32 human-test-val1 cosmovisor[242141]: 11:46AM INF running app args=["start","humansd","start","--metrics","--evm.tracer=json","json-rpc.api","eth,txpool,personal,net,debug,web3,miner","--api.enable"] module=cosmovisor path=/home/validator/.humansd/cosmovisor/genesis/bin/humansd
May 16 11:46:32 human-test-val1 cosmovisor[242141]: 11:46AM ERR failed to read error="lstat /home/validator/.humansd/cosmovisor/current/upgrade-info.json: no such file or directory" filename=/home/validator/.humansd/cosmovisor/current/upgrade-info.json module=cosmovisor
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Unlocking keyring
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF starting ABCI with Tendermint
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF starting node with ABCI Tendermint in-process
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start impl=EventBus module=events msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF ABCI Handshake App Info hash="���7R���yo�h5���`0��K�V�{}\tr����" height=72045 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF ABCI Replay Blocks appHeight=72045 module=consensus server=node stateHeight=72045 storeHeight=72045
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Completed ABCI Handshake - CometBFT and App are synced appHash="���7R���yo�h5���`0��K�V�{}\tr����" appHeight=72045 module=consensus server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF This node is a validator addr=266E3FA7B7034D61A646DD4FB0A5992A85E031D3 module=consensus pubKey=v2QlXKDGkgYfpghzl/wS3kVyhKDfgP3zEynQdqB0ESE= server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF P2P Node ID ID=d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e file=/home/validator/.humansd/config/node_key.json module=p2p server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Adding persistent peers addrs=[] module=p2p server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 11:46:32 human-test-val1 cosmovisor[242150]: 11:46AM INF Add our address to book addr={"id":"d7eb0e65cecbeeaa649b0a2fdf95ca2fb9f0cc3e","ip":"206.125.33.0","port":26656} book=/home/validator/.humansd/config/addrbook.json module=p2p server=node
~~~
