# Публикация на GitHub Pages

Сайт: https://azamuzak2004-sys.github.io/fbim-portal/

Репозиторий: https://github.com/azamuzak2004-sys/fbim-portal

В репозитории хранится готовая статическая сборка `site.zip`. Workflow `.github/workflows/static.yml` распаковывает её и публикует через GitHub Pages. Он не изменяет код репозитория. На хостинге работают только HTML, CSS, JavaScript и изображения.

## Обновление

1. Изменить содержимое сайта локально.
2. Выполнить `node prepare-github-pages.mjs` и `node verify.mjs`.
3. В PowerShell выполнить `Compress-Archive -Path dist\* -DestinationPath release\site.zip -Force`.
4. На GitHub загрузить новый `release/site.zip` в корень репозитория вместо старого `site.zip` и сохранить в ветку `main`.
5. Дождаться зелёного статуса workflow в разделе Actions.

Содержимое архива должно начинаться с `index.html`, а не с папки `dist`.
Адрес GitHub Pages для метаданных задаётся в `prepare-github-pages.mjs`.
Локальный редактор и его резервные копии не опубликованы.
