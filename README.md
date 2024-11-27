sshfs:

apt install sshfs

root@e2e-96-116:~# cat /etc/rc.local 
#!/bin/bash
# rc.local

# Wait for network to be ready
sleep 10

# Mount the remote SSHFS directory
sshfs -o IdentityFile=/root/.ssh/id_rsa root@164.52.197.217:/data /mnt/master_data -o allow_other


exit 0
