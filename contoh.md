## Format
format penulisan kamus :
```
kata, (konteks/kepanjangan/maksud) arti.
```
setiap kata dan arti HARUS dalam satu baris tidak boleh ada baris baru (\n). jika menggunakan teks editor aktifkan `Word Wrap` agar tidak scroll ke samping.

contoh benar
```
1 zakat,(Islam) tithe. zakat-fitrah (Islam) tithe in rice or money paid on 
  last day of fasting month. zakat-maal tithe paid by rich people.
2 
3
4
5
```
contoh salah
```
1 zakat,(Islam) tithe. zakat-fitrah (Islam) tithe in rice or money paid on 
2 last day of fasting month. zakat-maal tithe paid by rich people.
3
4
5
```


## Contoh
```
grep, (linux-cli) pencarian konten file dengan pola.
yuncto,/yungkto/ (Leg.) in connection with.
yunior,"1 (Sport) junior, pertaining to or concerning youth. 2 son of."
yuniorat,k.o. college preparatory school emphasizing classics (esp. in colonial period and formerly in Jesuit training).
zabur,psalm. Kitab-Zabur (Bib.) Book of Psalms.
zadat,(Phys.) solid.
zakat,(Islam) tithe. zakat-fitrah (Islam) tithe in rice or money paid on last day of fasting month. zakat-maal tithe paid by rich people.
zakelijk,/sakelek/ (Coll.) businesslike.
zat,"(Chem.) essence, substance. zat-air hydrogen.  zat-asam oxygen. zat-cair liquid. zat-hijau cholorophyl. zat-lemas nitrogen. zat-makanan vitamin.  zat-telur protein, albumen. zat-yang maha tinggi the supreme substance (God)."
zending,(Rel.) /sending/ Protestant missionary or mission.
zeni,1. (Mil.) detachment of army engineers. 2. (Coll.) genius.
zero,(Ling.) zero allomorph.
zirah,(Lit.) coat of chain-mail.
zohal,(Astr.) Saturn.
zuriat,"1 (Biol.) seed. 2 descendant, posterity."
```

## Menambahkan
Setelah edit file selesai simpan dengan nama yang anda mau misal `new-data.csv`.

Merge file `new-data.csv` dengan file `kmus-db`
```bash
$ more new-data.csv >> kmus-db
```