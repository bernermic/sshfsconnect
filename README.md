# sshfsconnect
Utility for connecting a remote filesystem via ssh. It will show you a simple dialogue window with your configured servers to connect to.
* simply place `sshfsconnect` into `~/.local/bin/`
* from CLI call `sshfsconnect`
* follow instructions from there

## Install
The script will check this preconditions and tell you if it missing something.
* assumes generated ssh-key `~/.ssh/id_rsa` is available on remote server
  * otherwise you have to enter the user's password on connect
* assumes ssh Host config `~/.ssh/config` is given


## Example config
### ssh key
For better security it is recommended to set up and use an ssh key `~/.ssh/id_rsa` for authentication: [see generate key](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/).
### ssh config
Disclaimer: this is just a example `~/.ssh/config` replace *example* with your domain/user. 

Further info [see SSH config](https://linuxize.com/post/using-the-ssh-config-file/). 
```
 Host example
      Hostname example.com
      User example
      IdentityFile ~/.ssh/id_rsa
      Ciphers aes128-gcm@openssh.com,aes256-gcm@openssh.com,chacha20-poly1305@openssh.com,aes256-ctr,aes192-ctr,aes128-ctr
      Compression yes
```
