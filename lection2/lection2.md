# Лекция 2. HTML, CSS

**HTML** (Hypertext Markup Language) - язык текстовой разметки, используется для структурирования и отображения веб-страницы и ее контента. <br>
<br>
**Тег** - открывающий <...> и закрывающий </...>, позволяют браузеру определить где началась и закончилась гиперссылка. Тегом размечаем область документа, контента, которую нужно оформить тем или иным способом&<br>
<br>
Тег \<p> - показывает браузеру, что это будет абзац. Поставили тег \<p>, абзац пошел, поставили тег \</p> - абзац закончился. <br>
<br>

      <p>Моя кошка очень милая.\</p>

**Синтаксические конструкции** (**элементы**) - совокупность открывающего тега, закрывающего тега и контента внутри них. Идентификация элемента - название элемента.
Элементы также могут иметь **атрибуты**, которые добавляют **св-ва** элементу (прим - выравнивание по центру - атрибут align).
Оформление элемента через атрибут - использование внутри тега доп параметры - атрибуты. Атрибут имеет свой синтаксис - имя, его свойства. <br>
<br>

      <p class="editor-note">Моя кошка очень милая</p>

В примере выше, **class** - имя атрибута, **editor-note** - значение атрибута. Класс позволяет дать элементу идентификационное имя, которое может использоваться позже, чтобы обращаться к элементу с информацией о стиле и проч. <br>
<br>

Атрибут всегда должен иметь:

1. пробел между ним и именем элемента (или предыдущим атрибутом, если элемент уже имеет один
   или несколько атрибутов).
2. имя атрибута, за которым следует знак равенства.
3. значение атрибута, заключённое с двух сторон в кавычки <br>
   <br>

## Вложенные эл-ты:

Мы также можем располагать элементы внутри других элементов — это называется вложением. Степень вложенности не ограничена, теги должны закрываться как матрешки - вложенность не должна перемежаться.

      <p>Моя кошка\<strong>очень\</strong>мимишная\</p> - верно

<br>

      <p>Моя кошка\<strong>очень мимишная\</p>\</strong> - НЕ верно

## Пустые эл-ты

Кроме элементов (откр тег+контент+закр тег), бывают эл-ты не требующие внутреннего контента - **пустые**. Пустой эл-т <img>(позволяет вставлять внутреннюю картинку в HTML документ) - атрибуты _src_ - путь, откуда берем картинку, _alt_ - конкретизируем что за изображение здесь будет показано.

      <img src="https://i.gifer.com/2GU.gif" alt="Моё тестовое изображение">

<br>

      <img src="https://rg.ru/uploads/images/157/42/83/30p_RIAN_150_obtravka_1000.jpg"/>

<br>

### Стандартная (общая) структура HTML-документа

Создавая HTML-документ с 0 - структура прописывается вручную, в IDE структура вставляется автоматически.<br>
<br>

HEAD - часть, нужная поисковым роботам; +организационные моменты, информация о кодировании. 6 ур-ней заголовков \<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6> <br>
<br>
BODY - контент страницы: картинки, видео, тексты. <br>
<br>
Списки - \<ul> \<li>
Создание гиперссылки - тег \<a>, атрибут - \<href> - указывается путь, куда мы должны перейти, щелкнув на гиперссылку.

### CSS (Cascading Style Sheets) - каскадная таблица стилей, код для стилизации веб-страницы/веб-сайта. С помощью селекторов указывает как будет оформлен элемент/совокупность элементов. Основа оформления, анимации в HTML - за счет CSS.

У CSS есть свой собственный синтаксис, который включает в себя структуру.

I способ: селектор (что конкретно) + набор его свойств (как оформлять). Все свойства - в фигурных скобках. У св-ва - название и его значение. Все св-ва отделены друг от дружки ";"
Прилинковать оформление в документ - внутри HTML-док-та можно открыть тег \<style> <br>
<br>
Красный абзац -

      p {
      color: red;
      }

II способ: внутри документа прописать ссылку/файл, где будет находиться таблица стилей. Хранится в отдельном док-те с расширением .css
link - внешняя связь - куда ссылаемся, где находится файл.

p - св-ва:

      p {
         color: red;

         width: 500px;

         border: 1px solid black;
         }

Выбор нескольких эл-тов.
Селектор эл-та. id-селектор - внутри эл-та уникальный идентификатор, на кот будем ссылаться. Можно оформлять не один эл-т, а мн-во.
Более сложные конструкции, состоящие из многих тегов, имеющие общие характеристики (прим: общий отступ от края) - создавать не отдельные id, а набор id - класс. Классу можно задавать оформление.
**Псевдоклассы** - объекты, сущности, которых якобы не существует - изменение кнопки, например, при взаимодействии с ней.

## Шрифты и текст

**Шрифт** по умолчанию **Times New Roman**
Проблемы - засечки - антиквы - в маленьком кедре(?) засвечиваются, выглядит не очень хорошо. Как минимум нужно надписи сделать гротескными(?) без засечек.
Решение: взять шрифт на сайте гугл фонт (автоматическая генерация). После прилинковки текстового файла с сервера гугла, нужно указать в таблице стилей, как будет оформляться элемент.
Прим: шрифт roboto отлично смотрится на android.

## Какие еще значения, кроме размера и цвета? padding, border, margin.

Современный интернет - интернет с блочной структурой - весь контент разделен на блоки или слои. Работая с этими слоями, легко получить картинку, которую задумал дизайнер.
У блоков есть соответствующие характеристики - **padding**(отступы внутри блока), **border**(граница, показывает где закончится элемент), **margin**(отступы внутри блока).

## Изменение цвета страницы - background color

Цвет создается по названию - html color

## Тело - body {width, margin, backround-color, padding, border}

Позиционирование и стилизация заголовка - h1 {margin(отсутствие отступа от внешней границы), padding(отступы внутри блока), text-shadow(не более 1-2 пикселей)}

Центрирование изображения - img {display, margin}
