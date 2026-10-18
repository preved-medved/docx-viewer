# Прочие фикстуры из Apache POI

Файлы для проверок, которым нужен не документ Word и не книга: что просмотр
отказывается открывать, и один `.docx` с колонками. Взяты из тестовых данных
Apache POI без изменений.

- **Источник:** https://github.com/apache/poi/tree/trunk/test-data
- **Коммит:** `ae62bb5116b9aee19ebd5834e3a82066132c9f7f` (тот же, что у `docs/poi/`)
- **Лицензия:** Apache License 2.0 — `LICENSE` и `NOTICE` в этом каталоге.

Колонка «Просмотр» — что показала страница просмотра в Chrome 2026-10-18.

| Файл | Откуда в POI | Для чего | Просмотр |
| --- | --- | --- | --- |
| `message.rtf` | `hmef/quick-contents/` | RTF; переименованная копия — `misnamed/message-rtf.doc` | ссылка на `.rtf` значка не получает |
| `quick.html` | `hmef/quick-contents/` | HTML-страница; переименованная копия — `misnamed/quick-html.xls` | ссылка значка не получает |
| `quick.pdf` | `hmef/quick-contents/` | вкладка Upload отклоняет `.pdf` | не открывается — так задумано |
| `SampleShow.pptx` | `slideshow/` | вкладка Upload отклоняет `.pptx`; клик по ссылке скачивает файл | не открывается — так задумано |
| `stress014.docx` | `integration/` | `.docx` в две колонки на несколько листов | 5 листов, текст в две колонки |
