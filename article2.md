# Svelte & SvelteKit

In de meesterproef heb ik besloten gebruik te maken van Svelte en SvelteKit. Dit omdat ik graag wat nieuws wilde leren na 4 projecten met EJS gewerkt te hebben, en we het goed konden gebruiken voor rapid prototyping van onze concepten.

## Over Svelte

Op Front-End gebied zijn er veel technieken en frameworks, zoals React en Vue. Een wat minder populair, maar wel opkomend framework is Svelte. Svelte staat vooral bekend om de fijne *Developer Experience.* Svelte is wel anders dan de eerder genoemde frameworks. Net als bij Vue gebruik je 1 bestand voor styling, structuur en logica. Alleen gebruik je bij Vue een .vue bestand, en bij Svelte een .svelte bestand. 

Ook is Svelte een stuk lichter, waardoor het tijdens het ontwikkelen een build kan doen in compile-time. Andere frameworks hebben vaak nog een apart build-proces, maar Svelte is direct te gebruiken. Hierdoor is Svelte meer een soort compiler. Het zet je Svelte code om in geoptimaliseerde JavaScript, inplaats van het meesturen van een library naar de client.

### Voordelen Svelte

1. **Reactive:** Svelte apps zijn reactief.
2. **Minder code:** Voor een Svelte app is minder code nodig dan bijvoorbeeld een *React* app, en is hierdoor simpeler en makkelijker te schrijven.
3. **Kleiner:** Svelte apps zijn veel kleiner dan React apps. Daardoor vereist het minder kracht van het device van de gebruiker.

Een Svelte bestand ziet er uit als volgt:

```html
<script>
  let name = 'Mark';
</script>

<h1>Hoi {name}!</h1>

<style>
  h1 {
    color: red;
  }
</style>
```

Je JS, CSS en HTML zit dus in 1 bestand. Omdat Svelte reactive is veranderd de text op je scherm gelijk wanneer de variabele `name` veranderd.

## SvelteKit

Naast Svelte heb je ook nog SvelteKit. Dit framework is vergelijkbaar met Next.js voor React en Nuxt voor Vue. SvelteKit biedt bovenop Svelte dingen als *Server Side Rendering* en *Routing.* Daarnaast is het ook makkelijk om *Progressive Web Apps* te maken met Sveltekit

### Voordelen SvelteKit

- Server-side rendering
- Code splitting
- Client-side routing
- Simplified data pre-fetching
- One-command static-site export
- Full-stack hot deploy (dev mode)

## Bronnen

- [https://craftcode.be/svelte-vs-sveltekit-2/](https://craftcode.be/svelte-vs-sveltekit-2/)
- [https://www.sharevalue.nl/blogs/svelte-en-sveltekit-nieuwe-spelers-in-het-front-end-landschap](https://www.sharevalue.nl/blogs/svelte-en-sveltekit-nieuwe-spelers-in-het-front-end-landschap)
- [https://www.antagonist.nl/blog/svelte-web-app/](https://www.antagonist.nl/blog/svelte-web-app/)
- [https://www.infoworld.com/article/3634771/hands-on-with-sveltekit.html](https://www.infoworld.com/article/3634771/hands-on-with-sveltekit.html)