> s3也可以当做一个文件系统来使用
```sh
sudo amazon-linux-extras install epel -y
sudo yum install -y s3fs-fuse
echo 'aws_access_key_id:aws_secret_access_key' > ~/.passwd-s3fs
chmod 600 ~/.passwd-s3fs
mkdir -p ~/Mountdir
s3fs Mountdir_s3  ~/Mountdir  -o passwd_file =  ~/.passwd-s3fs
```