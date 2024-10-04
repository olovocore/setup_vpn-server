# Common Info
Данные плейбуки необходимы для настройки SSH, iptables, создания пользователя и запуска WireGuard с GUI.
# Запустить
>ansible-playbook user.yml && ansible-playbook wg.yml && ansible-playbook ssh_iptables.yml
# ENVs
[my_servers:vars]<br>
wireguard_host_ip=ip_server<br>
wireguard_admin_password=password<br>
wireguard_port_tcp=55556<br>
wireguard_port_udp=55555<br>
username=user_server<br>
ssh_key="{{ lookup('file', '/home/user/.ssh/id_rsa.pub') }}"<br>
ssh_port=8888<br>
password_username="{{ 'password' | password_hash('sha512') }}"<br>