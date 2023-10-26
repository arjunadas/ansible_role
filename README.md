# ansible_role

inst-soft.yaml - устанавливает Nginx + Docker

deploy.yaml - поднимает докер контейнер рядом с существующим, если получает http code 200, переглючает трафиик в nginx на новый контейнер


для запуска:

git clone https://github.com/arjunadas/ansible_role.git

cd ansible_role

ansible-galaxy collection install community.general # для отправки уведомлений в Телеграм

ansible-playbook deploy.yaml --extra-vars "ansible_sudo_pass= ************************** " --extra-vars "ansible_ssh_pass= ************************** "

curl -o /dev/null -s -w "%{http_code}\n" http://185.98.82.78
