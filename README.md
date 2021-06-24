# yii2_docker_start
1. Установить docker в систему
  1.1 Установить: docker
  1.2 Установить: docker-compose
  1.3 Если система позволяет установить kitematick (https://kitematic.com/ интерфейс для визуального администрирования контейнеров)
2. Склонировать файлы в ранее созданную директорию.
  2.1 Склонировать Framework yii2 advanced в папку www/advanced/
3. Пройти в директорию с файлом docker-compose.yml и выпонить из консоли "docker-compose up -d"
4. После открыть kitematick или выполнить в консоли "docker ps -a": эта команда покажет наличие созданных контейнеров.
5. Для установки composer зайти на контейнер php командой: docker exec -it <id контейнера> /bin/bash
6. В контейнере php запустить: curl -sS https://getcomposer.org/installer | php mv composer.phar /usr/local/bin/composer
7. Пройти в директорию в контейнере php: cd /var/www/advanced и выпонить "php init" после выбрать 0 и отвечать yes
8. Пройти в директорию в контейнере php: cd /var/www/advanced и выпонить "composer install"
9. На рабочей машине создать в директории cd /etc в файл hosts запись в конце с новой строки "127.0.0.1 frontend.dev" и следующей строкой "127.0.0.1 backend.dev"
10. В браузере открыть frontend.dev и увидеть страницую приветствия framework-а yii2 )

PS: если что-то пойдет не так, можно погуглить ;)
