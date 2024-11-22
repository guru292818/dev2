sshfs:

apt install sshfs

sudo sshfs -o IdentityFile=/root/.ssh/id_ed25519 root@164.52.194.92:/data /mnt/remote_data -o allow_other

To persist:
------------

cat /etc/rc.local 
#!/bin/bash
# rc.local

# Mount the remote SSHFS filesystem (replace with your own command)
sudo sshfs -o IdentityFile=/root/.ssh/id_ed25519 root@164.52.194.92:/data /mnt/remote_data -o allow_other

exit 0

