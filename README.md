# htmlcss-pricing-plan

Progetto realizzato in **HTML** e **CSS** per replicare una sezione **Pricing Plan** responsive, partendo esclusivamente dagli screenshot forniti.

## Obiettivo

L’esercizio consisteva nel ricreare una classica pagina con **piani prezzi**, capace di adattarsi alle diverse risoluzioni dello schermo.

Il layout doveva comportarsi in questo modo:

- in **mobile** le card si dispongono **una sotto l’altra**
- aumentando lo spazio disponibile, le card si **affiancano progressivamente**
- in **desktop** il layout arriva fino a **3 colonne**, quando lo spazio lo consente

## Nome repository

`htmlcss-pricing-plan`

## Richieste della consegna

- realizzare l’intera struttura da zero
- usare come font un generico `sans-serif`
- creare un layout responsive capace di adattarsi automaticamente alle varie larghezze

## Bonus

- in modalità **tablet**, quando entrano solo **2 card**, la **terza card** deve occupare tutta la larghezza disponibile
- quando una card occupa tutta la riga, la lista delle **feature** deve disporsi su **2 colonne**, come mostrato nello screenshot di riferimento

## Tecnologie utilizzate

- **HTML5**
- **CSS3**

## Struttura del progetto

- `index.html` → struttura della pagina
- `style.css` → stile e gestione del layout responsive

## Scelte sviluppative

Per la disposizione delle card è stato utilizzato **Flexbox** con:

- `display: flex`
- `flex-wrap: wrap`
- `gap`
- `flex-basis` con `calc()`

In questo modo il layout si adatta in maniera fluida allo spazio disponibile, permettendo alle card di andare automaticamente a capo senza dover dipendere solo dalle media query classiche.

## Formula utilizzata per le colonne

Per gestire l’incolonnamento delle card è stata usata una formula con `calc()` applicata a `flex-basis`.

Esempio per un layout a **3 colonne** con `gap: 32px`:

```css
.card {
  flex-basis: calc(100% / 3 - (32px * 2) / 3);
}
```

## Competenze allenate

Con questo esercizio ho lavorato su:

- struttura semantica HTML
- gestione del layout responsive
- utilizzo di Flexbox
- organizzazione degli spazi tra gli elementi
- costruzione di un’interfaccia a partire da un riferimento grafico

## Conclusione

Questo progetto è stato utile per esercitarmi nella creazione di componenti responsive e nella gestione dinamica dell’incolonnamento degli elementi in una sezione reale di interfaccia.