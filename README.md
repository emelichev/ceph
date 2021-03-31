# ceph
ceph обновление в пределах релиза

watch -n0 ceph -s
Проверяем что статус OK и нет никаких операций восстановления
ceph version
ceph tell osd.* version


yum update ceph-* -y

1. Шаг systemctl restart ceph-mon.target на каждой ноде
2. Шаг systemctl restart ceph-mgr.target   на каждой ноде
3. Шаг. systemctl restart ceph-osd.target  на каждой ноде
4. Шаг systemctl status ceph-radosgw.target  на каждой ноде
ceph version
ceph tell osd.* version

Можно использовать playbook ansible для массового запуска каждой команды
