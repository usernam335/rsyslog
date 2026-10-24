# RSYSLOG
## Структура каталога 

 rsyslog  
   ├── ansible-playbook.yml  
   ├── inventory.ini   
   └── Vagrantfile  


## Описание домашнего задания:

1. Поднимаем две машины — web и log.
2. На web поднимаем nginx.
3. Настраиваем центральный лог-сервер на любой системе по выбору:
   - journald;
   - rsyslog;
   - elk.

4. Настраиваем аудит, который будет отслеживать изменения конфигураций nginx.
   - Все критичные логи с web должны собираться и локально и удаленно.    
   - Bсе логи с nginx должны уходить на удаленный сервер (локально только критичные).
   - Логи аудита должны также уходить на удаленную систему

## Поднимаем две машины — web и log.

1. Переходим в каталог с [Vagrantfile](https://github.com/usernam335/rsyslog/blob/main/rsyslog/Vagrantfile) и запускаем его.

       cd /path/to/rsyslog
____________________________________________
       vagrant up

2. Для настройки я выбрал rsyslog. Все настройки прописаны в [ansible-playbook](https://github.com/usernam335/rsyslog/blob/main/rsyslog/ansible-playbook.yml). Playbook запускается из Vagrantfile.

<img width="1908" height="355" alt="Снимок экрана от 2026-10-24 12-01-57" src="https://github.com/user-attachments/assets/34be2961-5dc8-406c-bf19-634ccd8d5e68" />


