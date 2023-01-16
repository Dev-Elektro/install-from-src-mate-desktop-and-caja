# install-from-src-mate-desktop-and-caja

Установка из исходников mate-desktop и caja под РЕД ОС 7.3 при помощи Ansible

## Инструкция по использованию

В inventory файл `ansible/hosts` указать имя ПК который вводится в домен.

    my-new-pc01

Для подключения к ПК с определенным именем пользователем:

    my-new-pc01 ansible_user=root

## Запуск playbook
Для запуска необходимо передать extra-vars `target` с указанием ПК который вводится в домен.

    ansible]$ ansible-playbook playbooks/install-from-src-mate-desktop-and-caja.yml --extra-vars "target=my-new-pc01"

если требуется пароль для sudo:

    ansible]$ ansible-playbook playbooks/install-from-src-mate-desktop-and-caja.yml --extra-vars "target=my-new-pc01" --ask-become-pass
