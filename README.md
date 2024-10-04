# Common Info
Данные плейбуки необходимы для настройки SSH, iptables, создания пользователя и запуска WireGuard с GUI.
# Запустить
>ansible-playbook user.yml && ansible-playbook wg.yml && ansible-playbook ssh_iptables.yml
# ENVs
[my_servers:vars]
wireguard_host_ip=ip_server
wireguard_admin_password=password
wireguard_port_tcp=55556
wireguard_port_udp=55555
username=user_server
ssh_key="{{ lookup('file', '/home/user/.ssh/id_rsa.pub') }}"
ssh_port=8888
password_username="{{ 'password' | password_hash('sha512') }}"