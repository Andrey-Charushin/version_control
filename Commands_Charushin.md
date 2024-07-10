# Основные команды для работы с GIT

### Инициализация репозитория в текущей директории (начало работы с GIT в текущей папке)

```sh
git init
```

### Просмотр статуса сохранения файлов в GIT

```sh
git status
```

### Добавление файла для внесения коммитов

```sh
git add <имя_файла>
```

### Создание коммита

```sh
git commit -m "комментарий к версии"
```

### Удаление внесённых изменений (возврат к последнему сохраненному коммиту)

```sh
git restore <имя_файла>
```

### Отображение истории коммитов

```sh
git log
```

#### *Отображение истории коммитов с ветвлением*

```sh
git log --graph
```

#### *Отображение истории коммитов в укороченном формате*

```sh
git log --oneline
```

#### *Отображение истории коммитов в укороченном формате с ветвлением*

```sh
git log --oneline --graph
```

### Переключение между коммитами

```sh
git checkout
```

## Работа с ветками

### Отображение всех веток

```sh
git branch
```

### Переключение между ветками

```sh
git checkout <имя_ветки>
```

### Создание новой ветки

```sh
git branch <имя_новой_ветки>
```

### Удаление ветки
```sh
git branch -d <имя_ветки>
```

## Работа с удаленными репозиториями

### Создание локальной копии удаленного репозитория

```sh
git clone <ссылка на удаленный репозиторий>
```

### Связь локального репозитория с удаленным

Обратите внимание, при первом подключению к удаленному репозиторию, необходимо авторизоваться

#### Подключение к удаленному репозиторию

```sh
git remote add <название для удаленного репозитория> <ссылка на заранее созданный удаленный репозиторий>
```

#### Объявление основной ветки

```sh
git branch -M <название ветки>
```

#### Отправка данных из локального репозитория в удаленный

```sh
git push
```

При отправке данных из ветки, отсутствующей в удаленном репозитории, используется следующая команда (один раз для каждой новой ветки):

```sh
git push --set-upstream <название репозитория> <название ветки>
```

#### Получение данных из удаленного репозитория в локальный с автоматическим слиянием

```sh
git pull
```

### Как сделать pull request (предложить свои изменения в репозиторий другого автора) на примере GitHub:

* Делаем fork репозитория
* Делаем clone СВОЕЙ версии репозитория
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull request 