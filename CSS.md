#Руководство по оформлению CSS кода
<h3>Определения</h3>
Данное руководство основывается на методологии <a href="https://ru.bem.info">БЭМ</a>.<br>
Основные термины:
<ul>
	<li>Блок - Логически и функционально независимый компонент страницы</li>
	<li>Элемент - Составная часть блока, которая не может использоваться в отрыве от него</li>
	<li>Модификатор - позволяет определять внешний вид, состояние и поведение блока или элемента.</li>
</ul>

<h3>Именование классов</h3>
<ul>
	<li>имена классов записываются в нижнем регистре</li>
	<li>для разделения слов в именах используется одно подчеркивание (_)</li>
	<li>имя элемента отделяется от имени блока двумя подчеркиваниями (__)</li>
	<li>имя модификатора отделяется от имени блока или элемента одним дефисом (-)</li>
	<li>любой CSS класс должен начинаться с имени блока</li>
	<li>любой класс по своему предназначению и правилам составления имени должен быть блоком, элементом, или модификатором</li>
</ul>

<h3>Общие правила</h3>
<ul>
	<li>Запрещено использование inline-стилей</li>
	<li>Запрещено использовать каскадные стили, глубиной более одного элемента (например table td)</li>
	<li>Модификатор должен переопределять не более 40% стилей, в противном случае лучше создать новый блок</li>
	<li>Для адаптивной верстки предпочтительно использовать подход mobile-first: от простого – к сложному</li>
</ul>

<h3>Пример БЭМ-а</h3>
```html
<div class="nav_wrap">  
    <ul class="dop_nav">
        <li class="dop_nav__item nav__item-active"><a class="dop_nav__link">One</a></span></li>
        <li class="dop_nav__item"><a class="dop_nav__link">Two</a></li>
        <li class="dop_nav__item"><a class="dop_nav__link">Three</a></li>
    </ul>
</div>
```
`nav_wrap` и `dop_nav` обозначает имя блока, `dop_nav__item` и `dop_nav__link` — имена элементов, а `dop_nav__item-active` — имя модификатора элемента item

<h3>Полезные ссылки</h3>
<ul>
	<li><a href="http://delka.github.io/talks/webcamp/2015/bem/">Пишем БЭМ правильно</a></li>
	<li><a href="http://habrahabr.ru/post/203440/">Верстка для самых маленьких. Верстаем страницу по БЭМу</a></li>
</ul>

<h3>Необходимо выбрать вариант наименование классов</h3>
1) some-block__some-element_some-modificator<br>
2) some-block__some-element--some-modificator<br>
<br>
3) someBlock__someElement_someModificator<br>
4) someBlock__someElement--someModificator<br>
<br>
5) some_block__some_element-some_modificator<br>
6) some_block__some_element--some_modificator<br>

