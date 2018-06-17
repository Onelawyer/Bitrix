## getHighloadElements()

Сниппит получает список элементов highload-блока.

```php
$arElements = getHighloadElements(
    'tableName', // string название таблицы
    [ // array (необязательный)
        'order' => 'desc' // string ASC|DESC направление сортировки
        'limit' => // int количество возвращаемых элементов
        'filter' => ['=ID' => 5] // array массив фильтров выборки
        'select' => ['ID', 'UF_NAME'] // array возвращаемый массив полей элемента
    ]
);
```

При успешной отработке возвращает – **массив элементов highload-блока** в другом случае – **пустой массив**.

## updateHighloadElement()

Сниппет обновляет значения полей highload-блока.

```php
$bUpdate = updateHighloadElement(
    'tableName', // string название таблицы
    5, // int ID элемента
    [ // array массив обновляемых полей со значениями
        'UF_NAME' => 'Новое имя'
    ]
);
```

При успешной отработке возвращает – **true** в другом случае – **false**.