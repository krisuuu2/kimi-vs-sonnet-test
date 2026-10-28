# Kimi K3.1 Pro kontra Claude Sonnet 5.5: test w 10 minut

Kimi K3.1 Pro (Moonshot AI) ma 65,7 w Terminal-Bench 4.0, tuż za Claude Opus 5.5 z wynikiem 66,4 (tabela samego Moonshot), a jego API kosztuje połowę tego, co Opus. W niezależnym rankingu Artificial Analysis jest 4. ogólnie, ok. 2 $ za zadanie wobec ok. 6 $ za Opusa. Ale w tym samym rankingu Claude Sonnet 5.5 ma o punkt więcej przy tej samej cenie za token (2 $ / 10 $ za 1 mln).

Nie zmieniaj modelu przez post. Sprawdź go na swojej pracy.

## Test (ok. 10 minut)

1. Weź JEDNO prawdziwe zadanie z tego tygodnia (funkcja do poprawy, raport, dane do uporządkowania). Nie pytanie z benchmarku.
2. Otwórz [OpenRouter](https://openrouter.ai) i uruchom prompt zadania dwa razy, z tymi samymi danymi: raz na `moonshotai/kimi-k3.1-pro`, raz na Claude Sonnet 5.5 (dokładne ID modeli sprawdź na liście w OpenRouter).
3. Wklej obie odpowiedzi do nowej rozmowy z promptem sędziego, na ślepo (nazwij je A i B).
4. Porównaj: ocenę sędziego, ile musiałeś poprawić ręcznie i koszt każdego uruchomienia (OpenRouter → Activity).

## Prompt zadania

```
Robisz dla mnie prawdziwe zadanie. Kontekst: <wklej pliki / dane / brief>.
Zadanie: <jak wygląda gotowe, jednym zdaniem>.
Ograniczenia: <format, długość, narzędzia, czego unikać>.
Zanim odpowiesz, wypisz założenia, które musiałeś przyjąć. Potem podaj tylko gotowy wynik.
```

## Prompt sędziego (na ślepo)

```
Poniżej są dwie odpowiedzi, A i B, na to samo zadanie. Oceń każdą w skali 1–10 za:
poprawność, kompletność, trzymanie się ograniczeń i ile trzeba poprawić, zanim da się jej użyć.
Zacytuj największy błąd w każdej. Potem jednym zdaniem napisz, którą byś oddał.
Zadanie: <prompt zadania>
A: <odpowiedź 1>
B: <odpowiedź 2>
```

## Zasada

Jeśli tańsze uruchomienie daje ten sam wynik bez dodatkowych poprawek, przenieś to zadanie. Resztę zostaw. Niska cena za token to nie niski rachunek: koszt zadania zależy od tego, ile tokenów zużyje model, więc porównuj prawdziwy rachunek.

Źródła: zobacz [README.md](README.md).
