# EduPage widget, Střední škola polytechnická Hustopeče

Statický widget pro vložení do webu v QARO přes iframe modul. Odkazuje na oficiální web školy [hustopecess.edupage.org](https://hustopecess.edupage.org/).

## URL pro iframe modul v QARO

```
https://dominikdigiday.github.io/edupage-ss-hustopece/
```

Doporučená výška iframe: cca 220 px na desktopu, cca 420 px na mobilu (pod 640 px se karta skládá do sloupce).

## Proč widget a ne přímý iframe na EduPage

EduPage posílá hlavičku `x-frame-options: sameorigin`, prohlížeč proto zobrazení `edupage.org` uvnitř iframe na cizí doméně zablokuje. Obsah EduPage tedy nejde vložit přímo, widget na něj místo toho odkazuje.

## Technické poznámky

- Odkaz se otevírá přes `target="_blank"`. QARO vkládá iframe se sandboxem bez `allow-top-navigation`, takže navigace celého okna by selhala. `allow-popups` v sandboxu je, nové okno projde.
- Čistě statické HTML a CSS, žádný JavaScript.
- Logo školy je uložené přímo v repu (`logo.png`), widget nezávisí na serverech EduPage.

## Úpravy

Texty jsou přímo v `index.html`, barvy v proměnných v bloku `:root` (zelená vychází z loga školy).
