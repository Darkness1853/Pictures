# Тестирование CLI
---
# Список команд

![img](https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202026-03-31%20105306.png?raw=true)
---
1. Создание контакта

![img1](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(10).jpg?raw=true)

в CLI программа позволяет ввести неверную дату 
2. Сортировка по ФИО

![img3](https://github.com/Darkness1853/Pictures/blob/main/TEST/image.png?raw=true)

3. Бинарный поиск

![img4](https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202026-03-31%20153053.png?raw=true)

4. Поиск в ДОП

![img5](https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202026-03-31%20153215.png?raw=true)

5. ДОП порядок обхода

![img6](https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202026-03-31%20153414.png?raw=true)

6. Обновление контакта

![img7](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(12).jpg?raw=true)

7. Удаление контакта

![img8](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(13).jpg?raw=true)

8. Добавление фото к контакту

![img9](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(14).jpg?raw=true)

9. Удаление фото

![img10](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(15).jpg?raw=true)

--- 
# Проблемы:

* Критичные

<video src="https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C%202026-03-31%20154909.mp4?raw=true" controls width="600"></video>

<video src="https://github.com/Darkness1853/Pictures/blob/main/TEST/%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C%202026-03-31%20154956.mp4" controls width="600"></video>

* Не критичные

Валидация даты

При тестировании поля ввода даты обнаружено, что бэкенд/логика приложения принимает даты, превышающие текущую

![img2](https://github.com/Darkness1853/Pictures/blob/main/TEST/image%20(11).jpg?raw=true)

Однако проблема не является критичным, так как:
Валидация корректно реализована на уровне графического интерфейса (GUI)
