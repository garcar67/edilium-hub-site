# Recap Sessione - Sito Edilium Hub
**Data:** 19 Marzo 2026

---

## Obiettivo
Creare un sito one-page WOW per **Edilium Hub Srls** (azienda di ristrutturazioni chiavi in mano), partendo da un documento di briefing (.pages) e loghi SVG forniti dal cliente.

---

## Fasi di lavoro

### 1. Ricerca
- **Best practice web design 2025-2026**: tipografia, colori, layout bento grid, hero section, CTA, mobile-first, animazioni, performance (Core Web Vitals)
- **Plugin HTML.to.Design (DivRiots)**: come strutturare HTML per importazione pulita in Figma (flexbox ovunque, Google Fonts, padding+gap invece di margin, no CSS Grid, DOM piatto, stili embedded)

### 2. Analisi contenuti
Estratto il testo dal file `TO DO LIST SITO.pages`:
- **Azienda:** Edilium Hub Srls
- **Identita:** Innovativa, efficiente, affidabile
- **Mission:** Rendere la ristrutturazione semplice e piacevole
- **Vision:** Cliente al centro, progetti estetico-funzionali
- **Valori:** Dettagli, precisione, attenzione al cliente
- **Differenziatori:** Rete partner 30ennale, consulenza completa (progetto + finanziaria + bandi), unico interlocutore
- **Target:** Privati, Aziende, Investitori
- **Servizi:** Progettazione, rilievo, intermediazione immobiliare, direzione lavori, impianti (elettrici, idraulici, fotovoltaico, videosorveglianza), manutenzione, chiavi in mano
- **Metodo:** Sopralluogo > Progetto > Preventivo > Esecuzione > Consegna
- **Team:** Ing. Giuseppe Decri (Direzione Tecnica), Maria Passarella (Commerciale)

### 3. Prima versione (classica)
File `index.html` originale con design elegante (Playfair Display + Inter, palette navy/gold/off-white). Scartata perche troppo classica.

### 4. Versione finale (tech/dark)
Ridisegnato tutto con estetica giovane, moderna e tech:
- **Font:** Space Grotesk (headings) + Inter (body) - Google Fonts per compatibilita Figma
- **Palette brand:** Gold #F9C441 + Teal #4F6C6C (estratti dal logo SVG fornito)
- **Background:** Dark #0a0f0f con cards semi-trasparenti e glow decorativi
- **Logo:** SVG inline nel navbar e footer (logo orizzontale completo con icona + testo "EDILIUM HUB web buildy oureality")
- **Layout:** Tutto flexbox (no CSS Grid) per auto-layout pulito in Figma
- **Sezioni:** Navbar > Hero > Chi Siamo > Servizi > Metodo > Target > Team > CTA > Footer

### 5. Animazioni e interattivita
- **Smooth scroll** sugli anchor links
- **Fade-up** con delay a cascata su hero e titoli sezioni
- **Fade-left/right** su chi siamo (solo desktop, su mobile diventa fade-up)
- **Scale-in** sul titolo CTA
- **Navbar:** fixed con shrink on scroll e backdrop blur
- **Active link highlight** dorato sulla sezione visibile
- **Hover effects:** translateY + shadow + border glow su tutte le cards e bottoni
- **prefers-reduced-motion** rispettato

### 6. Responsive
- **Desktop** (>1024px): layout completo
- **Tablet** (768-1024px): servizi 2 col, metodo grid 2x, hero impilato
- **Mobile** (<768px): single column, hamburger menu modale full-screen slide-down, bottoni full-width
- **Small mobile** (<400px): font-size ulteriormente scalati
- **Animazioni mobile:** tutte uniformate a fade-up (stessa direzione)

### 7. Menu mobile
- Hamburger animato (3 linee > X)
- Menu modale full-screen che scende dall'alto (translateY)
- Si chiude al click su un link
- Link grandi (22px) con spacing generoso

### 8. Copywriting
Riscritto tutto il copy da schematico/freddo a coinvolgente/conversazionale:
- Linguaggio diretto, in prima persona
- Focus su benefici per il cliente, non feature aziendali
- Tono rassicurante: "Niente sorprese", "Ci occupiamo di tutto", "Raccontacelo"
- CTA calde: "Parlaci del tuo progetto", "Scrivici", "Oppure chiamaci"

---

## Deployment
- **Repo GitHub:** https://github.com/garcar67/edilium-hub-site (pubblico)
- **GitHub Pages:** https://garcar67.github.io/edilium-hub-site/
- **Account:** garcar67
- **File unico:** `index.html` (tutto inline: CSS, JS, SVG)

---

## File presenti nel repo
- `index.html` — sito completo (versione finale dark/tech con logo, responsive, animazioni, copy riscritto)
- `RECAP-SESSIONE.md` — questo file

---

## Note tecniche per Figma
Per importare in Figma via HTML.to.Design:
- Il file usa solo flexbox (mappa ad Auto Layout in Figma)
- Solo Google Fonts (disponibili in Figma)
- Padding + gap invece di margin
- Stili tutti embedded nel tag `<style>`
- Larghezza base 1440px (max-width)
- Rimuovere il JS e le classi di animazione prima dell'import se si vuole un risultato piu pulito
