# getComparison

Сниппет для вывода ссылки на имеющееся сравнение товаров в любом месте. Например, в шапке сайта.

## Параметры

| Название  | По умолчанию       | Описание                             |
| --------- | ------------------ | ------------------------------------ |
| **&list** | default            | Имя существующего списка сравнения.  |
| **&tpl**  | tpl.Comparison.get | Чанк оформления ссылки на сравнение. |

## Вызов на странице

Обычный вызов, с параметрами по умолчанию:

```php
[[!getComparison]]
```

[![](https://file.modx.pro/files/4/e/b/4ebd312439d1736e182fc3ff495dbcd6s.jpg)](https://file.modx.pro/files/4/e/b/4ebd312439d1736e182fc3ff495dbcd6.png)

## Логика работы

Сниппет запрашивает список сравнения из сессии пользователя и выводит ссылку на страницу, указанную как `list_id` при вызове [addComparison][0].

Чанк по умолчанию cодержит такие классы, чтобы реагировать на ajax события при работе со списком на странице.
Например, если **getComparison** вызван в шапке сайта, а ниже у вас идёт вывод каталога, то при добавлении\удалении товаров в избранном, значения ссылки в шапке будут меняться соответственно.

На странице сравнения, где у вас должен быть вызван [CompareList][1] для этого списка, ссылка не выводится.

[0]: /ru/01_Компоненты/12_Comparison/01_addComparison.md
[1]: /ru/01_Компоненты/12_Comparison/02_CompareList.md
