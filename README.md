# Screnshot composer.json
![Screnshot 1](/src/public/ScreenshotComposerJson.png "Скриншот файла composer.json")

## composer.json
    {
        "name": "andrei/composer",
        "description": "\"Домашнее задание по Composer\"",
        "require-dev": {
            "psr/log": "^3.0"
        },
        "autoload": {
            "psr-4": {
                "Andrei\\Composer\\": "src/"
            }
        },
        "authors": [
            {
                "name": "andrei ivanov"
            }
        ],
        "minimum-stability": "stable",
        "require": {}
    }

# Ответы на вопросы

1. Файл **composer.lock** содержит информацию какие именно точные версии зависимостей установлены и используются в проекте. Генерируется автоматически. В файле **composer.json** версии пакетов зачастую указаны "расплывчато" (нпр, выше такой-то или 1.1 вместо полной версии 1.1.7).
2. *require-dev* содержит зависимости, используемые **только** для разработки.
3. Команда **composer install** устанавливает все точные версии пакетов, которые указаны в файле **composer.lock** ничего не меняя, создает точную копию. Команда **composer update** обновляет версии пакетов на более новые, если позволяет  совместимость, обновляет **composer.lock**