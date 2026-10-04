# Guess the Career

Gissa fotbollsspelaren utifrån deras karriärstatistik, i Wikipedia-stil.

🔗 **Live:** [guess-the-career.vercel.app](https://guess-the-career.vercel.app)

## Vad är det?

Ett webbaserat gissningsspel. Du får se en spelares karriärtabell (klubbar, säsonger, matcher, mål) presenterad som en Wikipedia-infobox och ska gissa vem spelaren är innan tiden tar slut.

## Funktioner

**Spelet**
- ⏱️ 20 sekunder per omgång, med snabb övergång mellan rundorna
- 🔍 Autosök som matchar för- och efternamn (hanterar även isländska specialtecken)
- 🎯 Filtrering per klubb: expandera en liga och välj enskilda klubbar eller hela ligor. Minst 5 klubbar krävs för att filtret ska gälla
- 🟢 **Easy Mode**: bara de ~20 % mest kända spelarna i de största klubbarna, utan filtrering
- 🏆 Streak: aktuell och längsta, med märken vid 3, 5, 7 och 10 i rad (⚽ 🔥 🌟 🐐)

**Community**
- 🔐 Google-inloggning (Supabase Auth). Gäster kan spela men får ingen sparad progress
- 🏅 Leaderboard med guld/silver/brons, worldwide eller filtrerat per liga och klubb
- 🌍 Landsflagga per användare
- 👤 Klickbara namn i leaderboarden visar personens tre bästa ligor
- 🧠 "Easiest player" och "Hardest player", beräknade från communityns gissningar
- 📊 Personlig profil med total progress, per-liga-statistik och visningsnamn

## Fusksäkring

Svaren rättas på servern, inte i webbläsaren:

- Spelarnas svar och namn skickas aldrig till webbläsaren. Autosök använder en ren namnlista utan koppling till karriärtabellerna.
- Spelar-id:n är slumpade, så de avslöjar inte namnet.
- Gissningar skickas till en databasfunktion (`submit_guess`) som kontrollerar svaret, sparar progress och räknar streaken.
- Servern håller reda på vilken spelare du fått och hur lång tid rundan tagit.
- Max 20 felgissningar per minut och användare.
- Poäng, streak och gissningar går inte att skriva direkt från webbläsaren. Row Level Security och kolumnrättigheter är på.

## Data

- ~2 800 spelare i sex ligor: Premier League, La Liga, Serie A, Bundesliga, Ligue 1 och Allsvenskan
- Karriärdata hämtas från Wikipedia via ett Python-skript

## Kvar att göra

- Anonym inloggning för gäster
- Apple-inloggning
- Dagliga utmaningar och dagliga streaks
- Privacy policy och cookie-banner
- Egen domän (disco.games)
- Fler ligor och klubbar
- Annonser och premium-konto

## Tech stack

- HTML, CSS och JavaScript (vanilla, inga ramverk), en fristående `index.html`
- [Supabase](https://supabase.com): Postgres, autentisering och databasfunktioner
- [Vercel](https://vercel.com): hosting, med automatisk deploy vid push till `main`

## Köra lokalt

Öppna `index.html` i en webbläsare. Spelet pratar direkt med Supabase, så ingen lokal server eller installation behövs.