# SSH Config in Cisco
## Switch Config
> aaa new-model \
> username alireza password 0 alireza \
> enable password alireza \
> line vty 0 4 \
> transport input all \
> exit \
> ip domain-name test \
> crypto key generate rsa \
> ip ssh version 2

## Client Config
Edit ~/.ssh/config
Add below lines
> Ciphers +aes128-cbc,aes256-cbc,3des-cbc \
> KexAlgorithms +diffie-hellman-group14-sha1 \
> HostkeyAlgorithms +ssh-rsa \
> #If you authenticate using a keypair: \
> PubkeyAcceptedAlgorithms +ssh-rsa
