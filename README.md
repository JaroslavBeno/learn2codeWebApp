# learn2codeWebApp
Tento repozitár je pre tých, ktorý si chcú trénovať git príkazy. Spolu môžme vytvoriť jednoduchú alebo zložitejšiu web stránku.

## Changelog
* použité HTMLPrettify a SassBeautify
* link na stylesheet zmenený na main-style.min.css
* Google Fonts presunuté do .scss
* Kompresia bg01.jpg (každý kb sa počíta)
* Odstránenie main-style.css.map
* Pridanie .gitignore, package.json, gulpfile.js
* Vytvorenie _variables.scss
* reorganizácia postupnosti v main-style.scss (zmena výzoru komentárov je len osobná preferencia)
* Pridanie normalize.css do main-style.scss
* `color: $color-3;` som pridal rovno `body,html` a odstránil som ho z `btn--red` a `.intro`
* `text-align: center;` som pridal rovno `body,html` a odstránil som ho z `.header` a `.headline__wrapper`
* z `.headline` som odstránil `font-weight: 700;`
* z `.text` som odstránil `font-family: $text;`
* pridaný jednoduchý transition na hover

## Spustenie Node.js, npm, gulp.js
1. Nainštaluj si [Node.js](https://nodejs.org/en/) (s ním sa nainštaluje aj [npm](https://www.npmjs.com/)).
2. Cez CMD (ja používam [cmder](http://cmder.net/)) sa prepni do adresára kde máš index.html napríklad: <br>`cd C:\Users\\'username'\Documents\GitHub` namiesto
`'username'` použi názov tvojho konta.
3. Do CMD napíš `npm install` - tento príkaz ti nainštaluje všetky dependencies ktoré potrebuješ. (môže to trvať pár minút)
4. DO CMD napíš `npm start` - tento príkaz bude sledovať súbor *main-style.scss* a vytvorí z neho *main-style.css* a *main-style.min.css*. Každá zmena bude zaznamenaná a súbory *main-style.css* a *main-style.min.css* sa automaticky prepíšu. Plus je v gulpfile.js priložený *browserSync*, ktorý vytvorí web server a keď sa zmení .html súbor sám refreshne browser a keď sa zmení .css tak ho replacne.

### Otázky
* Používaš [BEM](http://getbem.com/)?
* Kôli čomu je v **main-style.css**:`@charset "utf-8";`?
* Kôli čomu je v **main-style.css**:
```
* {
    &,
    &:before,
    &:after {
        box-sizing: border-box;
    }
}

a,
a:hover {
    color: inherit;
    text-decoration: none
}

.no-padding {
    padding: 0;
}

.no-margin {
    margin: 0;
}
```
* Prečo má `.btn` `display: inline-block;`?