# 酸酸仁乳（ShadowsocksRR）一键安装包饮用指南
这是一个我魔改的酸酸乳一键安装包，原脚本来自秋水逸冰（Teddysun）大神https://git.io/vdMTK ，原脚本里的ShadowsocksR服务端版本有一些旧了，底包最高只能支持到auth_chain_b协议，我的一键安装包目前可以随时和@Akkariiin接盘后的ShadowsocksR（ShadowsocksRR）https://git.io/vdMTB 的最新版本保持同步。
### 使用方法：
if 已安装过秋水逸冰大神的一键包，请先卸载：
<pre><code> ./shadowsocksR.sh uninstall </code></pre>
then 重新安装：
<pre><code>wget --no-check-certificate -O shadowsocksRR.sh https://git.io/vdMUr</code></pre>
<pre><code>chmod +x shadowsocksRR.sh</code></pre>
<pre><code>./shadowsocksRR.sh 2>&1 | tee shadowsocksR.log</code></pre>
安装完成后，推荐重启一下SSRR服务：
<pre><code>/etc/init.d/shadowsocks restart</code></pre>
<br />

### 更新历史：
- auth_chain_c 协议在配合20端口使用下，在一段时间正常连接后，突然失去响应，切换到别的节点再切换回来，即立马恢复正常，配合80、443等端口使用，未发现明显的问题，目前还是不推荐使用，不在一键脚本里添加该选项；（2017.10.17）
- 经测试，移除对 auth_chain_c 协议的支持，我用了一点事儿都没，然后就…………（2017.10.16）;
- 替换安装提示中的关键词ShadowsocksR为ShadowsocksRR（2017.10.16）；
- 更新libsodium至1.0.15；（2017.10.16）；
- 添加对 salsa20、xchacha20、xsalsa20 加密方式的支持（2017.10.15）；
- 添加对 auth_chain_e和add auth_chain_f 协议的支持（2017.10.15）；
- 添加对 auth_chain_c和add auth_chain_d 协议的支持（2017.10.15）。
