###  一行命令启动一个qemu虚拟机
`qemu-system-x86_64 -machine q35 -m 1024 -smp cpus=2 -cpu qemu64 -drive if=pflash,format=raw,read-only=on,file=/usr/share/OVMF/OVMF_CODE.fd -netdev user,id=n1,net=10.33.0.0/24,dhcpstart=10.33.0.100,host=10.33.0.1,hostfwd=tcp::2322-:22 -device virtio-net,netdev=n1 -cdrom cloud_init.iso  -nographic client-jammy-2322.img`

> -machine q35 