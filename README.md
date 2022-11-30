# wireguard

一件安装wireguard 实现异地组网

WireGuard是一个安全的网络隧道，在第3层运行，作为Linux的内核虚拟网络接口实现，其目标是在大多数情况下取代IPsec，以及流行的用户空间和/或基于tls的解决方案，如OpenVPN，同时更安全、性能更高且更易于使用。虚拟隧道接口基于安全隧道的基本原则:对等公钥和隧道源IP地址之间的关联。它使用基于NoiseIK的单次往返密钥交换，并使用新的计时器状态机机制对用户透明地处理所有会话创建。短的预共享静态密钥（Curve25519点）用于OpenSSH风格的相互认证。该协议除了提供高度的身份隐藏之外，还提供了强大的完美前向保密性。使用ChaCha20Poly1305身份验证加密将数据包封装在UDP中可以实现传输速度。 IP绑定cookie的改进形式用于缓解拒绝服务攻击，从而大大改进了IKEv2和DTLS的cookie机制以添加加密和身份验证。总体设计不允许为接收到的数据包分配任何资源，并且从系统的角度来看，有多种有趣的Linux实现技术用于队列和并行性。最后，WireGuard可以轻松地用不到4,000行代码在Linux上实现，从而易于审核和验证。
WireGuard的优势：
更轻便：以Linux内核模块的形式运行，资源占用小。
更高效：相比目前主流的IPSec、OpenVPN等协议，WireGuard的效率要更高。
更快速：比目前主流的VPN协议，连接速度要更快。
更安全：使用了更先进的加密技术。
更易搭建：部署难度相对更低。
更隐蔽：以UDP协议进行数据传输，比TCP协议更低调。
不易被封锁：TCP阻断对WireGuard无效，IP被墙的情况下仍然可用。
更省电：不使用时不进行数据传输，移动端更省电。
搭建方法:
ubuntu:
apt update
apt install curl
curl -O https://raw.githubusercontent.com/Love5461/wireguard/master/wg_mult.sh && chmod +x wg_mult.sh && ./wg_mult.sh
centos
yum install curl
curl -O https://raw.githubusercontent.com/love5461/wireguard/master/wg_mult.sh && chmod +x wg_mult.sh && ./wg_mult.sh
客户端官网有哦,不要用乱七八糟的客户端!
另外你可以使用openvpn也是不错的选择
如果在中国,我不建议你自己搭建这样的服务器

如果有问题，留言。
