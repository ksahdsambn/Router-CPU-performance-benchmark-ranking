
测试路由器性能的跑分脚本（该脚本用于测试aes-128-gcm，代表你的路由器科学上网的性能）
SSH进路由器，然后以root权限执行下列脚本，然后等待跑分完成即可

单核跑分（single core）
openssl speed -evp aes-128-gcm

多核跑分(multi core)
openssl speed -multi $(cat /proc/cpuinfo |grep processor | wc -l) -evp aes-128-gcm
