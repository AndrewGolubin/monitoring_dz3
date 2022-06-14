Для успешного выполнения ДЗ вам необходимо:

1. Уустановить ELK (elasticsearch, logstash, kibana). Базовая операционная система - по вашему выбору.

2. После успешной установки ELK-стека вам необходимо настроить отправку логов sshd в elasticsearch через logstash. Для этого вам придется изменить настройку rsyslog. Проверьте создался ли index в elasticsearch.

3. После настройки отправки логов в ELK попробуйте настроить визуализацию логов от sshd в kibana.

Отчет:

1. В дополнение к инфраструктуре https://github.com/AndrewGolubin/monitoring_dz1 и https://github.com/AndrewGolubin/monitoring_dz2, в среде vmware, поднята ВМ Virt1 (192.168.12.178), в среде ВМ 
