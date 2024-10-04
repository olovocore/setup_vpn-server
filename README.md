# Common Info
Данные плейбуки необходимы для настройки SSH, iptables, создания пользователя и запуска WireGuard с GUI.
# Запустить
>ansible-playbook user.yml && ansible-playbook wg.yml && ansible-playbook ssh_iptables.yml
