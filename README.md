# ansible

Подсказки по использованию ansible-playbook

### Предварительная настройка для запуска playbooks

Для запуска необходимо создать 3 виртуальные машины (в моём случае VirtualBox, но можно использовать KVM и т.д.):
centos - 2 
ubuntu - 1

На всех linux машинах создайте одного и того же пользователя (в моём случае пользователь sanya)
Добавьте в группу sudoer и на время выполнения инсталляций с помощью ansible-playbook отключить необходимость вводить пароль

Экспортируйте публичный ключ со своей linux машины:

`ssh-copy-id username@remote_host`

В файле ansible-m-setup-all описана конфигурация виртуальных машин полученная командой:
ansible -m setup all

### Запуск playbooks

Запуск playbooks выполняется командой  ansible-playbook, например:
`ansible-playbook playbook1_ping.yml`

Для запуска playbook7_ext_vars.yml и playbook11_ansible-vault.yml созданы отдельные файлы запуска 
run-extra-vars.sh и run-ansible-vault.sh для передачи внешних переменных или параметров.




