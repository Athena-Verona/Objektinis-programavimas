# Objektinis-programavimas
2023 metų ISI 1 kurso objektinio programavimo uždavinys

# Galutinė 1.0 versija

Galutinė 1 projekto versija, apjungianti visas 5 praeitas versijas. Galima rasti du aplankus, kuriuose yra du skirtingi variantai. 

### Paleidimas
1. Pasirinkite aplanką ir paleiskite makefile parašius **make** į savo komandinę eilutę. 
2. Paleidimui parašykite **./main**
## Aplankas "vector"
Tai galutinė versija, optimizuota su sparčiais konteinerių algoritmais. Ankstesnėse versijose jau realizuota sparti versija, todėl palyginimo nėra.
## Aplankas "vector deque list"
Galima rinktis, kurį studentų skaidymo būdą rinktis ir galima pamatyti konteinerių spartos analizę.
### Spartos analizė
#### Skaidymas į du naujus konteinerius
|            | Vector | Deque | List |
|------------|--------|-------|------|
| 1000       |    0.000286    |    0.000185   |    0.000263  |
| 10 000     |    0.001677    |    0.005085   |   0.003295   |
| 100 000    |    0.032419    |   0.025153    |   0.054680   |
| 1 000 000  |     0.254413   |    0.591458   |   0.535757   |
| 10 000 000 |    3.570025    |    3.128859   |   6.356380   |

 **Užimta 2,5-3 GB atminties su 10 mil**

#### Skaidymas į vieną naują konteinerį

|            | Vector | Deque | List |
|------------|--------|-------|------|
| 1000       |  0.000266      |    0.000344   |  0.000260    |
| 10 000     |   0.002467    |    0.001799   |   0.004344   |
| 100 000    |    0.025050    |    0.024613   |    0.064135  |
| 1 000 000  |    0.240916    |    0.253827   |    0.757946  |
| 10 000 000 |    2.747569    |   2.935171    |  7.743919    |

 **Užimta 1,7-2 GB atminties su 10 mil**

# Penktoji versija
Šioje versijoje nebuvo daug kas pakeista, tik šie veiksmai - failo nuskaitymas, sortinimas didėjimo tvarka ir skaidymas į du failus - atliekami trimis skirtingais būdais: **std::vector, std::deque ir std::lis**t. Paleista programa automatiškai atlieka skaičiavimus visais trimis būdais.
Kadangi failai vienodi palyginus su praeita versija, čia pateikiami tik spartos išmatavimai. 
## Vector
|          | Skaitymas | Rūšiavimas | Skaidymas |
|----------|-----------|------------|-----------|
| 1000     |     0.002784      |      0.000075      |      0.000266     |
| 10000    |     0.023773      |       0.000476     |      0.002467     |
| 100000   |      0.196043     |      0.005073      |      0.025035     |
| 1000000  |      1.865709     |       0.063594     |      0.252097     |
| 10000000 |      18.743032     |     0.591280       |    3.129753      |
## Deque
|          | Skaitymas | Rūšiavimas | Skaidymas |
|----------|-----------|------------|-----------|
| 1000     |      0.002416     |     0.000079       |      0.000185     |
| 10000    |     0.019360      |       0.000588     |     0.001799      |
| 100000   |    0.186196       |       0.009757     |      0.027583     |
| 1000000  |      1.817097     |       0.068257     |        0.217228   |
| 10000000 |     18.010306     |      0.679888      |     2.835921      |
## List
|          | Skaitymas | Rūšiavimas | Skaidymas |
|----------|-----------|------------|-----------|
| 1000     |     0.002304      |      0.000093      |     0.000260      |
| 10000    |      0.022091     |     0.001753       |      0.003295     |
| 100000   |     0.190998      |       0.030831     |    0.030142       |
| 1000000  |     1.961710      |      0.600316      |     0.331130      |
| 10000000 |      18.590231     |      9.588606      |     3.551435      |

## Kompiuterio duomenys:

**CPU:** 2,3 GHz Dual-Core Intel Core i5
**RAM:** 8 GB 2133 MHz LPDDR3
**SSD:** 121,33 GB APPLE SSD AP0128J

# Ketvirtoji versija
Ketvirta projekto versija, papildyta failų generatoriumi bei spartos matavimais.

### .cpp failai
1. _main.cpp_ - paleidžiamasis projekto failas, kuriame sukodinta programos eiga ir user input.
2. _calculate.cpp_ - čia aprašytos visos pagrindinės funkcijos (nuskaitymas, spausdinimas, balo skaičiavimas, rūšiavimas)
3. _generatorius.cpp_ - čia aprašyta tik viena - failo generavimo - funkcija, naudojanti map metodą ir C failo kūrimo metodą.
### .h failai
1. _mylib.h_ - įtrauktos bilbiotekos ir šablonai.
2. _cac.h_ - funkcijų prototipai, aprašyta struktūra.
### .txt failai
1. _studentai1000.txt_ - pavyzdinis generatoriaus sukurtas studentų failas.
## Programos spartos analizė pagal įrašų kiekį, įvertinta **sekundėmis**.
|   | 1000 | 10 000  | 100 000  | 1 000 000  | 10 000 000  |
|---|---|---|---|---|---|
| **Generavimas** | 0.002524  |  0.020975 | 0.188590  |  1.967706 |  17.909841 |
| **Nuskaitymas**  | 0.003156  |  0.022608 |  0.191797 |  1.840811 |  18.620220 |
| **Rūšiavimas**  |  0.000220 |  0.001314 |  0.018996 |  0.234441 |  2.817948 |
| **Spausdinimas**  |  0.001736 | 0.011761 | 0.094345  | 1.126077  | 10.26588  |
| **_TOTAL_**  | **0.006266** |**0.036453** |  **0.316182** |  **3.369767** | **33.458193** |

_Darbą atlieka S. Atėnė Vaicekauskaitė_

# Antroji ir trečioji projekto versijos
_**SVARBU! Ši projekto versija įgyvendina tiek v0.2, tiek v0.3 versijų reikalavimus, todėl įkeliamas vienas bendras projektas siekiant išvengti pasikartojimų tarp subrepozitorijų!!**_

# .h failai
1. mylib.h yra surašytos bibliotekos ir std funkcijos, kurios bus reikalingos visam projektui (pvz., sort(), vector).
2. calc.h yra surašytos funkcijų deklaracijos, reikalingos kodo vykdymui.

# .cpp failai
1. main.cpp yra paleidžiamasis failas, kuris tik kreipiasi į funkcijas.
2. calculate.cpp yra surašytos visos funkcijos, struktūros bei globalūs kintamieji.

# .txt failai
1. faile "kursiokai.txt" surašyti visi studentai, po 20 jų kiekvieno pažymių ir egzamino rezultatas. failo struktūra yra griežta, t.y. galima keisti skaičius ir duomenis tik jeigu eilutės lieka taip pat sulygiuotos.
2. kai paleisite programą, turi atsirasti failas "rezultatai.txt" su studentų galutiniais rezultatais.

# Failų skaitymo metodas
Failų skaitymo ir rašymo metodas buvo pasirinktas kaip C kalbos variantas (eilutė po eilutės). Taip buvo pasirinkta, nes programuotojos kompiuteryje šis būdas veikė bene triskart greičiau, nei bet kuris kitas būdas (10 000 eilučių su C užtruko 0.294896 sekundės, su "greitu" variantu per buferį - 1.55617 sekundės").

_pasikeitimai: pataisyta, kad būtų nuskaitoma failo pirma eilutė ir iš jos sprendžiama, kiek namų darbų studentas turi_

# Pirmoji versija

Tai yra pirma versija ilgalaikės užduoties, atlikta dviem būdais

1. Kodas **01_array.cpp** atliktas naudojant **dinaminius masyvus**
2. Kodas **01_vector.cpp** atliktas naudojant **vektorius**
3. Abu jie kreipiasi į failą mylib.h

_Darbą atlieka S. Atėnė Vaicekauskaitė:)_