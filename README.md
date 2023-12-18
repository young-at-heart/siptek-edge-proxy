To install siptek-edge-proxy (only on debian 12)
1. intstall debian 12 minimal (select only standard system utilities) 
2. #apt install git
3. #git clone https://github.com/young-at-heart/siptek-edge-proxy.git
4. #cd siptek-edge-proxy
5. #chmod 744 install.py
6. #./install.py
7. #chmod 744 setup.py 
8. #./setup.py
9. #reboot

To use siptek-edge-proxy

IP-PBX ----- siptek-edge-proxy ----- internet router ----- the internet

1. internal nic of siptek-edge-proxy connects to IP-PBX (Asterisk, FreeSWITCH, etc.)
2. external nic of siptek-edge-proxy connects to internet router
3. internet service type is fixed public ip address
4. internet router must forward port 5060/udp and 10000-32768/udp to siptek-edge-proxy external nic
5. endpoints (ip phones, softphones, ATAs, etc.) can be on internal network (same network as siptek-edge-proxy internal nic) or on the internet or on other sites (behind NAT)
