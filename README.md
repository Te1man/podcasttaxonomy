# Словарь подкастинга — таксономия ролей

Открытая таксономия ролей производства подкастов для русскоязычной индустрии: названия, группы и описания в машиночитаемом JSON.

Совместима по духу с международным стандартом [Podcast Taxonomy](https://github.com/podcasttaxonomy/podcasttaxonomy): общий язык для кредитов, вакансий и продуктов в подкастинге.

## Цели

1. Дать студиям, сетям и независимым авторам общий список ролей и должностных описаний.
2. Упростить поиск работы и найм в подкастинге за счёт единых названий (RU + EN).
3. Держать таксономию живой: обновления через вклад сообщества.

## JSON

Файл `taxonomies/creator-roles.json` — массив объектов, каждый из которых описывает одну роль.

### Поля

- `positionTitle` — название роли на русском
- `code` — стабильный идентификатор (camelCase)
- `groupName` / `groupNameEn` — группа ролей (RU / EN)
- `enLabel` — английское название
- `description` — краткое описание обязанностей
- `example` — пример (если есть)
- `aliases` — синонимы и альтернативные названия

### Пример

```json
[
  {
    "positionTitle": "Исполнительный продюсер",
    "code": "executiveProducer",
    "groupName": "Продюсирование",
    "groupNameEn": "Producing",
    "enLabel": "Executive Producer",
    "description": "Исполнительный продюсер — главный продюсер проекта…",
    "example": "",
    "aliases": ["Executive Producer", "EP"]
  }
]
```

### Как использовать

Скопируйте JSON в своё приложение или сайт, либо подключайте напрямую по URL (обязательно кэшируйте у себя на разумный срок):

https://raw.githubusercontent.com/Te1man/podcasttaxonomy/main/taxonomies/creator-roles.json

```js
const res = await fetch(
  'https://raw.githubusercontent.com/Te1man/podcasttaxonomy/main/taxonomies/creator-roles.json'
);
const roles = await res.json();
```

## Лицензия

Тексты таксономии — [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).  
При использовании указывайте атрибуцию: «Словарь подкастинга».
