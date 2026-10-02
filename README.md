# BELLOW HORROR

### Maturitná práca — Unreal Engine

> **„Čím hlbšie sa ponoríš, tým menej vieš, čo je skutočné.“**

Krátka príbehovo orientovaná hororová hra z pohľadu prvej osoby odohrávajúca sa v temnom podvodnom prostredí.

Hráč sa ujíma úlohy potápača, ktorý musí postupne odhaľovať príbeh, plniť úlohy a prežiť v prostredí, kde sú kyslík, orientácia a vlastná psychika rovnako dôležité ako samotné nebezpečenstvo.

---

## O projekte

Cieľom maturitnej práce je vytvoriť funkčný prototyp krátkej príbehovo orientovanej hororovej hry.

Hra kombinuje:

* podvodný prieskum
* psychologické prvky a mechaniku paniky
* systém kyslíka
* dynamické osvetlenie a obmedzenú viditeľnosť
* orientáciu pomocou vodiaceho lana
* hľadanie predmetov pomocou detektora kovov
* interakciu s predmetmi a ich používanie
* environmentálne nebezpečenstvá
* zvukové a vizuálne efekty
* príbeh založený na postupnom odhaľovaní udalostí

Výsledkom bude ucelená podvodná mapa s minimálne 5 nadväzujúcimi príbehovými úlohami, ktoré využívajú vytvorené herné mechaniky.

---

# Matejova časť

## Gameplay & Player Systems

Matej je zodpovedný najmä za hernú logiku spojenú s hráčom a hlavnými gameplay mechanikami.

### Hlavné systémy

#### Pohyb hráča pod vodou

* realistický pohyb potápača
* ovplyvnenie pohybu stavom paniky
* reakcia ovládania na aktuálny stav hráča

#### Systém kyslíka

* postupná spotreba kyslíka
* vizuálna spätná väzba
* zvukové upozornenia
* reakcia ostatných herných mechaník na stav kyslíka

#### Mechanika paniky

* dynamická úroveň paniky
* reakcia na nedostatok kyslíka
* reakcia na prostredie
* reakcia na príbehové udalosti
* ovplyvnenie správania a pohybu hráča

#### Interakčný systém

* interakcia s predmetmi
* zbieranie predmetov
* používanie predmetov
* prepojenie predmetov s príbehovými úlohami

#### Detektor kovov

* vyhľadávanie skrytých predmetov
* zvuková a vizuálna signalizácia
* využitie v rámci príbehových úloh

#### Vodiace lano

* navigácia v podvodnom prostredí
* pomoc pri orientácii
* využitie počas príbehových udalostí

### Prepojenie mechaník

Jednotlivé systémy budú navzájom prepojené tak, aby vytvárali ucelený gameplay loop.

```text
Prieskum
    ↓
Interakcia
    ↓
Príbehová udalosť
    ↓
Zvýšenie napätia
    ↓
Zmena stavu hráča
    ↓
Ďalší postup
```

---

# Igorova časť

## Environment, Events & Atmosphere

Igor je zodpovedný najmä za návrh herného prostredia, atmosféru, príbehové udalosti a systémy reagujúce na postup hráča.

### Podvodná úroveň

* návrh a tvorba jednej kompletnej hrateľnej podvodnej úrovne
* rozmiestnenie objektov a interaktívnych prvkov
* vytvorenie prostredia podporujúceho príbeh
* prepojenie jednotlivých častí mapy s príbehovými úlohami

### Dynamické osvetlenie

* systém dynamického podvodného osvetlenia
* obmedzená viditeľnosť
* zmeny osvetlenia podľa situácie
* vizuálne zvýraznenie príbehových udalostí
* využitie svetla na vytváranie napätia

### Skriptované udalosti

Prostredie bude reagovať na postup hráča pomocou skriptovaných udalostí.

Môže ísť napríklad o:

* zmenu osvetlenia
* aktiváciu zvukov
* objavenie nových objektov
* zmenu prostredia
* spustenie príbehovej udalosti
* aktiváciu nebezpečenstva

### Checkpoint & Save systém

Implementácia systému umožňujúceho:

* ukladanie priebehu hry
* vytváranie checkpointov
* načítanie posledného checkpointu
* zachovanie stavu príbehových udalostí
* pokračovanie v hre po načítaní

### Nepriateľ / environmentálne nebezpečenstvo

Súčasťou úrovne bude nepriateľ alebo environmentálne nebezpečenstvo, ktoré bude reagovať na hráčovu prítomnosť alebo jeho postup.

Jeho správanie bude prepojené s:

* stavom prostredia
* príbehovými udalosťami
* zvukom
* osvetlením
* postupom hráča

---

# Herná štruktúra

Hra bude obsahovať minimálne 5 nadväzujúcich príbehových úloh.

### 01 — Začiatok ponoru

Hráč sa oboznámi s prostredím a základnými hernými mechanikami.

### 02 — Prvý nález

Pomocou interakcie a detektora kovov hráč objavuje prvé dôležité predmety.

### 03 — Strata orientácie

Prostredie a obmedzená viditeľnosť začínajú ovplyvňovať hráčovu orientáciu a psychický stav.

### 04 — Neznáme nebezpečenstvo

Hráč sa stretáva s udalosťou alebo nebezpečenstvom, ktoré výrazne mení atmosféru hry.

### 05 — Odhalenie

Posledná časť spája získané predmety, príbehové udalosti a herné mechaniky do záverečnej sekvencie.

> Jednotlivé úlohy budú vzájomne prepojené a vytvoria jeden súvislý príbeh.

---

# Technológie

| Technológia         | Využitie                           |
| ------------------- | ---------------------------------- |
| **Unreal Engine**   | Herný engine                       |
| **Blueprints**      | Herná logika a systémové mechaniky |
| **3D editor**       | Tvorba a úprava 3D objektov        |
| **Audio**           | Zvukové efekty a atmosféra         |
| **Vlastné skripty** | Špecifické herné mechaniky         |

---

# Assety

Projekt využíva kombináciu:

* vlastných 3D modelov
* upravených assetov
* hotových assetov
* vlastných materiálov
* zvukových efektov
* vizuálnych efektov

> Hotové assety slúžia predovšetkým ako súčasť výsledného prostredia. Hlavná hodnota projektu spočíva vo vlastnej implementácii herných mechaník a ich vzájomnom prepojení.

---

# Architektúra herných mechaník

```text
                         ┌───────────────┐
                         │    PRÍBEH     │
                         └───────┬───────┘
                                 │
                ┌────────────────┼────────────────┐
                │                │                │
                ▼                ▼                ▼
          ┌──────────┐     ┌──────────┐     ┌───────────┐
          │  PANIKA  │◄───►│  KYSLÍK  │     │ PROSTREDIE│
          └────┬─────┘     └────┬─────┘     └─────┬─────┘
               │                │                 │
               └────────────────┼─────────────────┘
                                ▼
                         ┌───────────────┐
                         │     HRÁČ      │
                         └───────┬───────┘
                                 │
                ┌────────────────┼────────────────┐
                │                │                │
                ▼                ▼                ▼
          ┌──────────┐     ┌──────────┐     ┌──────────┐
          │ DETEKTOR │     │INTERAKCIA│     │   LANO   │
          │  KOVOV   │     │ S OBJEKT.│     │          │
          └──────────┘     └──────────┘     └──────────┘
```

---

# Cieľ projektu

Cieľom projektu je vytvoriť krátky, ale ucelený herný zážitok, v ktorom jednotlivé mechaniky nie sú oddelené systémy, ale navzájom spolupracujú a podporujú príbeh.

Dôraz je kladený najmä na:

**Atmosféru · Napätie · Príbeh · Gameplay · Interakciu · Ponorenie hráča**

---

# Autori

## Matej

### Gameplay Programmer

Zodpovednosť:

`Player Movement` · `Oxygen System` · `Panic System` · `Interaction` · `Metal Detector` · `Guideline System`

## Igor

### Level & Systems Designer

Zodpovednosť:

`Level Design` · `Lighting` · `Events` · `Save System` · `Environmental Threats` · `Atmosphere`

---

# Maturitná práca

**Študijný odbor:** Umelá inteligencia
**Prostredie:** Unreal Engine
**Typ projektu:** First-Person Horror / Story-driven
**Platforma:** PC
**Status:** `In Development`

---

> ### GO DEEPER.
>
> **Find the truth.**
> **Before the oxygen runs out.**
