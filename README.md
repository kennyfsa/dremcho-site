# Дремчо — публичен сайт (GitHub Pages)

Статичен сайт за **dremcho.com** (one-pager + privacy).

## Файлове
- `index.html` — landing (от mockup one-pager)
- `privacy.html` — политика за поверителност (за Google Play)
- `logo_*.svg` — бранд

## Качване в GitHub Pages
1. Създай repo (напр. `dremcho-site`), Visibility: Public.
2. Качи съдържанието на тази папка `site/` в root на repo-то.
3. Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)`.
4. Custom domain: `dremcho.com` (и по желание `www.dremcho.com`).
5. Изчакай HTTPS да стане зелено.

## DNS в SuperHosting (за dremcho.com)
В клиентската зона → Домейни → DNS зоната на `dremcho.com`:

**За apex (dremcho.com)** — GitHub Pages A записи (махаш стари A към паркинг, ако има):
```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
```

**За www** (по желание):
```
CNAME  www   <твой-github-user>.github.io
```
(Замени с реалното ти `username.github.io`.)

TTL: 300 или default. Пропагацията може да отнеме от минути до няколко часа.

## Проверка
- https://dremcho.com
- https://dremcho.com/privacy.html  ← този URL слагаш в Play Console

## Не тук
API-то (`api.dremcho.com`) се хоства отделно (Render/Railway/VPS) — не в GitHub Pages.
