## Что надо сделать
Возьмите Postgres версии 8.4 и попробуйте установить, используя Vagrant. В результате у вас получится vagrant box или Vagrantfile. Первый можно залить на любой файл-хостинг и расшарить ссылку менторам курса, а второй — разместить в своём github-репозитории sf__legacy_vagrant.
----
![Снимок экрана от 2023-07-05 18-13-29](https://github.com/DjHelkern/sf__legacy_vagrant/assets/80486143/655de3cc-92cc-4db1-b3bc-18edb2b6be10)
----

Запустете виртуальную машину с помощью vagrant up

Создайте vagrant box из виртуальной машины с помощью vagrant package:

vagrant package --base my-box.box --output my-box.box

Пример (vagrant package --base postgresql_postgresql-8-4_1688644604277_18619 --output my-box.box)

----
Добавьте созданный vagrant box в локальный репозиторий с помощью vagrant box add:

vagrant box add my-box.box --name my-box.box

Проверьте, что ваш новый vagrant box находится в локальном репозитории с помощью vagrant box list:

vagrant box list

![Снимок экрана от 2023-07-06 17-22-46](https://github.com/DjHelkern/sf__legacy_vagrant/assets/80486143/18a66d24-bce0-4af9-98ac-1df0488f3a1d)
