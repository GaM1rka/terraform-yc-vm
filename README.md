## Terraform для автоматического создания VM на Yandex Cloud.
# Для работы с данным проектом нужно:
- Сгенерироваить ssh ключ на Yandex Cloud (https://center.yandex.cloud/organization -> Пользователи -> SSH-ключи -> Добавить ключ)
- Вставить в файле "meta.txt" в поле ssh_authorized_keys ваш публичный ключ.
- Ввести следующие команды:
``` bash
terraform init
terraform plan # для просмотра заданных конфигураций создания VM
terraform apply # запуск процесса создания VM
ssh {{name}}@ip-address -i {your private ssh key}
terraform destroy # удаляем VM при необходимости
```
