**rhyme@ip-10-199-80-63:\~$** sudo kubectl get pods

The connection to the server 10.199.80.63:8443 was refused - did you
specify the right host or port?

**rhyme@ip-10-199-80-63:\~$** sudo kubectl get pods -l app=nginx2

The connection to the server 10.199.80.63:8443 was refused - did you
specify the right host or port?

**rhyme@ip-10-199-80-63:\~$** sudo kubectl get rc

The connection to the server 10.199.80.63:8443 was refused - did you
specify the right host or port?

**rhyme@ip-10-199-80-63:\~$** cd yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

The connection to the server 10.199.80.63:8443 was refused - did you
specify the right host or port?

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods -l app=nginx2

The connection to the server 10.199.80.63:8443 was refused - did you
specify the right host or port?

**rhyme@ip-10-199-80-63:\~/**yml$ sudo minikube start --vm-driver=none

😄 minikube v1.2.0 on linux (amd64)

💡 Tip: Use 'minikube start -p \<name>' to create a new cluster, or
'minikube delete' to delete this one.

🔄 Restarting existing none VM for "minikube" ...

⌛ Waiting for SSH access ...

🐳 Configuring environment for Kubernetes v1.15.0 on Docker 19.03.6

▪ kubelet.resolv-conf=/run/systemd/resolve/resolv.conf

🔄 Relaunching Kubernetes v1.15.0 using kubeadm ...

🤹 Configuring local host environment ...

⚠️ The 'none' driver provides limited isolation and may reduce system
security and reliability.

⚠️ For more information, see:

👉
https://github.com/kubernetes/minikube/blob/master/docs/vmdriver-none.md

⚠️ kubectl and minikube configuration will be stored in /home/rhyme

⚠️ To use kubectl or minikube commands as your own user, you may

⚠️ need to relocate them. For example, to overwrite your own settings:

▪ sudo mv /home/rhyme/.kube /home/rhyme/.minikube $HOME

▪ sudo chown -R $USER $HOME/.kube $HOME/.minikube

💡 This can also be done automatically by setting the env var
CHANGE_MINIKUBE_NONE_USER=true

⌛ Verifying: apiserver proxy etcd scheduler controller dns

🏄 Done! kubectl is now configured to use "minikube"

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods -l app=nginx2

NAME READY STATUS RESTARTS AGE

my-nginx-rc-57bqf 0/1 Completed 0 86m

my-nginx-rc-dpc7n 0/1 Completed 0 86m

my-nginx-rc-grwx6 0/1 Completed 0 86m

my-nginx-rc-hprd6 0/1 Completed 0 86m

my-nginx-rc-khkjb 0/1 Completed 0 86m

my-nginx-rc-ljj9q 0/1 Completed 0 86m

my-nginx-rc-m5n5t 0/1 Completed 0 86m

my-nginx-rc-rmz4r 0/1 Completed 0 86m

my-nginx-rc-stxth 0/1 Completed 0 86m

my-nginx-rc-vpjlk 1/1 Running 1 86m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

NAME DESIRED CURRENT READY AGE

my-nginx-rc 10 10 10 92m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

NAME READY STATUS RESTARTS AGE

my-nginx-pod 1/1 Running 1 3h7m

my-nginx-rc-57bqf 1/1 Running 1 87m

my-nginx-rc-dpc7n 1/1 Running 1 87m

my-nginx-rc-grwx6 1/1 Running 1 87m

my-nginx-rc-hprd6 1/1 Running 1 87m

my-nginx-rc-khkjb 1/1 Running 1 87m

my-nginx-rc-ljj9q 1/1 Running 1 87m

my-nginx-rc-m5n5t 1/1 Running 1 87m

my-nginx-rc-rmz4r 1/1 Running 1 87m

my-nginx-rc-stxth 1/1 Running 1 87m

my-nginx-rc-vpjlk 1/1 Running 1 87m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

NAME READY STATUS RESTARTS AGE

my-nginx-pod 1/1 Running 1 3h8m

my-nginx-rc-57bqf 1/1 Running 1 88m

my-nginx-rc-dpc7n 1/1 Running 1 88m

my-nginx-rc-grwx6 1/1 Running 1 88m

my-nginx-rc-hprd6 1/1 Running 1 88m

my-nginx-rc-khkjb 1/1 Running 1 88m

my-nginx-rc-ljj9q 1/1 Running 1 88m

my-nginx-rc-m5n5t 1/1 Running 1 88m

my-nginx-rc-rmz4r 1/1 Running 1 88m

my-nginx-rc-stxth 1/1 Running 1 88m

my-nginx-rc-vpjlk 1/1 Running 1 88m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

NAME DESIRED CURRENT READY AGE

my-nginx-rc 10 10 10 99m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

NAME READY STATUS RESTARTS AGE

my-nginx-pod 1/1 Running 1 3h14m

my-nginx-rc-57bqf 1/1 Running 1 94m

my-nginx-rc-dpc7n 1/1 Running 1 94m

my-nginx-rc-grwx6 1/1 Running 1 94m

my-nginx-rc-hprd6 1/1 Running 1 94m

my-nginx-rc-khkjb 1/1 Running 1 94m

my-nginx-rc-ljj9q 1/1 Running 1 94m

my-nginx-rc-m5n5t 1/1 Running 1 94m

my-nginx-rc-rmz4r 1/1 Running 1 94m

my-nginx-rc-stxth 1/1 Running 1 94m

my-nginx-rc-vpjlk 1/1 Running 1 94m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f nginx-rc-og.yml

replicationcontroller/my-nginx-rc configured

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

NAME DESIRED CURRENT READY AGE

my-nginx-rc 10 10 1 100m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f nginx-rc-og.yml

replicationcontroller/my-nginx-rc-og created

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

NAME DESIRED CURRENT READY AGE

my-nginx-rc 10 10 10 101m

my-nginx-rc-og 10 10 0 7s

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

NAME READY STATUS RESTARTS AGE

my-nginx-pod 1/1 Running 1 3h16m

my-nginx-rc-57bqf 1/1 Running 1 96m

my-nginx-rc-65vtv 1/1 Running 0 57s

my-nginx-rc-7l7jd 1/1 Running 0 57s

my-nginx-rc-9m5rw 1/1 Running 0 57s

my-nginx-rc-d6n4c 1/1 Running 0 57s

my-nginx-rc-dpc7n 1/1 Running 1 96m

my-nginx-rc-f6sf5 1/1 Running 0 57s

my-nginx-rc-grwx6 1/1 Running 1 96m

my-nginx-rc-hprd6 1/1 Running 1 96m

my-nginx-rc-khkjb 1/1 Running 1 96m

my-nginx-rc-ljj9q 1/1 Running 1 96m

my-nginx-rc-m5n5t 1/1 Running 1 96m

my-nginx-rc-m62lf 1/1 Running 0 57s

my-nginx-rc-m8zw7 1/1 Running 0 57s

my-nginx-rc-mmp4r 1/1 Running 0 57s

my-nginx-rc-og-22lhb 1/1 Running 0 14s

my-nginx-rc-og-5kzx5 1/1 Running 0 14s

my-nginx-rc-og-7dzq2 1/1 Running 0 14s

my-nginx-rc-og-7jvxp 1/1 Running 0 14s

my-nginx-rc-og-8pv77 1/1 Running 0 14s

my-nginx-rc-og-9gs6w 1/1 Running 0 14s

my-nginx-rc-og-c7vc5 1/1 Running 0 14s

my-nginx-rc-og-lchvp 1/1 Running 0 14s

my-nginx-rc-og-ml85r 1/1 Running 0 14s

my-nginx-rc-og-wbcnm 1/1 Running 0 14s

my-nginx-rc-rmz4r 1/1 Running 1 96m

my-nginx-rc-stxth 1/1 Running 1 96m

my-nginx-rc-v8fmm 1/1 Running 0 57s

my-nginx-rc-vbpgd 1/1 Running 0 57s

my-nginx-rc-vpjlk 1/1 Running 1 96m

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl delete pods -l app=nginx2

pod "my-nginx-rc-57bqf" deleted

pod "my-nginx-rc-dpc7n" deleted

pod "my-nginx-rc-grwx6" deleted

pod "my-nginx-rc-hprd6" deleted

pod "my-nginx-rc-khkjb" deleted

pod "my-nginx-rc-ljj9q" deleted

pod "my-nginx-rc-m5n5t" deleted

pod "my-nginx-rc-rmz4r" deleted

pod "my-nginx-rc-stxth" deleted

pod "my-nginx-rc-vpjlk" deleted

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

NAME READY STATUS RESTARTS AGE

my-nginx-pod 1/1 Running 1 3h18m

my-nginx-rc-65vtv 1/1 Running 0 2m26s

my-nginx-rc-7l7jd 1/1 Running 0 2m26s

my-nginx-rc-9m5rw 1/1 Running 0 2m26s

my-nginx-rc-d6n4c 1/1 Running 0 2m26s

my-nginx-rc-f6sf5 1/1 Running 0 2m26s

my-nginx-rc-m62lf 1/1 Running 0 2m26s

my-nginx-rc-m8zw7 1/1 Running 0 2m26s

my-nginx-rc-mmp4r 1/1 Running 0 2m26s

my-nginx-rc-og-22lhb 1/1 Running 0 103s

my-nginx-rc-og-5kzx5 1/1 Running 0 103s

my-nginx-rc-og-7dzq2 1/1 Running 0 103s

my-nginx-rc-og-7jvxp 1/1 Running 0 103s

my-nginx-rc-og-8pv77 1/1 Running 0 103s

my-nginx-rc-og-9gs6w 1/1 Running 0 103s

my-nginx-rc-og-c7vc5 1/1 Running 0 103s

my-nginx-rc-og-lchvp 1/1 Running 0 103s

my-nginx-rc-og-ml85r 1/1 Running 0 103s

my-nginx-rc-og-wbcnm 1/1 Running 0 103s

my-nginx-rc-v8fmm 1/1 Running 0 2m26s

my-nginx-rc-vbpgd 1/1 Running 0 2m26s

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

NAME DESIRED CURRENT READY AGE

my-nginx-rc 10 10 10 106m

my-nginx-rc-og 10 10 10 4m59s

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_service.yml

error: error parsing nginx_service.yml: error converting YAML to JSON:
yaml: line 4: found character that cannot start any token

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_service.yml

error: error parsing nginx_service.yml: error converting YAML to JSON:
yaml: line 4: found character that cannot start any token

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_service.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_service.yml

error: error parsing nginx_service.yml: error converting YAML to JSON:
yaml: line 4: found character that cannot start any token

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_service.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_service.yml

service/my-nginx-service created

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get svc

NAME TYPE CLUSTER-IP EXTERNAL-IP PORT(S) AGE

kubernetes ClusterIP 10.96.0.1 \<none> 443/TCP 3h50m

my-nginx-service NodePort 10.111.77.115 \<none> 80:32704/TCP 46s

**rhyme@ip-10-199-80-63:\~/**yml$ ifconfig

docker0: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet 172.17.0.1 netmask 255.255.0.0 broadcast 172.17.255.255

inet6 fe80::42:29ff:feb5:510b prefixlen 64 scopeid 0x20\<link>

ether 02:42:29:b5:51:0b txqueuelen 0 (Ethernet)

RX packets 11162 bytes 772500 (772.5 KB)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 11994 bytes 3660612 (3.6 MB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

ens5: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 9001

inet 10.199.80.63 netmask 255.255.128.0 broadcast 10.199.127.255

inet6 fe80::869:d6ff:fe73:de37 prefixlen 64 scopeid 0x20\<link>

ether 0a:69:d6:73:de:37 txqueuelen 1000 (Ethernet)

RX packets 61793 bytes 68221636 (68.2 MB)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 19107 bytes 6409070 (6.4 MB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

lo: flags=73\<UP,LOOPBACK,RUNNING> mtu 65536

inet 127.0.0.1 netmask 255.0.0.0

inet6 ::1 prefixlen 128 scopeid 0x10\<host>

loop txqueuelen 1000 (Local Loopback)

RX packets 309851 bytes 65512221 (65.5 MB)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 309851 bytes 65512221 (65.5 MB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth017324e: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::ac73:32ff:fe50:9275 prefixlen 64 scopeid 0x20\<link>

ether ae:73:32:50:92:75 txqueuelen 0 (Ethernet)

RX packets 5585 bytes 464596 (464.5 KB)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 6036 bytes 1834168 (1.8 MB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth01f3009: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::9c18:39ff:fe42:69ef prefixlen 64 scopeid 0x20\<link>

ether 9e:18:39:42:69:ef txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth0609de2: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::707c:2dff:fe85:7c2 prefixlen 64 scopeid 0x20\<link>

ether 72:7c:2d:85:07:c2 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth08b39d2: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::88ea:e5ff:fe01:5467 prefixlen 64 scopeid 0x20\<link>

ether 8a:ea:e5:01:54:67 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 40 bytes 4378 (4.3 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth0cd961e: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::84cf:72ff:fe05:9c00 prefixlen 64 scopeid 0x20\<link>

ether 86:cf:72:05:9c:00 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth0f496bb: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::ec65:67ff:fe96:5526 prefixlen 64 scopeid 0x20\<link>

ether ee:65:67:96:55:26 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth161f331: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::2843:45ff:feff:b47e prefixlen 64 scopeid 0x20\<link>

ether 2a:43:45:ff:b4:7e txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 65 bytes 6711 (6.7 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth2a300d6: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::681e:eff:fe95:999a prefixlen 64 scopeid 0x20\<link>

ether 6a:1e:0e:95:99:9a txqueuelen 0 (Ethernet)

RX packets 5577 bytes 464172 (464.1 KB)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 6031 bytes 1833371 (1.8 MB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth37c0f43: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::acec:9ff:fec5:dbdf prefixlen 64 scopeid 0x20\<link>

ether ae:ec:09:c5:db:df txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth3c0b8c1: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::7819:3cff:fece:d852 prefixlen 64 scopeid 0x20\<link>

ether 7a:19:3c:ce:d8:52 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth40d45ce: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::42e:acff:fe3a:4a79 prefixlen 64 scopeid 0x20\<link>

ether 06:2e:ac:3a:4a:79 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 40 bytes 4378 (4.3 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth6044fa0: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::14c1:60ff:fe16:f397 prefixlen 64 scopeid 0x20\<link>

ether 16:c1:60:16:f3:97 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth6cd0098: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::49a:c6ff:fee6:79eb prefixlen 64 scopeid 0x20\<link>

inet6 fe80::49a:c6ff:fee6:79eb prefixlen 64 scopeid 0x20\<link>

ether 06:9a:c6:e6:79:eb txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth7c07263: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::886a:bff:fe22:d9a8 prefixlen 64 scopeid 0x20\<link>

ether 8a:6a:0b:22:d9:a8 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth915b63e: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::f847:d1ff:fe6e:710e prefixlen 64 scopeid 0x20\<link>

ether fa:47:d1:6e:71:0e txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

veth91cbedf: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::8878:c1ff:fef0:fd6b prefixlen 64 scopeid 0x20\<link>

ether 8a:78:c1:f0:fd:6b txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vetha646a95: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::a811:a1ff:fe3c:df1a prefixlen 64 scopeid 0x20\<link>

ether aa:11:a1:3c:df:1a txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vetha87c934: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::5058:9fff:fe72:a434 prefixlen 64 scopeid 0x20\<link>

ether 52:58:9f:72:a4:34 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 40 bytes 4378 (4.3 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vethb2ad901: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::c43e:c0ff:feac:2f73 prefixlen 64 scopeid 0x20\<link>

ether c6:3e:c0:ac:2f:73 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vethba0cc02: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::2c69:95ff:fefe:d812 prefixlen 64 scopeid 0x20\<link>

ether 2e:69:95:fe:d8:12 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vethc595252: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::8fb:4ff:fe2d:f42e prefixlen 64 scopeid 0x20\<link>

ether 0a:fb:04:2d:f4:2e txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vethd47e359: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::c47f:5ff:fe09:4a38 prefixlen 64 scopeid 0x20\<link>

ether c6:7f:05:09:4a:38 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

vethdfed7ec: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST> mtu 1500

inet6 fe80::ac9f:5eff:fe1a:2c92 prefixlen 64 scopeid 0x20\<link>

ether ae:9f:5e:1a:2c:92 txqueuelen 0 (Ethernet)

RX packets 0 bytes 0 (0.0 B)

RX errors 0 dropped 0 overruns 0 frame 0

TX packets 41 bytes 4448 (4.4 KB)

TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

**rhyme@ip-10-199-80-63:\~/**yml$

**rhyme@ip-10-199-80-63:\~/**yml$ ipconfig

Command 'ipconfig' not found, did you mean:

command 'iwconfig' from deb wireless-tools

command 'ifconfig' from deb net-tools

command 'iconfig' from deb ipmiutil

Try: sudo apt install \<deb name>

**rhyme@ip-10-199-80-63:\~/**yml$

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_deployment

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_deployment.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_deployment.yml

deployment.apps/nginx-deployment created

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get deployment

NAME READY UP-TO-DATE AVAILABLE AGE

nginx-deployment 5/5 5 5 30s

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_service.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_service.yml

service/my-nginx-service configured

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get svc

NAME TYPE CLUSTER-IP EXTERNAL-IP PORT(S) AGE

kubernetes ClusterIP 10.96.0.1 \<none> 443/TCP 4h30m

my-nginx-service NodePort 10.111.77.115 \<none> 80:32704/TCP 40m

**rhyme@ip-10-199-80-63:\~/**yml$ vi nginx_deployment.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_deployment.yml

deployment.apps/nginx-deployment configured

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_deployment.yml

deployment.apps/nginx-deployment configured

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f
nginx_deployment.yml

deployment.apps/nginx-deployment configured

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl rollout history deploy
nginx-deployment

deployment.extensions/nginx-deployment

REVISION CHANGE-CAUSE

1 \<none>

2 \<none>

3 \<none>

4 \<none>

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl rollout undo deploy
nginx-deployment --to-revision=1

missed out cmds:

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f nginx_pod.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get pods

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl apply -f nfinx_rc.yml

**rhyme@ip-10-199-80-63:\~/**yml$ sudo kubectl get rc

**rhyme@ip-10-199-80-63:\~/**yml$sudo kubectl get pods -l app=nginx

**rhyme@ip-10-199-80-63:\~/**yml$sudo kubectl delete pods -l app=nginx
