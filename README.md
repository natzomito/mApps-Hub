# mApps Hub - 100% vibe coded

**Tiny apps for everyday life. Like Shortcuts or macros — but open, portable, and written by AI in a minute.**

mApps are single-file HTML mini-apps: a med reminder generator, a Morse trainer, a 4,600-year-old board game, a unit converter — anything that solves one small problem well. No app store, no accounts, no cloud. mApps Hub is the launcher that holds them all: install it once as a web app on your phone, then import any mApp and it lives on your device.

**Offline by default.** Every imported mApp runs with all network access blocked by a Content Security Policy enforced by the browser itself — it cannot send your data anywhere, even if the code were malicious. You grant internet access per app, explicitly, only if you trust it. Most mApps never need it.

## Install the Hub (iPhone)

1. Open **https://natzomito.github.io/mApps-Hub/** in Safari
2. Share → **Add to Home Screen**
3. Done — the Hub runs fullscreen with its own icon and works offline

On Android, open the same URL in Chrome and use "Install app" / "Add to Home screen".

## Use it

- **+** adds an app: paste HTML code or pick a file from your phone. Set a custom icon from your photo gallery, or let the Hub generate one from the first letter.
- **🧭 (compass icon, top left)** opens the **Discover** catalog — browse every mApp published in this repo and tap **Install** to add it straight to your library. No download-and-import needed; the Hub fetches it for you in your language automatically (falls back to English).
- **Long-press a tile** for actions: pin, hide, edit, allow/block internet, export the HTML, delete.
- **Settings** → backup all apps and icons to a single JSON file, restore anytime, switch language (English/Polish, auto-detected), check for Hub updates, replay the welcome screen (tap "mApps Hub").

First time you open the Hub, a short welcome screen explains all of this — swipe through it or tap Skip.

## Get apps

Easiest way: open the **Discover** tab in the Hub (compass icon) and tap Install — done in one tap, no browser involved.

Prefer to look before you leap? Browse the [`apps/`](apps/) folder on GitHub instead. Each mApp has a `meta.json` (description, tags, languages) and one HTML file per language (`en.html`, `pl.html`, …). Open the file for your language, read the code, and if you like what you see, either install it from Discover or download the `.html` file and import it manually.

Current catalog: see [`catalog.json`](catalog.json).

## Make your own mApp

Ask any LLM (Claude, ChatGPT, Mistral, a local model):

> Create a single-file HTML mini-app that does X. Everything inline (CSS and JS in one file), no external CDNs or network requests, mobile-first, works offline. Persist data in localStorage under a unique key prefix.

Import the result into your Hub. That's the whole workflow — an idea to a working app on your home screen in a few minutes.

## Contribute

**Share an app:** open a Pull Request adding a folder under `apps/your-app-id/` with `meta.json` (see existing apps for the format) and at least `en.html`. Rules: single file, no network calls (or declare `"network": true` in meta.json with a reason), no trackers, readable code.

**Translate:** copy an app's `en.html`, translate the visible strings (an LLM does this in one prompt: *"translate all user-facing strings in this HTML file to <language>, change nothing else"*), and open a PR adding `<lang>.html`. Apps needing translations are flagged in `meta.json` under `translationWanted`.

**Request a translation or an app:** open an Issue.

## License

[EUPL-1.2](LICENSE) — the European Union Public Licence. Free and open source forever: every fork and modification must stay open. Available in 23 languages with equal legal standing.

---

# mApps Hub (PL)

**Małe aplikacje do codziennych spraw. Jak Skróty albo makra — tylko otwarte, przenośne i pisane przez AI w minutę.**

mApps to jednoplikowe mini-aplikacje HTML. Hub to launcher, który je wszystkie trzyma: instalujesz raz jako web-apkę (Safari → Udostępnij → Dodaj do ekranu początkowego), potem importujesz dowolną mApkę i zostaje na Twoim urządzeniu. Bez kont, bez chmury.

**Domyślnie offline.** Każda zaimportowana apka działa z zablokowanym dostępem do sieci (Content Security Policy egzekwowane przez przeglądarkę) — nie może nigdzie wysłać Twoich danych. Internet włączasz per aplikacja, jawnie, tylko dla zaufanego kodu.

Katalog aplikacji: zakładka **Discover** w Hubie (ikona kompasu) — jedno dotknięcie „Zainstaluj" i apka ląduje w bibliotece. Możesz też przejrzeć kod wcześniej w folderze [`apps/`](apps/) na GitHubie. Chcesz dodać własną apkę albo tłumaczenie? Wystaw Pull Request (szczegóły wyżej, w sekcji Contribute). Chcesz poprosić o tłumaczenie? Załóż Issue.

Licencja: EUPL-1.2 — na zawsze otwarte.
