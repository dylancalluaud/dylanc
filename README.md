# TP1

## First steps

La version de systemctl est 243.4.1.fc31

[admin@localhost ~]$ systemctl --version
systemd 243 (v243.4-1.fc31)
+PAM +AUDIT +SELINUX +IMA -APPARMOR +SMACK +SYSVINIT +UTMP +LIBCRYPTSETUP +GCRYPT +GNUTLS +ACL +XZ +LZ4 +SECCOMP +BLKID +ELFUTILS +KMOD +IDN2 -IDN +PCRE2 default-hierarchy=unified


Le PID de systemd est bien 1.
─init.scope
           │ └─1 /usr/lib/systemd/systemd --switched-root --system --deserialize 30
           
           
Pour lister tous les processus qui ne sont pas des processus Kernel, on peut utiliser la commande : 
ps --ppid 2 -p 2 --deselect 



[root@localhost admin]# ps --ppid 2 -p 2 --deselect
    PID TTY          TIME CMD
    
      1 ?        00:00:00 systemd
      
    631 ?        00:00:00 systemd-journal
    
    647 ?        00:00:00 systemd-udevd
    
    736 ?        00:00:00 auditd
    
    738 ?        00:00:00 sedispatch
    
    767 ?        00:00:00 ModemManager
    
    769 ?        00:00:00 bluetoothd
    
    772 ?        00:00:00 firewalld
    



Par exemple : 
Firewalld : est le processus qui gère le pare-feu du système.
bluetoohhd : est le processus qui gère les connexions/carte bluetooth 
...
