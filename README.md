
#### rsync
-- install rsync
```
brew install rsync
```

-- key
```
ssh-keygen

ssh-copy-id ec2-user@ec2-18-223-133-30.us-east-2.compute.amazonaws.com

```
https://www.youtube.com/watch?v=S5B09dq-jGQ


-- mount
```
rsync -av — progress -e “ssh -i /path_to/your_public_key.pem/” 
/absolute_path_to/local_files/ remote_server_root@public_DNS:/absolut_path/remote_directory_destination

rsync -av — progress -e "ssh -i /Users/h/kindom/perm.pem" /Users/h/share/ ec2-user@ec2-18-223-133-30.us-east-2.compute.amazonaws.com:/home/ec2-user/share/
ssh -i "perm.pem" ec2-user@ec2-18-223-133-30.us-east-2.compute.amazonaws.com
```


##### install in amazon linux
```
-- install
https://superuser.com/questions/1567828/how-to-install-sshfs-in-centos-8-from-repository-using-package-manager-tool

-- usage
sshfs ubuntu@ec2-ip-address:/home/ubuntu/aws_share /home/yourname/local_folder -o IdentityFile=~/your-pemfile.pem -o allow_other

sshfs ec2-user@ec2-18-223-133-30.us-east-2.compute.amazonaws.com:/home/ec2-user/share ~/Users/h/share -o IdentityFile=~/Users/h/kindom/perm.pem -o allow_other


```






##### download
https://osxfuse.github.io/



##### public-key
https://serverpilot.io/docs/how-to-use-ssh-public-key-authentication/
