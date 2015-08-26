---

layout: default

---

# Яндекс

## **{{ site.presentation.title }}** {#cover}

<div class="s">
    <div class="service">{{ site.presentation.service }}</div>
</div>

{% if site.presentation.nda %}
<div class="nda"></div>
{% endif %}

<div class="info">
	<p class="author">{{ site.author.name }}, <br/> {{ site.author.position }}</p>
</div>

## &nbsp;
{:.section}

### БЭМ

## Для тех, кто ничего не знает про БЭМ
{:.code-with-text}

* [Начало](https://ru.bem.info/method/definitions/)
* [Вебинар с самых азов](https://ru.bem.info/talks/beminar-css-2015/)
* [Форум](https://ru.bem.info/forum/)

## БЭМ
{:.with-big-quote}

> Кроме блоков, элементов и модификаторов, есть ещё части...

[bem.info/method/definitions](https://ru.bem.info/method/definitions/)
{:.note}


## &nbsp;
{:.section}

### Разработка для нескольких платформ

## «Несколько платформ»

- Desktop
- Touch Pad
- Touch Phone

## Разработка для нескольких платформ

- Native
- Adaptive

## Нативная разработка

### Плюсы:

- пользовательский опыт близок к опыту с операционной системой
- можно учитывать особенности платформы (очень хорошо учитывать)
- сложные вещи работают быстро
- &nbsp;&hellip;

## Нативная разработка

### Минусы:

- дорого: разработка под iOS, Android и Windows Phone требует в три раза больше сил

## Адаптивный дизайн

### Плюсы:

- дешевле: один раз делаем — работает везде

## Адаптивный дизайн

### Минусы:

- сложность: нужно написать одно решение, которое работает очень разными способами
- не всегда возможно сделать сильно разное для разных платформ

## «Золотая середина»

### Плюсы:
- дёшево: используем общие части между разными платформами
- проще: не надо заставлять один код быть сильно полиморфным
- индивидуально для платформы

## «Золотая середина»

### Минусы:
- web-технологии&hellip;

## БЭМ
{:.section}

### Переопределения

## Переопределения
{:.code-with-text}

### CSS

~~~css
.button {
    border: 1px solid #666;
    font-size: 13px;
}
~~~

## Переопределения
{:.code-with-text}

Можем разложить на части:

- общее для всех платформ

~~~css
.button {
    border: 1px solid #666;
}
~~~

- специфичное для конкретной платформы

~~~css
.button {
    font-size: 13px;
}
~~~

## Уровни переопределения

- common
- desktop
- touch
- touch-pad
- touch-phone
- deskpad?

## Уровни переопределения
{:.code-with-text}

common.blocks/button/button.css

~~~css
.button { border: 1px solid #666; }
~~~

desktop.blocks/button/button.css

~~~css
.button { font-size: 13px; }
~~~

touch.blocks/button/button.css

~~~css
.button { font-size: 26px; }
~~~

## Платформы собираются из уровней переопределения

| desktop | touch-pad | touch-phone |
+---------|-----------|-------------+
| common  | common    | common      |
| desktop | touch     | touch       |
|         | touch-pad | touch-phone |
+---------|-----------|-------------+

## БЭМ
{:.with-big-quote}
> «Не только CSS»™

[Основные понятия: Технология реализации](https://ru.bem.info/method/definitions/#Технология-реализации)
{:.note}


## БЭМ: «Не только CSS»™

Аналогичный декларативный стиль с возможностью точечного переопределения применим для других технологий:

- [JS](https://ru.bem.info/technology/i-bem/v2/i-bem-js/)
- [HTML](https://ru.bem.info/technology/bemhtml/v2/intro/)

## БЭМ: Разработка для нескольких платформ
{:.section}

### Реальные примеры




## &nbsp;
{:.section}

### Заключение

## Tl;dr

- можно потратить усилия на организацию кода (декларативность, точечные переопределения)&hellip;
- и программировать под несколько платформ, экономя силы


## **Контакты** {#contacts}

<div class="info">
<p class="author">{{ site.author.name }}</p>
<p class="position">{{ site.author.position }}</p>

    <div class="contacts">
        <p class="contacts-left github">github.com/veged</p>
        <p class="contacts-left contacts-top mail">veged@yandex-team.ru</p>
        <p class="contacts-right twitter">@veged</p>
        <!-- <p class="contacts-right contacts-bottom vk">vk</p> -->
        <p class="contacts-right contacts-top facebook">veged</p>
    </div>
</div>
