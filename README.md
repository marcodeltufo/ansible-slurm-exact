# ansible-slurm
## Made for Ubuntu Server 20.04
### Operazioni preliminari
- aggiungere la chiave pubblica del controller ansible in /root/.ssh/authorized_keys sui managed nodes
#### Slurm controller:
- Popolare il file /etc/hosts con gli ip del controller e dei nodi
- ```PermitrootLogin yes``` in /etc/ssh/sshd_config
- ```$ systemctl restart sshd```
#### Slurm computing nodes:
- ```PermitrootLogin yes``` in /etc/ssh/sshd_config
- ```$ systemctl restart sshd```
- aggiungere la chiave pubblica dello slurm master in /root/.ssh/authorized_keys sui nodi

#### Playbook:
- modificare le opzioni dello slurm.conf a piacimento
- correggere gli hostname dove presenti
- modificare hosts.ini
