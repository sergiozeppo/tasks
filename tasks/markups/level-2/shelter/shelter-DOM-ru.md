| Крайний срок сдачи | Имя папки | Имя ветки |
| ----------- | ------------- | ------------- |
| 26.10.2020 23:59 | shelter | shelter |


# Домашнее задание: shelter. DOM

Сверстать страницу согласно макету:

Figma:

**[shelter. DOM. Figma](https://www.figma.com/file/tKcmzkARtMUFQAR9VLdLkl/shelter-dom)**  

- Основные блоки должны быть точно расположены на заданной ширине экрана так, как на дизайне Figma.
- Изображения, логотипы (если они есть) должны быть расположены в рамках логического контейнера с правильным подходом по центрированию и расположению. Допускается отклонение от макета в угоду сеточной или колоночной структуре.
- Иконки, картинки должны сохранять идеальное расстояние до начала соответствующего им текста на приведенной ширине экрана.
- Имеются отдельно спроектированные блоки с описанием того, как выглядит кнопка с hover-эффектом, и без него.
- Если использован правильный шрифт, проверьте высоту текста — он должен соответствовать исходнику. Ширина может варьироваться. Но общепринятой практикой является добавление свойства межбуквенного интервала (`letter-spacing`) тексту заголовков, девиза (motto) или цитат.
- Если в строке несколько объектов визуально одинаковой ширины, то ширина содержащих их блоков должна быть одинаковой. Разница с дизайном в несколько пикселей не имеет значения, важно совпадение размеров.

Расширение PerfectPixel для Google Chrome можно использовать для того, чтобы сверяться с изображением 
*[Расширение PerfectPixel для Google Chrome](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)*

Поддержка браузеров: **Google Chrome, Mozilla Firefox, Microsoft Edge (Windows) or Safari (MacOS)**.

В первую очередь мы разрабатываем для Google Chrome. Затем проверяем, не «рушат» ли Mozilla Firefox, Microsoft Edge или Safari наши стили.


## Требования к репозиторию

- Задание выполняется в приватном репозитории школы [Как работать с приватным репозиторием](https://docs.rs.school/#/stage2?id=Как-работать-с-приватным-репозиторием)
- Структура папок не меняется, в каждой из папок внутри `pages` будут находиться файлы типы `.js`. Можно называть их `script.js`, и добавлять на каждую страницу в файле `.html` через относительный путь.
- Для деплоя используйте gh-pages [Как сделать деплой задания из приватного репозитория школы](https://docs.rs.school/#/stage2?id=Как-сделать-деплой-задания-из-приватного-репозитория-школы)
- История коммитов должна отображать процесс разработки приложения. [Требования к коммитам](https://docs.rs.school/#/git-convention)

## Проверка задания

- Задание будет проверяться целиком посредством кросс-чека согласно инстуркции, **которая появится 20 октября.** [Общая инструкция по проведению cross-check](https://docs.rs.school/#/cross-check-flow)

## Технические требования

- Запрещается использование CSS-фреймворков (bootstrap, foundation и т.д.).
- Рекомендуется использование CSS препроцессоров, normalize.css.
- Запрещается пользоваться фреймворками или компонентными библиотеками (React).
- Библиотеками с набором вспомогательных функций (lodash) пользоваться можно, как и утилитами для создания слайдера, пагинации, попапов. Однако, рекомендуется пользоваться чистым, или *ванильным* JavaScript.

Каждый из питомцев будет представлять из себя объект с набором данных, например:

```javascript
const pet = {
  name: 'Jennifer',
  img: '../../assets/images/jennifer.png',
  type: 'Dog',
  breed: 'Labrador',
  description: 'Jennifer is a sweet 2 months old Labrador that is patiently waiting to find a new forever home. This girl really enjoys being able to go outside to run and play, but won\'t hesitate to play up a storm in the house if she has all of her favorite toys.',
  age: '2 months',
  inoculations: ['none'],
  diseases: ['none'],
  parasites: ['none'],
}
```

❗ Каждый DOM-объект (блок) с описанием питомца, будь то слайдер, пагинация или попап, будет генерироваться из данных объекта. В объекте могут быть поля, которые вы придумаете и назовете сами, выше приведен лишь пример.

Данные всех 8 питомцев будут добавлены в формате `JSON` завтра.


### Main Page

1. **Header**
- В меню будут работать первые 2 элемента: `About the shelter` и `Our pets`. Остальные 2 пункта меню, хоть и будут присутствовать на странице, но будут неактивными, для чего можно использовать js.
- При нажатии на "Our pets" будет переход на страницу `Pets Page`.
- При нажатии на "About the shelter" страница окажется в начальном положении, т.е. с нулевым отступом сверху.
- При нажатии на логотип перехода не будет, так как мы уже находимся на основной странице.

#### Burger menu
- Бургер меню будет на странице только при width < 768px.
- При нажатии на бургер меню, с правой стороны будет выезжать блок шириной 320px, в котором будут вертикально расположенные и центрированные элементы меню. Должна присутствовать анимация выезда (slide-in).
- В элементах действуют те же правила активности и неактивности, как и в меню на большей ширине экрана.
- Область, выступающая за 320px должна быть затемнена. Свойство затемнения описано в дизайне макета Figma.
- При открытии меню, сама иконка меню поворачивается на 90 градусов. Должна присутствовать анимация поворота (rotate).
- При нажатии вне границ меню, на затемненную область, или на кнопку с иконкой бургер меню, меню должно заехать обратно. Должна присутствовать анимация заезда (slide-out).
- При закрытии меню, сама иконка меню поворачивается обратно на 90 градусов. Должна присутствовать анимация поворота (rotate).
- При нажатии на "About the shelter" страница окажется в начальном положении и меню будет закрыто.
  
2. Блок **Not only**
- При нажатии на кнопку "Make a Friend" будет переход на страницу `Pets Page`.
  
3. Блок **Our Friends**
- При нажатии на кнопку "Get to know the rest" будет переход на страницу `Pets Page`.

#### Slider
- Слайдер должен быть реализован со стрелакми, при нажатии на которые случается переход на новый блок элементов.
- Слайдер бесконечный, не имеет границ, т.е. можно нажимать влево и вправо сколько угодно раз, и каждый раз контент в блоках будет новый. В нашем случае, каждый новый слайд будет содержать **случайный** набор питомцев, т.е. формироваться из исходных объектов в случайном порядке.
- При 1280px <= width в блоке слайда 3 питомца.
- При 768px <= width < 1280px в блоке слайда 2 питомца.
- При width < 768px в блоке слайда 1 питомец.

#### Popup
- Попап - это отдельный элемент, который всплывает поверх страницы при нажатии на любое место элемента (блока) с описанием конкретного питомца, и центрируется. Остальная часть страницы затемняется. Цвет тени, форма попапа, кнопка его закрытия определены в дизайне макета Figma.
- В слайдере активные элементы выделаяются более светлым цветом заднего фона, и реагируют на `hover`.
- При нажатии на окно (блок) попапа ничего не происходит.
- При нажатии вне границ попапа, на затемненную область, или на кнопку с крестиком, попап и затемнение должны исчезнуть.
- При наведении мышкой на затемненную область или кнопку с крестиком, т.е. при событии `hover`, кнопка должна получить эффект наведения. Другими словами: кнопка интеректавная. При этом при наведении на окно (блок) самого попапа ничего не происходит.
- При 768px <= width в дизайне попапа есть картинка питомца.
- При width < 768px в дизайне попапа картинки питомца нет.
  
  
### Pets Page

- В меню будут работать первые 2 элемента: `About the shelter` и `Our pets`. Остальные 2 пункта меню, хоть и будут присутствовать на странице, но будут неактивными, для чего можно использовать js.
- При нажатии на "About the shelter" будет переход на страницу `Main Page`.
- При нажатии на "Our Pets" страница окажется в начальном положении, т.е. с нулевым отступом сверху.
- При нажатии на логотип будет переход на страницу `Main Page`.

#### Burger menu
- Бургер меню будет на странице только при width < 768px.
- При нажатии на бургер меню, с правой стороны будет выезжать блок шириной 320px, в котором будут вертикально расположенные и центрированные элементы меню. Должна присутствовать анимация выезда (slide-in).
- В элементах действуют те же правила активности и неактивности, как и в меню на большей ширине экрана.
- Область, выступающая за 320px должна быть затемнена. Свойство затемнения описано в дизайне макета Figma.
- При открытии меню, сама иконка меню поворачивается на 90 градусов. Должна присутствовать анимация поворота (rotate).
- При нажатии вне границ меню, на затемненную область, или на кнопку с иконкой бургер меню, меню должно заехать обратно. Должна присутствовать анимация заезда (slide-out).
- При закрытии меню, сама иконка меню поворачивается обратно на 90 градусов. Должна присутствовать анимация поворота (rotate).
- При нажатии на "Our Pets" страница окажется в начальном положении и меню будет закрыто.
  
2. Блок **Our Friends**

#### Popup
- Попап - это отдельный элемент, который всплывает поверх страницы при нажатии на любое место элемента (блока) с описанием конкретного питомца, и центрируется. Остальная часть страницы затемняется. Цвет тени, форма попапа, кнопка его закрытия определены в дизайне макета Figma.
- В слайдере активные элементы выделаяются более светлым цветом заднего фона, и реагируют на `hover`.
- При нажатии на окно (блок) попапа ничего не происходит.
- При нажатии вне границ попапа, на затемненную область, или на кнопку с крестиком, попап и затемнение должны исчезнуть.
- При наведении мышкой на затемненную область или кнопку с крестиком, т.е. при событии `hover`, кнопка должна получить эффект наведения. Другими словами: кнопка интеректавная. При этом при наведении на окно (блок) самого попапа ничего не происходит.
- При 768px <= width в дизайне попапа есть картинка питомца.
- При width < 768px в дизайне попапа картинки питомца нет.

#### Pagination
- Пагинация представляет из себя переключение страниц (таблиц или слайдов), путем перерисовки одних данных на другие, эффекты при этом могут быть разные: slide, fade. При этом всегда есть первая сраница и последняя.
- Самое важное: *при неизменных размерах области пагинации, возвращаясь на страницу под определнным номером, контент на ней всегда будет одинаков*.
- При загрузке `Our Pets` должен быть сформирован массив из 48 элементов псевдо-случайным образом. Каждый из 8 приведенных на макете питомцев должен встречаться ровно 6 раз. При этом каждые 8, каждые 6, и каждые 3, питомца не должны повторяться. Т.е. на одной странице пагинации не может быть одноврменно два одинаковых питомца.
- При загрузке `Our Pets` всегда должна быть активной первая страница.
- Кнопка `<<` всегда открывает первую страницу
- Кнопка `<` открывает предыдущую до текущей страницы
- Кнопка `>` открывает следующую после текущей страницы
- Кнопка `>>` всегда открывает последнюю страницу
- В кружке по центру указан номер текущей страницы
- Если открыта первая страница, кнопки `<<` и `<` - неактивны.
- Если открыта последняя страница, кнопки `>` и `>>` - неактивны.  
- При 1280px <= width на странице одновременно показаны 8 питомцев, а самих страниц 6. Т.е. при нажатии `>>` открывается шестая страница.
- При 768px <= width < 1280px на странице одновременно показаны 6 питомцев, а самих страниц 8. Т.е. при нажатии `>>` открывается восьмая страница.
- При width < 768px на странице одновременно показаны 3 питомца, а самих страниц 16. Т.е. при нажатии `>>` открывается шестнадцатая страница.


-------------
Успехов!