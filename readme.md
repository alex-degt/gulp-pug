# Gulp-збірка для верстки

Gulp-збірка для верстки з використанням шаблонізатора PUG, CSS фреймворку Tailwind CSS та препроцесора SASS для середніх за розміром проєктів (інтернет-магазин, корпоративний сайт, сервіс).  
З метою оптимізації кінцевого результату та зручності підтримки продукту кожна HTML-сторінка містить в собі:  
- загальні CSS-файли - ті, що використовуються на всіх сторінках (як власні стилі, так і бібліотеки):
	- `tailwind.css`
	- `...`
	- `all-pages.css`
- унікальні CSS-файли - ті, що використовуються лише на цій сторінці (як власні стилі, так і бібліотеки):
	- `owl.carousel.min.css`
	- `owl.theme.default.min.css`
	- `...`
	- `product.css`
- загальні JS-файли - ті, що використовуються на всіх сторінках (як власні скрипти, так і бібліотеки):
	- `jquery.min.js`
	- `...`
	- `all-pages.js`
- унікальні JS-файли - ті, що використовуються лише на цій сторінці (як власні скрипти, так і бібліотеки):
	- `owl.carousel.min.js`
	- `...`
	- `product.js`

## Старт

Необхідно мати [Node.js](https://nodejs.org/en/) та [Npm](https://www.npmjs.com/).

1. Встановити всі пакети:
```
npm i
```
2. Запустити в режимі розробки:
```
npm run dev
```
3. Зібрати production-версію:
```
npm run prod
```

## Опис задач 

1. **clean()** - видалити вміст `docs`
2. **copyJs()** - скопіювати js-файли з `src/js/*` в `docs/js/` (без обробки)
3. **copyImg()** - скопіювати зображення з `src/img/*` в `docs/img/` (без обробки)
4. **copyLibs()** - скопіювати бібліотеки з `src/libs/*` в `docs/libs/` (без обробки)
5. **copyFonts()** - скопіювати шрифти з `src/fonts/*` в `docs/fonts/` (без обробки)
6. **devStyles()** - обробити sass-файли з `src/sass/*` та покласти в `docs/css`
7. **prodStyles()** - обробити sass-файли з `src/sass/*` та покласти в `docs/css` з постобробкою для production
8. **jade()** - обробити pug-файли з `src/pug/gulp-pages/*` та покласти в `docs/`
9. **jadeProd()** - обробити pug-файли з `src/pug/gulp-pages/*` та покласти в `docs/` з постобробкою для production
10. **livePreview()** - запустити локальний сервер
11. **watchFiles()** - відстежувати зміну файлів
12. **previewReload()** - перезавантажити сервер якщо файли змінились

## Корисні сторонні сервіси

Для обробки векторної графіки (svg) - [SVGOMG](https://jakearchibald.github.io/svgomg/).  
Для обробки растрової графіки (jpg, png, webp, ..) - [Squoosh](https://squoosh.app/).  
Для генерації зображень будь-яких розмірів, що імітують зображення умовного товару - [Lorem Picsum](https://picsum.photos/).

