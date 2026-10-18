# Файлы под чужим расширением

Просмотр выбирает обработчик по содержимому файла, а не по имени. Каждый файл
здесь — копия образца с другим расширением; в имени записано, что внутри на
самом деле. Колонка «Просмотр» — что показала страница просмотра в Chrome
2026-10-18.

| Файл | Что внутри | Копия чего | Ожидаемый результат |
| --- | --- | --- | --- |
| `SampleSS-xls.doc` | книга Excel 97–2003 | `poi-spreadsheet/SampleSS.xls` | таблица с переключателем на 3 листа |
| `SampleSS-xlsx.xls` | книга `.xlsx` | `poi-spreadsheet/SampleSS.xlsx` | таблица, как у `.xlsx` |
| `message-rtf.doc` | RTF | `poi-misc/message.rtf` | «RTF documents are not supported», кнопка сохранения есть |
| `quick-html.xls` | HTML-страница | `poi-misc/quick.html` | «That address did not return a document» |
| `orders-csv.xls` | CSV («выгрузка в Excel») | `orders.csv` из `node test/make-fixtures.mjs` | «That address did not return a document» |

`.docx` под именем `.doc` — это `../sample-docx.doc`, он открывается как обычный `.docx`.

Копии файлов Apache POI распространяются по Apache License 2.0 — `LICENSE` и
`NOTICE` в этом каталоге; источник и коммит — в `../poi-misc/README.md` и
`../poi-spreadsheet/README.md`.
