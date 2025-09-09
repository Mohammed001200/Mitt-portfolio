# Anteckningar: HTML Basics och Semantic HTML

## HTML Basics - Grundläggande Koncept

### Vad är HTML?
- **HyperText Markup Language** - språk för att strukturera webbsidor
- Använder **taggar** (tags) för att märka upp innehåll
- Är inte ett programmeringsspråk utan ett **markup-språk**

### Grundläggande HTML-struktur
```html
<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <title>Sidtitel</title>
</head>
<body>
    <!-- Innehållet här -->
</body>
</html>
```

### Viktiga nya begrepp från HTML Basics:

#### 1. DOCTYPE Declaration
- `<!DOCTYPE html>` - talar om för webbläsaren vilken HTML-version som används
- Måste alltid vara första raden i HTML-dokumentet
- HTML5 har förenklat detta till bara `<!DOCTYPE html>`

#### 2. HTML Element Anatomi
- **Öppningstagg**: `<tagname>`
- **Innehåll**: texten mellan taggarna
- **Stängningstagg**: `</tagname>`
- **Attribut**: extra information i öppningstaggen `<tagname attribut="värde">`

#### 3. Viktiga Meta-taggar
- `<meta charset="UTF-8">` - definierar teckenkodning
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` - för responsiv design
- `<meta name="description" content="...">` - beskrivning för sökmotorer

#### 4. Block vs Inline Element
- **Block-element**: tar upp hela bredden (div, p, h1-h6)
- **Inline-element**: tar bara upp nödvändig plats (span, a, strong)

## Semantic HTML - Semantiska Element

### Vad betyder "Semantisk"?
- **Semantik** = betydelse/mening
- Semantisk HTML använder element som beskriver **vad** innehållet är, inte **hur** det ser ut
- Hjälper webbläsare, sökmotorer och hjälpmedel att förstå innehållet

### Viktiga semantiska element:

#### Strukturella Element
- `<header>` - huvudsektion, oftast överst på sidan eller i en sektion
- `<nav>` - navigationsområde med länkar
- `<main>` - huvudinnehållet på sidan (bara ett per sida)
- `<section>` - tematisk gruppering av innehåll
- `<article>` - fristående innehåll som kan läsas separat
- `<aside>` - sidoinnehåll, som sidokolumner eller relaterat innehåll
- `<footer>` - sidfot, oftast nederst på sidan eller i en sektion

#### Textstruktur
- `<h1>-<h6>` - rubriker (hierarkisk ordning viktigt!)
- `<p>` - paragraf/stycke
- `<address>` - kontaktinformation
- `<time>` - datum/tid
- `<mark>` - markerad/highlighted text

#### Listor och Definitioner
- `<dl>` - definition list (lista med definitioner)
- `<dt>` - definition term (termen som definieras)
- `<dd>` - definition description (själva definitionen)

### Nya begrepp från Semantic HTML:

#### 1. Document Outline
- Strukturell hierarki skapad av h1-h6 element
- Hjälper skärmläsare att navigera
- Viktigt att inte hoppa över nivåer (h1 → h3 utan h2)

#### 2. Landmark Roles
- Semantiska element skapar automatiskt **landmark roles**
- Hjälper användare med hjälpmedel att navigera snabbt
- Exempel: `<nav>` = navigation role, `<main>` = main role

#### 3. Content Sectioning
- Dela upp innehåll i logiska sektioner
- `<section>` för tematisk gruppering
- `<article>` för självständigt innehåll
- `<aside>` för sidoinnehåll

#### 4. Accessibility Benefits
- **Screen readers** kan bättre förstå sidstruktur
- **Keyboard navigation** blir enklare
- **SEO-fördelar** - sökmotorer förstår innehållet bättre

#### 5. Progressive Enhancement
- Börja med semantisk HTML som fungerar överallt
- Lägg till CSS för styling
- Lägg till JavaScript för interaktivitet
- "Content first" - innehållet ska vara tillgängligt även utan CSS/JS

## Praktiska Tips

### Do's (Gör så här):
- Använd semantiska element istället för `<div>` när det finns lämpliga alternativ
- Skapa logisk rubrikhierarki (h1 → h2 → h3)
- Testa sidan med skärmläsare eller accessibility tools
- Validera HTML-koden regelbundet

### Don'ts (Undvik):
- Använda `<div>` och `<span>` för allt
- Hoppa över rubriknivåer
- Använda element för styling istället för semantik
- Glömma alt-text på bilder

## Sammanfattning
Semantisk HTML handlar om att välja rätt element för rätt innehåll. Det förbättrar tillgänglighet, SEO och kodens underhållbarhet. Modern webbutveckling ska alltid börja med välstrukturerad, semantisk HTML.