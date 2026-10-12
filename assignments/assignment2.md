# Zadanie 2

V druhom zadaní využijete poznatky z predmetu na analýzu, riešenie a vyhodnotenie modelového optimalizačného problému. Na projekte pracujete v **trojčlenných tímoch**. Vaším cieľom je ukázať, že viete problém presne formulovať, navrhnúť a implementovať vhodné reprezentácie a modely, vybrať primerané metódy riešenia, navrhnúť férové experimenty a vysvetliť, čo výsledky hovoria o skúmanom probléme a použitých prístupoch.

Projekt odovzdáte postupne v niekoľkých míľnikoch. Po každej odovzdávke dostanete spätnú väzbu, ktorú môžete zapracovať do ďalšej verzie. Očakáva sa, že v ďalších výstupoch stručne uvediete, ako ste na spätnú väzbu reagovali a prečo ste prípadné odporúčania nezapracovali. Priebežné verzie slúžia na overenie smerovania projektu; rozumná zmena metódy alebo experimentálneho plánu po získaní prvých výsledkov je súčasťou práce.

## Výber a rozsah problému

V tomto zadaní si tému nevyberáte voľne. K dispozícii bude päť modelových optimalizačných úloh, každá v troch variantoch. Ako tím uvediete svoje preferencie; konkrétnu úlohu a variant vám následne pridelí vyučujúci. Pri prideľovaní sa zohľadnia preferencie tímov a dostupnosť jednotlivých variantov. Viac informácií bude poskytnutých v MS Teams.

### Ponúkané úlohy

1. **Úloha 1: Optimalizácia spojenia vo verejnej doprave**
   - **Variant 1A – Optimalizácia cesty vlakom:** Pripravte údaje o vlakových spojeniach a hľadajte vhodné cesty medzi zvolenou východiskovou a cieľovou stanicou pre určený deň v týždni a čas odchodu. Riešenie môže zahŕňať viacero vlakov a prestupov. Pri hodnotení cesty zvážte napríklad čas príchodu, celkové trvanie, počet prestupov a čas potrebný na prestup. K riešeniu pripravte aj jednoduché grafické rozhranie.
   - **Variant 1B – Optimalizácia cesty MHD:** Získajte cestovný poriadok MHD vo zvolenom meste a hľadajte trasy medzi dvoma geografickými polohami. Začiatok ani cieľ cesty nie sú priamo zastávky: súčasťou riešenia je výber dostupných nástupných a výstupných zastávok a zohľadnenie pešieho presunu k nim. Pri hodnotení trasy zvážte celkový čas cesty vrátane chôdze a čakania, počet prestupov a prípadné limity pešej vzdialenosti. K riešeniu pripravte aj jednoduché grafické rozhranie.
   - **Variant 1C – Optimalizácia časov odchodov spojov:** Získajte cestovný poriadok regionálnych autobusov vo vybranom kraji alebo MHD vo vybranom meste. Vašou úlohou je upraviť časy odchodov vybraných spojov tak, aby sa zlepšila dostupnosť odľahlých obcí, prípadne okrajových častí mesta. Najprv určte, ktorých cestujúcich alebo spojení sa má zlepšenie týkať a ako ho budete merať. Pri úpravách rešpektujte zvolené prevádzkové obmedzenia, napríklad povolený rozsah posunu odchodov a nadväznosť spojov. Porovnajte upravený cestovný poriadok s pôvodným a posúďte aj to, či zlepšenie jedných spojení nezhoršilo iné.

2. **Úloha 2: Optimalizácia fungovania mesta**
   - **Variant 2A – Riadenie križovatky:** Na základe modelu dopravných tokov optimalizujte organizáciu jednej križovatky. Môžete skúmať zmenu hlavnej cesty alebo nastavenie dĺžky a poradia fáz semaforov. Cieľom môže byť skrátenie čakania, obmedzenie tvorby kolón alebo zlepšenie priechodu chodcov pri dodržaní bezpečnostných pravidiel. Na modelovanie križovatky a získanie údajov o toku použite napríklad verejné kamery. 
   - **Variant 2B – Umiestnenie miest na ochladenie počas horúčav:** Vyberte, kde zriadiť obmedzený počet verejne prístupných ochladzovacích miest. Uprednostnite dostupnosť pre obyvateľov z oblastí s vyšším tepelným zaťažením alebo s menším prístupom k zeleni. Súčasťou úlohy je rozhodnúť, ako merať dostupnosť a ako zohľadniť kapacitu jednotlivých miest.
   - **Variant 2C – Plánovanie opráv mestských komunikácií:** Pri obmedzenom rozpočte rozhodnite, ktoré úseky opraviť a v akom poradí. Zohľadnite technický stav, mieru využívania, cenu opravy a riziko ďalšieho zhoršovania.

3. **Úloha 3: Optimalizácia stratégie pri hraní hier**
   **Poznámka:** V tejto úlohe budete optimalizovať **celú hernú stratégiu**. Jedno kandidátne riešenie musí predstavovať súbor pravidiel alebo parametrov, podľa ktorých hráč rozhoduje počas celej hry. Môže ísť napríklad o váhy hodnotiacej funkcie, ktoré určujú, ako stratégia posudzuje dostupné ťahy. Kandidáta vyhodnotíte odohraním viacerých hier a optimalizačná metóda následne hľadá lepšie nastavenie celej stratégie.

   - **Variant 3A – Človeče, nehnevaj sa:** Navrhnite stratégiu, ktorá pri viacerých možných ťahoch vyberá, ktorou figúrkou pohnúť. Vopred stanovte pravidlá hry, podľa ktorých budete simulovať partie. Stratégie porovnávajte na viacerých hrách s rôznymi hodmi kockou a proti rovnakým súperom.
   - **Variant 3B – Connect Four:** Navrhnite stratégiu pre výber stĺpca, do ktorého hráč vloží žetón. Stratégie vyhodnocujte proti viacerým súperom a sledujte výsledky pri hre za oboch začínajúcich hráčov.
   - **Variant 3C – 2048:** Navrhnite stratégiu pre výber smeru posunu dlaždíc. Keďže nové dlaždice vznikajú náhodne, každú stratégiu vyhodnoťte vo viacerých hrách. Porovnajte napríklad dosiahnuté skóre, najvyššiu vytvorenú dlaždicu a stabilitu výsledkov.

4. **Úloha 4: Maximalizácia výnosov**
   - **Variant 4A – Výber akcií alebo indexov:** Máte obmedzenú sumu, ktorú na začiatku sledovaného obdobia rozdelíte medzi vybrané akcie alebo indexové fondy. Kandidátnym riešením je výber aktív a sumy investované do každého z nich. Nasimulujte vývoj hodnoty portfólia počas niekoľkých rokov a porovnajte jeho výnos a riziko s jednoduchou východiskovou stratégiou, napríklad rovnomerným rozdelením investície. Stanovte pravidlá, či a ako započítate poplatky a dividendy. Nepoužívajte rovnaké časové okno na doladenie optimalizácie výberu a vyhodnotenie stratégií.
   - **Variant 4B – Načasovanie nákupu a predaja:** Pracujete s vopred určenou sadou akcií. Vašou úlohou je navrhnúť stratégiu, ktorá určuje, kedy a v akom objeme jednotlivé akcie kúpiť alebo predať. Pri simulácii rešpektujte dostupný kapitál a nemožnosť použiť budúce ceny pri rozhodovaní a náklady na obchody. Vyhodnoťte výnos aj riziko stratégie na oddelenom období.
   - **Variant 4C – Stávkovanie na športové zápasy:** Na základe historických údajov o zápasoch a kurzoch navrhnite stratégiu, ktorá určuje, na ktoré výsledky staviť a akú časť dostupného rozpočtu použiť. Kandidát môže predstavovať pravidlá výberu stávok a určovania ich výšky. Používajte iba informácie a kurzy dostupné pred začiatkom daného zápasu. Na oddelených historických zápasoch nasimulujte vývoj rozpočtu a vyhodnoťte nielen celkový výnos, ale aj straty, kolísanie výsledkov a riziko vyčerpania rozpočtu. Napoužívajte rovnaké dáta na doladenie optimalizácie a na jej vyhodnotenie.

5. **Úloha 5: Optimalizácia rozhodnutí v každodennom živote**
   - **Variant 5A – Prideľovanie termínov u lekára:** Priraďte pacientom dostupné termíny podľa dĺžky vyšetrenia, ordinačných hodín a časových možností pacientov. Zohľadnite ich preferované časy a prípadné rozdiely v naliehavosti. Kandidátnym riešením je rozpis termínov pre všetkých pacientov. Vyhodnoťte, koľkým pacientom sa podarilo prideliť termín, ako dlho naň čakajú a do akej miery rozpis zodpovedá ich preferenciám.
   - **Variant 5B – Výber nehnuteľnosti:** Z dostupnej ponuky vyberte nehnuteľnosť, ktorá najlepšie vyhovuje možnostiam a preferenciám konkrétneho kupujúceho. Pri rozhodovaní zohľadnite napríklad celkové náklady na kúpu, lokalitu, veľkosť, stav nehnuteľnosti a dostupnosť miest dôležitých pre kupujúceho. Rozlíšte neprekročiteľné podmienky, ako je rozpočet, od vlastností, pri ktorých je kupujúci ochotný robiť kompromisy. Ukážte, ako sa výsledný výber mení pri odlišných preferenciách. Vytvorte interaktívnu aplikáciu, ktorá pomáha kupujúcemu vyberať nehnutelnosti pri zadávaní a zmene preferencií.
   - **Variant 5C – Optimalizácia nákupu potravín:** Pre zadaný nákupný zoznam rozhodnite, ktoré produkty a v akom množstve kúpiť v jednotlivých dostupných obchodoch. Zohľadnite ceny, veľkosti balení, dostupnosť produktov a prípadné zľavy. Do celkových nákladov zahrňte aj náklady alebo čas potrebný na návštevu viacerých obchodov. Kandidátnym riešením je kompletný nákupný plán, ktorý pokryje požadované množstvá.

Každý tím bude riešiť jeden pridelený variant. Variant určuje východiskový problém a jeho konkrétne podmienky; vašou úlohou bude problém analyzovať, navrhnúť a implementovať postup riešenia a vyhodnotiť dosiahnuté výsledky. Presný rozsah experimentov spresníte v návrhu projektu po oboznámení sa s pridelenou témou a po konzultácii s vyučujúcim. Problém musí byť dostatočne konkrétny, aby bolo možné jednoznačne definovať kandidátne riešenie, účelovú funkciu, prípadné obmedzenia a spôsob vyhodnotenia. Zároveň musí umožniť zmysluplné porovnanie viacerých prístupov na rovnakej sade inštancií.

V tomto zadaní **nestačí prevziať hotové riešenie ani iba zopakovať výsledky jedného článku**. To je náplňou prvého zadania. Môžete vychádzať z literatúry a existujúcich implementácií, ale musíte zdokumentovať vlastné rozhodnutia, experimenty a interpretáciu výsledkov. Nevyžaduje sa návrh úplne nového algoritmu ani dosiahnutie najlepšieho známeho výsledku.

## Čo má riešenie obsahovať

1. **Analýzu a formuláciu problému:** typ úlohy, účelovú funkciu vrátane smeru optimalizácie, prípustné riešenia, obmedzenia, veľkosť a vlastnosti kandidátov a ich komponenty. Vysvetlite, ako reprezentujete kandidátov a ako overujete splnenie obmedzení.
2. **Implementáciu modelu problému:** finálna reprezentácia kandidátnych riešení, implementácia cieľovej alebo ohodnocovacej funkcie a postup vyhodnotenia kandidáta. Súčasťou modelu musí byť aj spôsob kontroly obmedzení, prípadne zdôvodnený postup, ako pracujete s neprípustnými riešeniami. Overte na jednoduchých príkladoch, že model hodnotí kandidátov podľa zamýšľanej formulácie.
3. **Porovnávacie riešenie (baseline):** jednoduchý postup, voči ktorému budete posudzovať vlastné riešenie. Môže ísť napríklad o náhodné generovanie riešení, greedy postup alebo jednoduché lokálne prehľadávanie. Vysvetlite, prečo je zvolený postup vhodným východiskom pre vašu úlohu.
4. **Vlastný prístup k optimalizácii:** aspoň dve ďalšie zmysluplne odlišné prístupy riešenia prideleného problému. Môžete vychádzať zo známych algoritmov, no musíte zdôvodniť ich výber a ukázať, ako ste ich prispôsobili konkrétnej úlohe. Popíšte kľúčové rozhodnutia, napríklad spôsob vytvárania nových kandidátov, prácu s obmedzeniami, nastavenie parametrov a podmienky ukončenia.
5. **Vyhodnotenie pomocou férových experimentov:** porovnanie vlastného prístupu s baseline na rovnakých inštanciách a podľa rovnakých pravidiel vyhodnotenia. Zabezpečte porovnateľný výpočtový rozpočet, napríklad rovnaký čas alebo počet vyhodnotení kandidátov. Pri náhodných metódach vykonajte viac nezávislých behov. Vyhodnoťte kvalitu riešení, výpočtové náklady a podľa potreby aj stabilitu výsledkov či mieru splnenia obmedzení. Výsledky prezentujte v tabuľkách alebo grafoch a vysvetlite, v ktorých prípadoch jednotlivé prístupy fungujú dobre a kde majú svoje limity. Rozsah experimentov prispôsobte náročnosti problému. Ak je niektorá požiadavka pre zvolenú úlohu nevhodná, navrhnite pri prvom míľniku primeranú náhradu a zdôvodnite ju.


## Priebežné odovzdávky

Projekt odovzdáte v štyroch míľnikoch. Po každej odovzdávke dostanete spätnú väzbu, ktorú môžete zapracovať do ďalšej fázy. Jednotlivé výstupy na seba nadväzujú: ak na základe experimentov zmeníte pôvodný návrh, vysvetlite, čo vás k zmene viedlo.

### 1. Analýza problému

**Termín:** 6. týždeň
**Odovzdáte:** správu s analýzou prideleného problému.

Popíšte pridelenú úlohu, jej vstupy, možné riešenia, cieľ optimalizácie a obmedzenia. Zaraďte problém podľa taxonómie predstavenej na prvej prednáške a každé zaradenie zdôvodnite. Venujte sa najmä tomu, či ide o numerickú alebo kombinatorickú optimalizáciu, rozhodovací, optimalizačný alebo kombinovaný problém, spojitú alebo diskrétnu, jednoúčelovú alebo viacúčelovú, deterministickú alebo stochastickú, statickú alebo dynamickú úlohu, či existujú obmedzenie a či máte prístup k vnútornej štruktúre hodnotenia kandidátov.

Navrhnite aj niekoľko zmysluplných alternatív formulácie. Napríklad vysvetlite, ako by vyzerala definícia úlohy, keby sa statická úloha zmenila na dynamickú. Súčasťou správy musí byť aj návrh štruktúry kandidátnych riešení, ako aj návrh ich programovej reprezentácie.

### 2. Implementácia modelu a overenie pomocou baseline

**Termín:** 9. týždeň
**Odovzdáte:** spustiteľný kód, návod na spustenie a krátku správu.

Implementujte model zvolenej formulácie problému: reprezentáciu kandidátov, cieľovú alebo ohodnocovaciu funkciu, vyhodnotenie kandidáta a kontrolu obmedzení. Pripravte inštancie úlohy alebo postup ich načítania či vytvorenia.

Použiteľnosť modelu overte implementáciou jednoduchého porovnávacieho prístupu (*baseline*), ktorý vytvára kandidátne riešenia. Ukážte na konkrétnych príkladoch, že kandidátov možno vyhodnotiť a že výsledky zodpovedajú zamýšľanej formulácii problému. Vysvetlite, ako baseline vytvára riešenia a ako nakladá s neprípustnými kandidátmi.

V správe navrhnite **aspoň ďalšie dve metódy**, ktoré chcete použiť na riešenie úlohy. Pri každej vysvetlite, prečo je pre daný problém vhodná a aké úpravy bude potrebovať. Zohľadnite pritom skúsenosti z implementácie modelu: napríklad náklady na vyhodnotenie kandidáta, náročnosť dodržania obmedzení alebo vlastnosti zvolenej reprezentácie.

### 3. Prvé výsledky s navrhnutými metódami

**Termín:** 11. týždeň
**Odovzdáte:** aktualizovaný kód a správu s prvými experimentmi.

Implementujte obe navrhnuté metódy a otestujte ich spolu s baseline na vybraných inštanciách. Predložte prvé výsledky kvality riešení a výpočtových nákladov. Pri metódach s náhodnými prvkami vykonajte viac behov, aby ste mohli posúdiť aj stabilitu výsledkov.

Na základe experimentov zhodnoťte, či sú zvolené metódy pre úlohu skutočne vhodné. Identifikujte súčasné problémy riešenia, napríklad slabú kvalitu kandidátov, časté porušovanie obmedzení, vysoké výpočtové náklady alebo nestabilné výsledky. Navrhnite konkrétne vylepšenia a plán, ako problémy preveríte alebo vyriešite pred finálnou odovzdávkou. Ak sa rozhodnete niektorú metódu zmeniť, svoje rozhodnutie zdôvodnite prvými výsledkami.

### 4. Finálna odovzdávka a obhajoba

**Termín:** 13. týždeň
**Odovzdáte:** finálnu správu, zdrojový kód, inštancie alebo postup ich získania a návod na spustenie; riešenie odprezentujete a obhájite.

Finálne riešenie musí obsahovať všetky časti definované v sekcii **Čo má riešenie obsahovať**: analýzu a formuláciu problému, implementáciu modelu, baseline, dva vlastné prístupy a ich vyhodnotenie pomocou férových experimentov. Porovnajte metódy na rovnakých inštanciách a pri porovnateľnom výpočtovom rozpočte. Výsledky prezentujte v tabuľkách alebo grafoch, interpretujte rozdiely medzi metódami a pomenujte obmedzenia svojich záverov.

V správe stručne uveďte, ako ste zapracovali spätnú väzbu z priebežných odovzdávok a aké úlohy riešili jednotliví členovia tímu. Na obhajobe sa zapoja všetci štyria členovia; každý musí vedieť vysvetliť svoju časť práce aj hlavné rozhodnutia a výsledky spoločného riešenia.

## Hodnotenie

Pri hodnotení sa zohľadní najmä:

- správnosť a jasnosť formulácie problému;
- vhodnosť zvolených metód a kvalita vlastnej implementácie;
- férovosť, reprodukovateľnosť a rozsah experimentov vzhľadom na náročnosť úlohy;
- vecnosť analýzy, interpretácia výsledkov a schopnosť pomenovať ich obmedzenia;
- priebežná práca, zapracovanie spätnej väzby, kvalita dokumentácie a obhajoba všetkých členov tímu.

Za každý zo štyroch míľnikov dostanete známku A (5 bodov), B (4 body), C (3 body), D (2 body), E (1 bod) alebo FX (0 bodov); výsledné bodové hodnotenie zadania je súčtom bodov za všetky míľniky. Body jednotlivým členom tímu sa udeľujú podľa ich podielu na riešení.
