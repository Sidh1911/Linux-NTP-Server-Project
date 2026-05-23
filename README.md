# Linux-NTP-Server-Project
Configured and managed Network Time Protocol (NTP) services to synchronize date and time between server and client systems in a Linux environment.


HOW TO CONFIGURE NTP ?      
# dnf install chrony -y 
# vim /etc/chrony.conf  
allow 192.168.0.0/24   26 line           
local stratum 10      29 line               
:wq 
# systemctl restart chronyd 
# systemctl enable chronyd 
# firewall-cmd --permanent --add-service=ntp 
# firewall-cmd –reload 

### Go to Client site ### 
# vim /etc/chrony.conf 
Comment the line number 3 starting with pool 
# pool 2.rhel………………..  iburst 
server 192.168.0.254 iburst           
:wq 
# systemctl restart chronyd 
# systemctl enable chronyd 
# timedatectl        
# chronyc sources                              


![image alt](https://github.com/Sidh1911/Linux-NTP-Server-Project/blob/59eff964d1e85c7efb41e956a810a7df5116fd66/6093565678649544614.jpg)

192.168.0.254 is a server ip
