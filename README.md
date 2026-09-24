# Guess the Career

Gissa fotbollsspelaren utifrån deras karriärstatistik – i Wikipedia-stil.

🔗 **Live:** [guess-the-career.vercel.app](https://guess-the-career.vercel.app)

## Vad är det?

Ett webbaserat gissningsspel där du får se en spelares karriärtabell (klubbar, säsonger, matcher, mål) presenterad som en Wikipedia-infobox, och ska gissa vem spelaren är innan tiden tar slut.

## Funktioner

- ⏱️ 15 sekunders timer per omgång, med snabb rundövergång
- 🔍 Autosök med matchning mot för-/efternamn (hanterar även isländska specialtecken)
- 🏆 Streak-räknare (aktuell + längsta streak, sparad per användare)
- ⚽🔥🌟🐐 Eskalerande streak-emoji vid 3/5/7/10 i rad
- 🎯 Klubb-baserad filtrering (expanderbar liga → klubb-lista, minst 5 klubbar krävs för att filtret ska aktiveras)
- 🟢 **Easy Mode** – bara de ~20% mest kända spelarna i de största klubbarna, ingen filtrering
- 🔐 Google-inloggning (Supabase Auth)
- 🌍 Landsflagga per användare (auto-detekterad via IP)
- 🏅 Leaderboard med guld/silver/brons, worldwide eller filtrerat per liga/klubb
- 👤 Klickbara profiler i leaderboarden – visar en persons topp 3 bästa ligor
- 🧠 "Easiest player" / "Hardest player" – uppdateras live baserat på communityns gissningar
- 📊 Personlig profilsida med total progress, per-liga-statistik, och möjlighet att byta visningsnamn

## Status

🚧 **Under aktiv utveckling.**

**Ligor med spelardata (2778 spelare totalt):**
- Premier League
- La Liga
- Serie A
- Bundesliga
- Ligue 1
- Allsvenskan

**Kvar att göra:**
- Fler ligor
- Apple-inloggning
- Dagligt streak-system ("Se svar"-token)
- Egen domän 
- Google AdSense

## Köra lokalt

Öppna `index.html` i valfri webbläsare. Ingen installation krävs — spelet är en fristående HTML-fil.

## Tech stack

- HTML/CSS/JavaScript (vanilla, inga ramverk)
- [Supabase](https://supabase.com) för databas, autentisering, och realtidsdata
- Hostat på [Vercel](https://vercel.com)
