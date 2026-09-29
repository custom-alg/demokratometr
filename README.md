# Demokratometr

**Jedno místo, kde je vidět stav a vývoj demokracie – s čísly, zdroji a hodnocením jejich důvěryhodnosti.**

Web: https://custom-alg.github.io/demokratometr/ · Verze 0.2 (prototyp)

## TL;DR

- Skládá mezinárodní indexy (Freedom House, V-Dem, EIU, RSF, TI CPI, WJP) do **12 oblastí demokracie** a jednoho **skóre 0–100**.
- Indexy se zpožďují o rok, proto zvlášť sleduje **signály**: konkrétní události za posledních 12 měsíců, každá se zdrojem.
- Každý zdroj má **hodnocení důvěryhodnosti** podle 6 kritérií (transparentnost, doložitelnost, nezávislost, věcnost, shoda zdrojů, aktuálnost).
- Hodnotí **instituce a pravidla, ne strany ani osoby**.
- Zatím měří Česko, Německo a Slovensko; Rakousko, Maďarsko a Polsko se připravují.

## Jak to funguje

```
indikátor (FH, V-Dem, EIU, …) → převod na 0–100
oblast  = průměr indikátorů
celkem  = vážený průměr oblastí (váhy si čtenář může změnit)
skóre   → pásmo režimu (liberální demokracie … uzavřená autokracie)
```

Podrobnosti jsou přímo na webu v sekci **Metodika**.

## Stav projektu

Funkční prototyp. Data jsou zatím natvrdo v `index.html` a část hodnot je převzatá ze sekundárních zdrojů (Wikipedie, statranker.org) – před ostrým spuštěním se musí ověřit v primárních datech.

Co je potřeba dodělat (data, ověřování lidmi, aktualizace pomocí agentů, organizace, která projekt zaštítí): **[PLAN.md](PLAN.md)**.

## Spuštění

Statický web bez závislostí. Stačí otevřít `index.html` v prohlížeči, nebo:

```sh
python3 -m http.server
```

Nasazení: GitHub Pages z větve `main`.

## Našli jste chybu?

Založte [issue](https://github.com/custom-alg/demokratometr/issues) s odkazem na zdroj. Každá oprava bude zapsána do veřejného seznamu změn.

## Autor

Petr Šimčák – web, technické řešení a návrh konceptu.
