# guess-the-career
# Guess the Career

Gissa fotbollsspelaren utifrån deras karriärstatistik – i Wikipedia-stil.

## Vad är det?

Ett webbaserat gissningsspel där du får se en spelares karriärtabell (klubbar, säsonger, matcher, mål) presenterad som en Wikipedia-infobox, och ska gissa vem spelaren är innan tiden tar slut.

## Funktioner

- ⏱️ 15 sekunders timer per omgång
- 🏆 Streak-räknare
- 🎯 Filtrera på liga/klubb
- ✅ Completionist-tracking (vilka spelare du redan klarat)
- 📊 Leaderboard (mock-data just nu, riktig backend på gång)

## Status

🚧 **Under aktiv utveckling.** Detta är fortfarande en prototyp.

Fungerar redan:
- Kärnspelet (gissa, timer, streak)
- Speldata för Premier League, delar av La Liga och Bundesliga

Kvar att göra:
- Riktig inloggning (Google/Supabase) — just nu simulerad
- Riktig leaderboard — just nu genererad slumpdata
- Fler ligor och klubbar
- Egen domän och lansering

## Köra lokalt

Öppna `index.html` i valfri webbläsare. Ingen installation krävs — spelet är en fristående HTML-fil.

## Tech stack

- HTML/CSS/JavaScript (vanilla, inga ramverk)
- Planerad backend: [Supabase](https://supabase.com) för auth och leaderboard
