# Ubuntu Cloud Images on VirtualBox

[Ubuntu Cloud Images](https://cloud-images.ubuntu.com/)

```shell
sudo apt-get install cloud-image-utils
```

```shell
cat >user-data <<EOF
#cloud-config
password: ubuntu
chpasswd: { expire: False }
ssh_pwauth: True
EOF
```

```shell
cloud-localds user-data.iso user-data
```

![](https://raw.githubusercontent.com/kelude/ubuntu-cloud-images-on-virtualbox/main/captures/capture-0.png)

and now you can login with:

- username: `ubuntu`
- password: `ubuntu`

![](https://raw.githubusercontent.com/kelude/ubuntu-cloud-images-on-virtualbox/main/captures/capture-2.png)
