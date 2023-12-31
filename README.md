# Расширенные элементы HTML
В начале Web был просто текстом, что было довольно скучно. К счастью, это продолжалось не долго - до появления возможности вставлять изображения (и другие, более интересные, типы контента) в веб-страницы. Существуют и другие типы мультимедиа, однако логичнее начать со скромного `<img>` элемента, используемого для вставки простого изображения в веб-страницу. В этой статье мы рассмотрим, как использовать элемент, начиная с основ, снабжать примечаниями, используя `<figure>`, и разберём, как это относится к фоновым изображениям CSS.
## Как разместить картинку на странице?
Изображения на веб-страницах вставляются с помощью тега `<img>`. Основные атрибуты этого тега:
src (source): путь к изображению. Это может быть URL-адрес в интернете или путь к файлу на локальном компьютере.
alt (alternative text): альтернативный текст, который отображается, если изображение не может быть загружено. Это также важно для доступности, так как читалки экрана используют этот текст для описания изображения пользователям с ограниченными возможностями зрения.
Чтобы разместить изображение на веб-странице, вы используете HTML и, при необходимости, CSS. Основной элемент для вставки изображений в HTML — это тег <img>. Вот базовые шаги для размещения изображения:</br>
1) Тег <img>: Это самозакрывающийся тег, который не требует закрывающего тега.</br>
2) Атрибут src (source): Определяет путь к изображению.</br>
3) Атрибут alt (alternative text): Предоставляет альтернативный текст для изображения, если оно не может быть отображено.</br>
```
<img src="path/to/your/image.jpg" alt="Описание изображения">
```
🔗[Описание тегa для работы с изображениями ](https://doka.guide/html/img/).</br>
В теге `<img>` в HTML используются разные типы ссылок для указания местоположения изображения. Вот основные виды ссылок, которые могут быть использованы:
#### 👁Абсолютные ссылки: 
Это полный URL, который указывает на местоположение изображения в интернете. Он включает в себя протокол (например, http или https), доменное имя и путь к файлу.
`<img src="https://www.example.com/images/photo.jpg" alt="Описание">` Здесь изображение загружается непосредственно с веб-сайта.
#### 👁Относительные ссылки: 
Эти ссылки указывают на файл изображения относительно текущего расположения HTML-документа. Они не включают доменное имя и полезны, когда изображение находится в той же директории, что и HTML-файл, или в поддиректории.
Пример:
`<img src="images/photo.jpg" alt="Описание">` Если HTML-файл находится в той же папке, что и папка images, этот код будет корректно отображать изображение.
##### ` CSS свойство object-fit: `
Свойство object-fit определяет, как содержимое заменяемого элемента, такого как `<img>` или `<video>`, должно заполнять контейнер относительно его высоты и ширины. </br>
  <b>Значения:</b> </br>
`fill:` Смещаемый контент меняет свой размер таким образом, чтобы заполнить всю область внутри блока: используется вся ширина и высота блока. </br>
`contain:` Смещаемый контент меняет свой размер таким образом, чтобы подстроиться под область внутри блока пропорционально собственным параметрам: окончательный размер контента будет определён как «помещённый внутрь» блока, ограничиваясь его шириной и высотой.</br>
`cover:` Смещаемый контент меняет свой размер таким образом, чтобы сохранять свои пропорции при заполнении блока: окончательный размер контента будет определён как «покрытие» блока, ограничиваясь его шириной и высотой.</br>
`none:` Смещаемый контент не изменяет свой размер с целью заполнить пространство блока: конечный размер контента будет определён с использованием алгоритма изменения размера по умолчанию, а также размер объекта по умолчанию равен ширине и высоте смещаемого контента.</br>

### Размещение фото через CSS
Свойство background объединяет все свойства для фона. Вы можете перечислить в нем значения для:
* background-image
* background-position
* background-size (CSS3)
* background-repeat
* background-attachment
* background-origin (CSS3)
* background-clip (CSS3)
* background-color

🔗[background-image](https://doka.guide/css/background-image/).
## Гиперссылка 
#### Что такое гиперссылка?
Гиперссылки — одно из самых интересных нововведений Интернета. Они были особенностью Сети с самого начала, но именно они превращают Интернет в Интернет. Они позволяют нам связывать наши документы с любым другим документом (или ресурсом), с которым мы хотим. С их помощью мы также можем связывать документы с их конкретными частями, и мы можем сделать приложения доступными на простом веб-адресе (сравните это с локальными приложениями, которые должны быть установлены, и другими такими же вещами). Почти любой веб-контент может быть преобразован в ссылку, так что когда вы кликаете по ней (или иным образом активируете), она заставляет веб-браузер перейти на другой веб-адрес [URL](https://developer.mozilla.org/ru/docs/Glossary/URL).</br>
Простая ссылка создаётся путём обёртывания текста или другого содержимого, который вы хотите превратить в ссылку, в элемент <a>, и придания этому элементу атрибута href который будет содержать веб-адрес, на который вы хотите указать ссылку.
```
<p>
  Я создал ссылку на
  <a href="https://greatcode.ru/">домашнюю страницу Greatcode</a>.
</p>
```
Атрибуты HTML-элемента <a>, используемого для создания ссылок, определяют его поведение и отображение. Вот наиболее часто используемые атрибуты этого элемента:
1) href (Hypertext Reference): Это основной атрибут, который указывает URL, на который ссылается ссылка. Может вести на другую веб-страницу, якорь на текущей странице, файл для скачивания, адрес электронной почты и т.д.
2) target: Определяет, где открыть связанный документ. Например, target="_blank" открывает ссылку в новой вкладке браузера.
3) itle: Предоставляет всплывающую подсказку, которая отображается при наведении курсора на ссылку. Может использоваться для предоставления дополнительной информации о том, куда ведет ссылка.
4) download: Предлагает загрузить указанный по ссылке файл вместо перехода на него. Этот атрибут часто используется для загрузки ресурсов, таких как изображения, документы и медиафайлы.
5) hreflang: Указывает язык ресурса, на который ссылается гиперссылка. Это полезно в многоязычных контекстах.
6) type: Определяет MIME-тип ресурса, на который указывает ссылка. Это может помочь браузеру правильно обработать или отобразить ресурс.
#### Практика написания хороших ссылок
При написании ссылок рекомендуется следовать некоторым правилам. Давайте рассмотрим их.

#### Используйте чёткие формулировки описания ссылок
На вашей странице легко добавить ссылки. Но этого не совсем достаточно. Мы должны сделать наши ссылки доступными для всех читателей, независимо от их возможностей и инструментов просмотра страницы, которые они предпочитают. Например:

1) Пользователям программ читающих с экрана нравится переходить по ссылкам на странице, читая адрес ссылки в тексте.
2) Поисковые системы используют текст ссылки для индексирования файлов, поэтому рекомендуется включать ключевые слова в текст ссылки, чтобы эффективно описывать, куда ведёт ссылка.
3) Пользователи часто бегло просматривают страницу, не читая каждое слово, и их глаза будут привлечены к тексту, который выделяется, например, ссылки. Им будет полезно описание того, куда ведёт ссылка.
### Псевдоклассы
Псевдокласс в CSS — это ключевое слово, добавленное к селектору, которое определяет его особое состояние. Например, `:hover` может быть использован для изменения цвета кнопки при наведении курсора на неё.
```
div:hover {
  background-color: #f89b4d;
}
```
Псевдоклассы дают возможность стилизовать элемент на основе не только отношений в DOM-дереве, но и основываясь на внешних факторах, таких как история посещений (например, `:visited`), состояние содержимого (вроде `:checked` у некоторых элементов формы) или позиции курсора мыши (например, `:hover` определяет, находится ли курсор мыши над элементом).</br>
🔗[псевдоклассы](https://developer.mozilla.org/ru/docs/Web/CSS/Pseudo-classes).</br>
### Некоторые псевдоклассы
* :hover
* :active
* :checked
* :disabled
* :first
* :focus
* :visited
* :nth-child()
### Некоторые псевдоэлементы
В CSS псевдоэлементы представляют собой ключевые инструменты для добавления специальных эффектов или декоративных особенностей к элементам без изменения HTML-структуры. Они используются для стилизации определенной части элемента. Ниже перечислены некоторые из наиболее часто используемых псевдоэлементов:

* ::before и ::after: Эти псевдоэлементы используются для вставки содержимого до или после содержимого целевого элемента. Они часто используются для добавления декоративных элементов.
* ::first-letter: Позволяет стилизовать первую букву параграфа. Это часто используется для создания "капитель".
* ::first-line: Применяется к первой строке текста в блочном элементе, позволяя стилизовать только эту часть текста.
* ::placeholder: Позволяет кастомизировать стиль текста-заполнителя в полях форм, таких как input и textarea.
* ::marker: Используется для стилизации маркеров в списках (`<ul>, <ol>`).
* ::selection: Позволяет изменять стиль текста, который пользователь выделяет (например, с помощью курсора мыши).
## Задачи
### 🏆 Задание 1: 
#### 1.1 Изображения в HTML:
#### 🔗[Ссылка на задание 1.1](https://greatcode.ru/lesson_3.1.html).
#### 🔗[Ссылка на задание 1.2](https://greatcode.ru/lesson_3.2.html).
#### 1.2 Ссылки в HTML:
Ссылки создаются с помощью тега `<a>` (anchor). Основные атрибуты: </br>
🔗[Описание тегa для работы с гиперссылками ](https://doka.guide/html/a/).
#### 🔗[Ссылка на задание 2.1](https://greatcode.ru/lesson_3.3.html).
#### 1.3 Таблицы в HTML:
Таблицы создаются с использованием нескольких тегов:
`(<table>)`: определяет саму таблицу.
`(<tr>)` (table row): определяет строку таблицы.
`(<th>)` (table header): определяет заголовочную ячейку, текст в которой обычно отображается жирным шрифтом и по центру.
`(<td>)` (table data): определяет стандартную ячейку таблицы.
🔗[Описание тегa для работы с таблицами ](https://doka.guide/html/tables/).
#### Если мы с вами успеваем закончить задание выше то приступаем к этому, если нет то статья обязятельна к чтению
### 🏆 Задание 2:  Изучение тегов, таких как `<b>, <i>, <strong>, <small>, и <mark>`.
Тег `<b>` используется для привлечения внимания 🔗[Описание тегa для работы с тегом ](https://doka.guide/html/b/).

Тег `<i>` курсивное начертание 🔗[Описание тегa для работы с тегом ](https://doka.guide/html/i/).

Тег `<strong>` добавляет обёрнутому в него слову или фразе очень высокую важность.🔗[Описание тегa для работы с тегом ](https://doka.guide/html/strong/).

Тег `<small>` используется для вывода текста мелким шрифтом. 🔗[Описание тегa для работы с тегом ](https://doka.guide/html/small/).

Tег `<mark>` выделяет или подсвечивает важный фрагмент текста. 🔗[Описание тегa для работы с тегом ](https://doka.guide/html/mark/).

