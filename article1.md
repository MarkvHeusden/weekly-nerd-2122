## CSS Logical Properties and Values

Wanneer je een meertalige website wil maken kun je te maken krijgen met problemen in de layout wanneer een taal niet van links naar rechts gaat, maar andersom. Of zelfs als de taal van onder naar boven leest. Wanneer dit het geval is, is het erg handig om te kijken naar Logical Properties & Values in CSS. De browser support is inmiddels vrij goed, en ook als je niet met een meertalige website werkt kan het super handig zijn.

![Schermafbeelding 2022-06-20 om 21.42.45.png](/docs/1-1.png)

### Inline & block

We hebben allemaal wel is iets gecentreerd op 1 van de volgende 2 manieren:

```css
/* Voorbeeld 1 */
div {
  margin-left: auto;
  margin-right: auto;
}

/* Voorbeeld 2 */
div {
  margin: 0 auto:
}
```

Het eerste voorbeeld vereist 2 regels CSS, waardoor vaak het tweede voorbeeld wordt gebruikt (developers zijn nou eenmaal lui). Het probleem hierbij is, dat je bij het tweede voorbeeld gelijk de margin aan de boven en onderkant weghaalt, wat niet altijd gewenst is. Gelukkig kan je tegenwoordig met gebruik van logical properties. Dit houdt in dat je met 1 regel code de `div` kan centreren, terwijl je tegelijkertijd de margin top en bottom behoudt die je mogelijk eerder hebt ingesteld.

```css
/* Met logical properties */
div {
  margin-inline: auto;
}
```

Met `margin-inline` kun je dus in 1 keer de `margin-left` en `margin-right` definiëren. Hetzelfde is mogelijk voor de`margin-top` en `margin-bottom` , hiervoor kun je namelijk `margin-block` gebruiken.

## Meer dan margin

Hier eindigt het echt niet. Je kunt dit niet alleen voor de margin gebruiken, maar voor nog veel meer properties. Hieronder volgt een voorbeeld van andere selecteren die kunt gebruiken met de uitkomst ervan.

### HTML

```html
<p class="voorbeeld-1">border-block</p>
<p class="voorbeeld-2">border-inline</p>
```

### CSS

```css
/* Gebruik ook bij bijvoorbeeld padding */
p {
  padding-inline: 0.5rem;
  padding-block: 4rem;
}

/* Of bij borders */
.voorbeeld-1 {
  border-block: 0.5rem solid red;
}

.voorbeeld-2 {
  border-inline: 0.5rem solid red;
}
```

### Resultaat

![Schermafbeelding 2022-06-20 om 21.58.05.png](/docs/1-2.png)

## Writing mode & direction

Dit waren handige dingen om fijnere code te schrijven, maar je kunt het ook gebruiken bij meertalige sites met een andere leesrichting. Onze taal leest van links naar rechts, maar bijvoorbeeld Arabisch leest andersom. Dit kun je in je HTML wijzigen door de direction aan te passen.

```html
<!-- Left To Right, bijv. Nederlands -->
<html dir="ltr">
    
<!-- Right To Left, bijv. Arabisch -->
<html dir="rtl">
```

Omdat CSS is ontwikkelt met de Engelse taal, geeft het veranderen van de leesrichting veel problemen met de layout. Voorheen was dit te fixen door middel van de volgende code:

```css
.absolute-element {
  position: absolute;
}

[dir="rtl"] .absolute-element {
  right: 50px;
}

[dir="ltr"] .absolute-element {
  left: 50px;
}
```

Het wijzigen van elk element op deze manier is geen leuk werk en vereist ook veel code. Gelukkig kun je hiervoor ook CSS Logical Properties gebruiken. Je kunt dan het beste dingen als `left`/`right` vervangen door `inline`, `top`/`bottom` door `block`, of `top` door `start` en `bottom` door `end`.

Als je talen wil ondersteunen die van onder naar boven lezen kun je zelfs dingen als `width` en `height` vervangen. Bijvoorbeeld `inline-size` voor  `width` en `block-size` voor `height`.

## Voorbeeld

Dit is misschien nog wat vaag, maar er zijn nog veel meer properties die je kunt vervangen voor deze logical properties. Hier vind je een lijstje met nog een paar voorbeelden:

```css
/* Logical properties           Normale properties         */
border-block-start: 10px;     	/*  border-top: 10px;      */
padding-inline-end: 10px;     	/*  padding-right: 10px;   */
margin-block-start: 10px;      	/*  margin-top: 10px;      */
text-align: start;            	/*  text-align: left;      */
inline-size: 100px;             /*  width: 100px;          */
max-block-size: 100px;         	/*  max-height: 100px;     */
```

## Bronnen

-   [https://www.voorhoede.nl/nl/blog/how-to-multilingual-website-rtl-html-css/](https://www.voorhoede.nl/nl/blog/how-to-multilingual-website-rtl-html-css/)
-   [https://css-tricks.com/css-logical-properties-and-values/](https://css-tricks.com/css-logical-properties-and-values/)
