# Домашнее задание к занятию ***«Кеширование Redis/memcached»***

---

### Задание 1. Кеширование 

Приведите примеры проблем, которые может решить кеширование. 
*Приведите ответ в свободной форме.*

---

**Решение**

1. Загрузка медиа-файлов: При кешировании медиа-файлов, таких как изображения, видео или аудио, пользователи могут получать быстрый доступ к этим файлам, без необходимости загружать их с сервера каждый раз. 
2. Запросы к базе данных: Кеширование запросов к базе данных может значительно уменьшить нагрузку на сервер и сократить время, необходимое для обработки запросов от пользователей.  
3. Динамические веб-страницы: Кеширование динамических веб-страниц может ускорить загрузку сайта для пользователей, так как они будут получать содержимое из кеша, а не каждый раз запрашивать его с сервера.  
4. API запросы: Кеширование API запросов может улучшить производительность приложений, позволяя им получать данные из кеша, вместо того чтобы делать запросы к удаленному серверу при каждом обновлении.  
5. Код и ресурсы: Кеширование файлов кода и ресурсов, таких как CSS, JavaScript и шрифты, может ускорить загрузку веб-страницы для пользователей, уменьшая время, необходимое для загрузки этих файлов с сервера.  

---

### Задание 2. Memcached

Установите и запустите memcached.

*Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.*

---

**Решение**

![image.jpg](https://github.com/Byzgaev-I/Redis-memcached/blob/main/2%20-%20start%20m.png)

---

### Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 
*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

---

**Решение**

Установили: 

```
sudo apt update && apt install memcached
```

Порт:

![image.jpg](https://github.com/Byzgaev-I/Redis-memcached/blob/main/2%20-%20port%20.png)

**подключаемся:**

```
 telnet localhost 11211
```

**вводим данные:**

```
set key flags exptime bytes <value>

```
**Скриншот выполнения команд:**

![image.jpeg](https://github.com/Byzgaev-I/Redis-memcached/blob/main/TTL.png)








