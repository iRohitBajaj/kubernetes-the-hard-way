## Few helpful commands to troubleshoot:  

### Checking service status  
systemctl list-unit-files | grep enabled  
systemctl | grep running  
systemctl -l status {service-name}  

### Checking service logs  
journalctl -u {service-name}  

### Stop and disable a service, for eg: kubelet  
{  
  sudo systemctl stop kubelet.service  
  sudo systemctl disable kubelet.service  
  sudo rm /etc/systemd/system/kubelet.service  
  sudo systemctl daemon-reload  
}  