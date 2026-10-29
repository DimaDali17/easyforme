# Сайт EasyForm — easyforme.ru

Статичный сайт-визитка. Без форм, cookies и счётчиков. Покупка — только по ссылкам на Wildberries и Ozon.

## Что в папке
- `index.html` — весь сайт (стили и анимация внутри)
- `assets/img` — логотип и фото товаров, `assets/fonts` — шрифты (Unbounded, Comfortaa), хранятся на сайте, без Google
- `CNAME` — домен easyforme.ru для GitHub Pages
- `.nojekyll`, `robots.txt`, `favicon.png`
- `page.html` — служебная копия для превью, на GitHub можно не загружать

## Как выложить на GitHub Pages (бесплатно)
1. На github.com создайте репозиторий, например `easyforme` (Public).
2. Add file → Upload files → перетащите всё содержимое этой папки (вместе с папкой `assets`, файлами `CNAME` и `.nojekyll`). Commit.
3. Settings → Pages → Source: «Deploy from a branch», ветка `main`, папка `/ (root)` → Save.
4. Там же в Custom domain должно стоять `easyforme.ru` (подтянется из файла CNAME).

## DNS у регистратора домена easyforme.ru
Удалите старые A-записи для `@` и добавьте:

| Тип   | Имя | Значение            |
|-------|-----|---------------------|
| A     | @   | 185.199.108.153     |
| A     | @   | 185.199.109.153     |
| A     | @   | 185.199.110.153     |
| A     | @   | 185.199.111.153     |
| CNAME | www | dimadali17.github.io. (или ваш_логин.github.io.) |

Через 10–60 минут (иногда до суток) в Settings → Pages поставьте галочку **Enforce HTTPS**.

## Что поменять при желании
- Ссылка на Ozon сейчас ведёт на поиск «easyform». Если есть ссылка на магазин продавца — замените `https://www.ozon.ru/search/?text=easyform` в index.html.
- Реквизиты продавца: в подвале есть закомментированная строка `<!-- Реквизиты продавца ... -->`.
- Карточки товаров ведут на WB: термобельё 1796630731, термомайка 502685453, термошорты 474514093, остальные — на поиск по бренду.
