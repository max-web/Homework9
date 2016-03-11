# Homework9


Тестирование верстки в IE 8 проводил на локальном сервере (через WebStorm), т.к. поддержка медиазапросов сделана через respond.js.  У него:
	"Some browsers may not allow this script to work on file:// urls (because it uses xmlHttpRequest). Run it on a web server."
	Источник <https://github.com/scottjehl/Respond> 
Как вариант - могу для удобства проверки выложить код на хостинг.

## Как обеспечивал кроссбраузерность:

### Поддержка html5-тегов
полифил html5shiv через условные комментарии
### Поддержка медиазапросов
полифил respond.js через условные комментарии
### Поддержка CSS3
На основе принципа Graceful degradation.
Rgba для фона слайдера под хедером  - через 1-пиксельный PNG файл.
Тени для текста в IE8 - можно реализовать через фильтры
	filter: dropshadow(color=#999999, offx=1, offy=1);
скрин https://gyazo.com/f2a4ca324a6da2b6a307ad9d42cd9a02 
но мне кажется такое решение ухудшает внешний вид, поэтому от него отказался.
Вендорные префиксы (проставлены через Autoprefixer с учетом поддержки  IE8+, Firefox 5+, Opera 15+).
