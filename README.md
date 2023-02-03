Для успешного выполнения ДЗ вам необходимо:

1. Уустановить ELK (elasticsearch, logstash, kibana). Базовая операционная система - по вашему выбору.

2. После успешной установки ELK-стека вам необходимо настроить отправку логов sshd в elasticsearch через logstash. Для этого вам придется изменить настройку rsyslog. Проверьте создался ли index в elasticsearch.

3. После настройки отправки логов в ELK попробуйте настроить визуализацию логов от sshd в kibana.

Отчет:

1. В дополнение к инфраструктуре https://github.com/AndrewGolubin/monitoring_dz1 и https://github.com/AndrewGolubin/monitoring_dz2, в среде vmware, поднята ВМ Virt1 (192.168.12.178), в среде ВМ установлен docker, docker-compose, и поднят portainer для управления контейнерами. Доступ к общей консоли управления перенесен на Virt1.
2. На Virt1, в докере, развернут ELK-stack (elasticsearch, logstash, kibana). Конфигурационные файлы в каталоге ELK.
3. На хостах Virt1, Virt2 и WP-CLoud настроеен rsyslog, причем хосты Virt2 и WP-Сloud отправляют логи на хост Virt1. Дополнительно на хостах настроено логирование входа на все ВМ по ssh с использованием тэга tag_sshd_log. Логи входа по все хостам консолидируютя в отдельном файле на Virt1 (/var/log/rsyslog/sshd/sshd.log), который используется как источник данных для logstash. Конфигурационные файлы в каталоге rsyslog.  

Скрины - ниже

![image](https://user-images.githubusercontent.com/23739863/216607922-7ff135d8-2ab8-42aa-8fad-ac0ea473eaa1.png)

![image](https://user-images.githubusercontent.com/23739863/216606560-52c96670-19cf-4f1a-a5dc-42ce46961cb7.png)
