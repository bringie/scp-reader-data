# scp-reader-data

## По-русски

Этот репозиторий хранит офлайн-архив сайта [scpfoundation.net](https://scpfoundation.net)
(русский филиал Фонда SCP) для личного приложения-читалки. Архив собирается автоматически
раз в сутки из открытого API сайта и публикуется как файлы релизов этого репозитория.
Кода здесь нет — только данные и расписание сборки.

### Лицензия и авторство

Материалы принадлежат их авторам и распространяются по лицензии
[CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Источник —
<https://scpfoundation.net>. Каждая статья в архиве содержит список авторов и ссылку на
оригинал. Некоторые изображения могут распространяться по другим лицензиям — они указаны
на страницах оригинала.

### Удаление по запросу

Если вы правообладатель и хотите убрать статью или файл из архива, откройте issue в этом
репозитории и укажите адрес страницы (и имя файла, если речь об одном файле). После того как
запись внесена в список исключений, следующая сборка, которая публикует архив:

- не включает удалённое в новый архив (для страницы — вместе с её фрагментами `fragment:` и
  их файлами), а приложение удаляет его с устройства при обновлении;
- если удалённое могло попасть в уже опубликованные пакеты, заново собирает все пакеты этого
  вида (картинки или прочие вложения) и удаляет старые пакеты из релизов;
- для удалённой страницы стирает её исходный текст и текст её фрагментов в служебном файле
  состояния (релиз `state`); название, теги, имена авторов и список файлов остаются;
- удаляет текстовые пакеты прежних сборок.

Сборка, остановленная по лимиту времени во время загрузки страниц, ничего не публикует и
ничего не удаляет: она только стирает исходный текст в файле состояния, а остальное делает
первая следующая сборка, которая публикует архив.

### Манифест

<https://github.com/bringie/scp-reader-data/releases/download/manifest/manifest.json>

## In English

This repository holds an offline archive of [scpfoundation.net](https://scpfoundation.net)
(the Russian branch of the SCP Foundation) for a personal reader app. The archive is built
automatically once a day from the site's open API and published as release assets of this
repository. There is no code here, only data and the build schedule.

### Licence and attribution

The content belongs to its authors and is licensed under
[CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Source:
<https://scpfoundation.net>. Every article in the archive carries its authors and a link
to the original. Some images may be under other licences; those are stated on the
original pages.

### Removal requests

If you hold the rights and want an article or a file removed from the archive, open an
issue in this repository with the page address (and the file name, for a single file).
Once the entry is on the exclusion list, the next build that publishes:

- leaves the item out of the new archive (for a page, together with its `fragment:` pages
  and their files), and the app deletes it from devices on update;
- if the item may be in published parts, rebuilds every part of that kind (images or other
  attachments) and deletes the old parts from the releases;
- for a removed page, blanks its source text and that of its fragments in the mirror's
  state file (the `state` release); titles, tags, author names and file lists stay;
- deletes the text packs of earlier builds.

A build stopped by its time limit while fetching pages publishes nothing and deletes
nothing: it only blanks the stored source text in the state file; the rest is done by the
first later build that publishes.

### Manifest

<https://github.com/bringie/scp-reader-data/releases/download/manifest/manifest.json>
