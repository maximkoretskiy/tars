# Handlebars-helpers


## repeat

Используется для создания простого цикла от 0 до n (цикл для обхода массива данных есть в handlebars по-умолчанию).

Синтаксис:

```handlebars
{{#repeat n}}
    Do something
{{/repeat}}
```

n — количество повторений. Number, целое.


## is

Используется для расширения стандартного if. Встроенный if умеет проверять только существует значение или нет. #is позволяет использовать стандартное поведение if. Операция сравнения передается в виде строки вторым аргументом. 1 и 3 передаются значения для сравнения. Доступны следующие операции (все операции выполняются в JavsScript, соотвественно и результат сравнения получается таким же, как если бы это был if внутри js):

* `==` Нестрогое равно.
* `===` Строгое равно.
* `>` Строго больше.
* `>=` Больше или равно.
* `<` Строго меньше.
* `<=` Меньше или равно.

test — переменная, переданная в шаблон

```js
testModule: {
    test: 10
}
```

Синтаксис:

```handlebars
{{#is test '>' 9}}
    true
{{else}}
    false
{{/is}}
```


## strip

Вырезает все пробелы из переданного контента.

Синтаксис:

```handlebars
<style>
    ul li {
        display: inline-block;
    }
</style>

{{#strip}}
    <ul>
        <li>qwe</li>
        <li>asd</li>
    </ul>
{{/strip}}
```

Результат:

```html
<ul><li>qwe</li><li>asd</li></ul>
```


## toLowerCase

Перевод переданной строки в нижний регистр.

Синтаксис:

```handlebars
{{toLowerCase 'string'}}
```


## toUpperCase

Перевод переданной строки в верхний регистр.

Синтаксис:

```handlebars
{{toUpperCase 'string'}}
```


## capitalizeFirst

Перевод первого символа переданной строки в верхний регистр.

Синтаксис:

```handlebars
{{capitalizeFirst 'string'}}
```
