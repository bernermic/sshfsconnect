# sshfsmanager
Utility for mounting / unmounting a remote filesystem via ssh. It will show you a simple dialogue window with your configured hosts in `~/.ssh/config` to connect to.  
If already connected script will unmount the selected host mount.
* run command `wget -O ~/.local/bin/sshfsmanager https://raw.githubusercontent.com/bernermic/sshfsmanager/master/sshfsmanager` this simply downloads the script and places `sshfsmanager` into `~/.local/bin/`
* from CLI call `sshfsmanager`
* follow instructions from there

## Install
The script will check this preconditions and tell you if it missing something.
* assumes generated ssh-key `~/.ssh/id_rsa` is imported on remote host
* assumes ssh Host config `~/.ssh/config` is given


## Example config
### ssh key
For better security it is recommended to set up and use an ssh key `~/.ssh/id_rsa` for authentication.  
[Read how to generate an SSH key](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/).
### ssh config
Disclaimer: this is just a example `~/.ssh/config` replace *example* with your domain/user. 
```
 Host example
      Hostname example.com
      User example
      IdentityFile ~/.ssh/id_rsa
      Ciphers aes128-gcm@openssh.com,aes256-gcm@openssh.com,chacha20-poly1305@openssh.com,aes256-ctr,aes192-ctr,aes128-ctr
      Compression yes
```

Further info [see SSH config](https://linuxize.com/post/using-the-ssh-config-file/). 