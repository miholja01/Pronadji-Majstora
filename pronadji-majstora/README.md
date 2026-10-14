# Pronađi Majstora

Landing page za gradnju porodičnih kuća, vikendica i stambenih objekata.

Sajt je jedan `index.html` fajl sa ugrađenim CSS-om i malo JavaScript-a. Nema build koraka ni zavisnosti, samo se okači i radi.

## Struktura

```
pronadji-majstora/
├── index.html          # ceo sajt
├── assets/
│   ├── logo.png        # logotip (header i footer)
│   ├── favicon.png     # ikonica u tabu pretraživača
│   └── radovi/         # ovde stavite fotografije objekata
└── README.md
```

## Postavljanje na GitHub Pages

1. Na GitHub-u napravite novi repozitorijum, na primer `pronadji-majstora`.
2. Otpremite sadržaj ovog foldera (dugme "Add file" → "Upload files", ili preko git-a, vidi ispod).
3. U repozitorijumu otvorite Settings → Pages.
4. Pod "Build and deployment" izaberite Source: "Deploy from a branch", grana `main`, folder `/ (root)`, pa Save.
5. Posle minut-dva sajt je dostupan na `https://VASE-KORISNICKO-IME.github.io/pronadji-majstora/`.

Preko git-a iz terminala:

```bash
cd pronadji-majstora
git init
git add .
git commit -m "Prva verzija sajta"
git branch -M main
git remote add origin https://github.com/VASE-KORISNICKO-IME/pronadji-majstora.git
git push -u origin main
```

## Šta treba promeniti pre objave

### 1. Forma (Formspree)

1. Napravite besplatan nalog na https://formspree.io i novu formu.
2. Kopirajte adresu forme, izgleda kao `https://formspree.io/f/abcdwxyz`.
3. U `index.html` nađite `YOUR_FORMSPREE_ENDPOINT` i zamenite ga tom adresom.

### 2. Kontakt podaci

Telefon, email i radno vreme su privremeni. Nađite i zamenite u `index.html`:

- `+381 60 000 0000` (pojavljuje se dva puta)
- `kontakt@pronadjimajstora.rs` (pojavljuje se dva puta)
- `Ponedeljak do subota, 7 do 17 h`

### 3. Fotografije

Stavite slike u `assets/radovi/` (preporuka: JPG ili WebP, širine oko 1600 px, do 300 KB po slici).

U `index.html` svako mesto za sliku izgleda ovako:

```html
<div class="ph">
  <svg ...>...</svg>
  Mesto za sliku
</div>
```

Zamenite ceo taj `<div class="ph">...</div>` jednom linijom:

```html
<img src="assets/radovi/kuca-1.jpg" alt="Spratna kuća sa dvorištem" loading="lazy">
```

Mesta za slike: glavna fotografija u hero sekciji, fotografija ekipe u sekciji "Kako radimo" i pet kartica u sekciji "Radovi". Na karticama promenite i naslov i reč "Lokacija" u stvarno mesto.

## Spoljni resursi

- Font Inter: Google Fonts
- Font Lato 2.0 (naslovi, puna podrška za Č, Ć, Ž, Š, Đ): jsDelivr, paket `lato-font@3.0.0`

Instagram: https://www.instagram.com/pronadji__majstora__/
