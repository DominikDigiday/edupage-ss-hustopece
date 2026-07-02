# EduPage widget, Střední škola polytechnická Hustopeče

Statický widget pro vložení do webu v QARO přes iframe modul. Odkazuje na oficiální web školy [hustopecess.edupage.org](https://hustopecess.edupage.org/).

## URL pro iframe modul v QARO

```
https://dominikdigiday.github.io/edupage-ss-hustopece/
```

Widget je stavěný na iframe **1188 × 175 px** a vyplní celou výšku iframe, ať je jakákoliv. Na šířkách pod 640 px skryje logo, takže výška 175 px stačí i na mobilu.

## Proč widget a ne přímý iframe na EduPage

EduPage posílá hlavičku `x-frame-options: sameorigin`, prohlížeč proto zobrazení `edupage.org` uvnitř iframe na cizí doméně zablokuje. Obsah EduPage tedy nejde vložit přímo, widget na něj místo toho odkazuje.

## Technické poznámky

- Odkaz se otevírá přes `target="_blank"`. QARO vkládá iframe se sandboxem bez `allow-top-navigation`, takže navigace celého okna by selhala. `allow-popups` v sandboxu je, nové okno projde.
- Čistě statické HTML a CSS, žádný JavaScript.
- Logo školy je uložené přímo v repu (`logo.png`), widget nezávisí na serverech EduPage.

## Úpravy

Texty jsou přímo v `index.html`, barvy v proměnných v bloku `:root` (hlavní barva `#00a2e8`).
