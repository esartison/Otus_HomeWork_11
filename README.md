# Домашнее задание Сартисона Евгения №11

Задание
```
☁️ Вариант 2. HA-кластер в облаке
Разверните кластер PostgreSQL с высокой доступностью с использованием одного из облаков, например:
Yandex Managed Service for PostgreSQL (если нужна управляемая БД)
Развертывание вручную в Yandex Cloud Compute
VK Cloud, Timeweb Cloud, Selectel, ROSA Cloud и др.
```
Времение не очень много и кое-что уже делали до этого. Решил размернуть Postgres HA кластер в VK Cloud.

## **(1) Создать кластек через GUI**

- Выбрать Postgres 17 с конфигурацией Мультизональный кластер
<img width="1229" height="920" alt="image" src="https://github.com/user-attachments/assets/5ed7b27e-7141-4f7a-8c45-85326512b617" />

- Установить кол-во синхронных и асинхронным реплик
<img width="1285" height="470" alt="image" src="https://github.com/user-attachments/assets/f2043a5c-bc30-4fbb-bd6d-2eb7177eeb47" />


кластер создался
<img width="1224" height="516" alt="image" src="https://github.com/user-attachments/assets/4e6259da-f46f-4e11-a437-000e5286b9b8" />




## **(2) Убедиться что кластер находится в разных зонах доступности**

Мастер 

<img width="1085" height="598" alt="image" src="https://github.com/user-attachments/assets/fb87e126-53a1-4a47-a7d2-42c527e3af34" />

Sync реплика

<img width="1156" height="577" alt="image" src="https://github.com/user-attachments/assets/05f80414-5f9d-43b8-8c45-464686657389" />

Async реплика

<img width="1100" height="580" alt="image" src="https://github.com/user-attachments/assets/cebd232b-feff-453e-be0d-b4c2f05ae056" />




## **(3) Сделать переключение**

Выбираем Sync Replica в другой зоне доступности и делаем переключение

<img width="1563" height="602" alt="image" src="https://github.com/user-attachments/assets/50d238b0-55ff-461f-a84f-0a124c844797" />

<img width="537" height="238" alt="image" src="https://github.com/user-attachments/assets/57f33ab5-cdb4-41bb-8565-14b38573660f" />

Мастер переключился

<img width="1253" height="531" alt="image" src="https://github.com/user-attachments/assets/41dd65cd-5b52-44b1-a9c5-20e91205134a" />



