# Mappings - Mapiranje podataka za usporedbu cijena

Ovaj projekt sadrži standardizirana mapiranja za normalizaciju podataka koji se koriste u sustavima za usporedbu cijena.

## 📋 Pregled

Projekt se sastoji od CSV datoteka za mapiranje koje pomažu u standardizaciji podataka iz različitih izvora:

- **Mapiranje kategorija proizvoda** - standardizacija naziva kategorija
- **Mapiranje gradova** - normalizacija naziva gradova u Hrvatskoj

**Izvor podataka**: Izvorne vrijednosti u mapiranjima preuzete su iz projekta prikupljanja podataka [cijene.dev](https://cijene.dev).

## 📁 Struktura datoteka

### `categories_mappings.csv`
Sadrži mapiranja specifičnih naziva kategorija proizvoda u standardizirane glavne kategorije:

- **Stupac `from`**: Originalni naziv kategorije (kako se pojavljuje u izvornim podacima)
- **Stupac `to`**: Standardizirani naziv glavne kategorije

**Regulatorni okvir**: Prema [Uredbi o načinu objavljivanja cijena (NN 75/2025)](https://narodne-novine.nn.hr/clanci/sluzbeni/2025_05_75_979.html), trgovci su dužni objaviti pripadajuće kategorije proizvoda: "hrana, piće, kozmetika, sredstva za čišćenje, toaletne potrepštine, proizvodi za kućanstvo". Međutim, neki trgovci ne poštuju ovu obvezu te koriste vlastite nazive kategorija, što zahtijeva mapiranje u propisane standardizirane kategorije.

**Napomena**: Unosi koji završavaju s `~~` označavaju kategorije za koje nismo sigurni kako ih mapirati. Preporučuje se da se takvi unosi ignoriraju prilikom obrade podataka.

**Glavne kategorije (prema uredbi):**
- `Hrana`
- `Piće`
- `Kozmetika`
- `Sredstva za čišćenje`
- `Toaletne potrepštine`
- `Proizvodi za kućanstvo`

### `cities_mappings.csv`
Sadrži mapiranja različitih varijanti naziva gradova u standardizirane nazive:

- **Stupac `from`**: Varijanta naziva grada (s dijakritičkim znakovima ili bez njih, kratice, itd.)
- **Stupac `to`**: Standardizirani naziv grada

**Primjeri mapiranja:**
- `Cakovec` → `Čakovec`
- `Zagreb - Sesvete` → `Zagreb`
- `Slavonski_Brod` → `Slavonski Brod`

## Svrha

Ovaj projekt omogućuje:

1. **Normalizaciju podataka** - ujedinjavanje različitih varijanti istih kategorija/gradova
2. **Standardizaciju** - korištenje konzistentnih naziva kroz različite sustave
3. **Olakšano filtriranje** - grupiranje proizvoda po glavnim kategorijama
4. **Poboljšanu pretraživost** - pronalaženje proizvoda bez obzira na varijante naziva

## 🔄 Ažuriranje

Datoteke je moguće proširiti dodavanjem novih mapiranja:

1. Dodajte novi redak u odgovarajuću CSV datoteku
2. Slijedite format: `izvorni_naziv;standardizirani_naziv`
3. Testirajte mapiranje prije produkcije

## 📄 Licenca

Ovaj projekt je licenciran pod [GNU Affero General Public License v3](LICENSE.txt).

## 🤝 Doprinosi

Doprinosi su dobrodošli! Molimo:

1. Provjerite postojeća mapiranja prije dodavanja novih
2. Koristite konzistentne standardizirane nazive
3. Testirajte promjene prije slanja

## 📧 Kontakt

Za pitanja ili prijedloge otvorite issue ili pošaljite pull request.

---

*Ovaj projekt pomaže u standardizaciji podataka za hrvatske sustave usporedbe cijena.*
