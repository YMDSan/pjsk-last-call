# PJSK Last Call

**Never miss free crystals — a deadline dashboard for Project Sekai, on EN, JP and CN.**

> **AI use declaration:** this is a completely vibe-coded tool. Every part of it — the code, the
> design decisions, this README — was heavily AI-assisted.
>
> **However, it is also actively used by the author**, on desktop, across three servers. Every
> timing rule in it was verified against a live game client, so all core functions should be
> running correctly.

Like any gacha game, crystals are hard to come by. For the author, who for some reason decided to
play three servers at once, collecting all of them is very much a hassle. This tool aims to help
the author — and hopefully you — collect the easy crystals that are prone to expiring, the ones in
virtual shows, item exchanges and event stories, across every server you play, in an
information-dense format.

It is a dashboard you glance at, not a to-do list you process. Tick something off when you have
dealt with it — or when you have decided you do not care — and it stops competing for your
attention until the next event.

![PJSK Last Call showing the EN, JP and CN columns side by side](docs/screenshot.png)

## Using it

**Online — <https://ymdsan.github.io/pjsk-last-call/>** — nothing to install.
**Recommended for mobile users.**

> **No artwork on the website.** The event and gacha banners come from
> [sekai.best](https://sekai.best), which blocks its images from being shown on other websites, so
> they cannot load at ymdsan.github.io and the artwork switch is greyed out there. Everything else
> works the same. If you want the banners, use the downloaded file below.

**Offline — download `index.html` and open it.** One self-contained file: no dependencies, no build
step, no server. It runs straight from a `file://` path, which makes it easy to keep in a folder,
edit, or carry on a USB stick. It is also the only way to see the artwork. Best suited to desktop,
and **not recommended on mobile** — opening
a downloaded `.html` file on a phone is awkward, with no clean way to launch it, and most mobile
browsers lose the file once you close the tab or restart the browser, so you end up digging through
your downloads every time.

**Add it to your home screen** (recommended alongside the online version). On iOS: Share → Add to
Home Screen; it then launches full-screen, without browser chrome. On Android: browser menu → Add
to Home screen, which gives you a one-tap shortcut.

> The shortcut still needs a connection to load the page itself. Your cached deadline data survives
> offline, but the page does not yet — **proper offline support is in development.**

On first run it asks which server you play, offers a preset for how much detail you want, lets you
set the theme and density, and shows what the initial download costs. Nothing is fetched before you
answer. If you don't spend money on the game, it recommends the Free-to-play preset. You can open it
again any time from Settings → Testing & setup.

![The first-run setup wizard](docs/wizard.png)

## What it shows

For your current event on each selected server:

- **Event ends** — the grind cutoff.
- **Bonus missions** — every bonus mission of the event, in the game's own wording (reading the last
  story episode is one of them), as a checklist folded away under one row, with "x/y complete" on
  the fold. They stay open until the event *closes*, which is up to two days after the grind cutoff
  depending on the server, so the row counts down to that. Ticking the row ticks every mission.
- **Item exchange** — worth at least 500 easily-obtained crystals every event, and the deadline is
  8–10 days later than most people assume.
- **Last virtual show** — the easiest thing to miss. Shows run as a roughly one-day burst, not for
  the whole event.
- **Stamp missions and shops** — collaboration and anniversary stamp missions, page by page, and
  limited-time exchange shops before they close.
- **Event gacha** and every concurrent banner, folded away by default.
- **Extras** — the monthly mission pass (buying it, finishing it, and a progress advisor), your
  first three ranked matches of the season, the CN weekly badge exchange, EN's weekly missions (a
  folded checklist that resets every Monday at 04:00 Pacific time), and paid Connect Live concerts.

Every row can be switched off in Settings, and presets set them in one click: **Show everything**,
**Hide all gachas**, or **Free-to-play** (hides everything that needs real money). Presets combine,
and you can save up to three of your own.

## Setting it up

Everything below can be changed later from **⚙ Settings** — nothing here is permanent. Settings is
split into four folding sections (Basics, What's shown, Time & data, Testing & setup), the **?**
buttons explain each part, and it remembers which sections you left open. On a wide screen the
sections sit in two columns.

**Servers.** Pick one to start. Each one you add is a separate column that loads independently, so
a server having a bad day never blanks the others. Columns fit as many across as your window
allows and stack when it gets narrow — two servers sit side by side on a fairly small screen, at
the same slim width three would use.

**Row presets.** These decide how much is on screen. The default shows everything; the **?** next
to the heading explains exactly what each preset hides.

- **Show everything** — every row visible, the default.
- **Hide all gachas** — hides the event gacha and the other-gachas list, which are about *spending*
  crystals rather than collecting them. Virtual shows stay, because they pay out crystals or wish
  pieces either way.
- **Free-to-play** — hides everything that needs real money: the two mission-pass rows, paid
  Connect Live shows, banners that take only paid crystals or need Colorful+, and the Colorful+
  options in the mission-pass advisor. Recommended if you don't spend money on the game.

They combine, and every individual row stays switchable afterwards.

**Theme.** Light, dark, or follow your system. Dark is the original; the light palette was rebuilt
from scratch rather than lightened, because the urgency colours stop working on a pale background.

**Density.** *Compact* is the default and fits noticeably more within the same screen real estate;
*Comfortable* is roomier if you prefer the space. Compact is not just tighter spacing — it drops
the server-time line and shortens the virtual-show block.

**Server time.** Shows each server's own local clock beside your own, which is useful for
double-checking a deadline against what the game itself displays. **Requires Comfortable density** —
compact hides it to save width, and says so when you look for the setting.

**Dates.** Shown in English by default. Settings can switch them to your system's own format, and
the Clock setting picks 12- or 24-hour.

**Artwork (downloaded file only).** Comfortable view can show each event's banner and the gacha
banners, loaded from the community-run [sekai.best](https://sekai.best) asset mirror. You are asked
when you switch to it. Compact stays text-only, so it doubles as a data saver. On the website the
switch is greyed out, because sekai.best blocks its images from being shown on other websites.

**Time travel.** Under *Testing & setup* in Settings. It shows the page as it would look at another
date and time, which is handy for checking what a deadline will look like before it arrives.
Nothing you tick while it is open is saved.

**Data.** A refresh is a few hundred kilobytes. Gacha timing and crystal amounts are the only large
downloads, and each only happens when you ask, after a prompt telling you the exact current size.
You can raise the threshold or turn the prompt off entirely.

## Reading the screen

Countdowns tick live, at the precision that still matters: seconds under a day, hours under three
days, days beyond that. Anything within **three days** gets a coloured chip — red under a day, orange
under three — and everything further out stays quiet grey text. The chip is the signal: if you see
one, something needs attention soon.

The badge beside each event says where it stands: **live** while the event runs, **wrapping up**
once it has ended but something is still open (usually the item exchange), and **ended** when
nothing is left. Before an event it counts server days ("starts next server day"), since the game's
day rolls over at 04:00 server time, not at your midnight.

**Stamp missions and shops.** Collaboration and anniversary stamp missions get their own block,
with a countdown and a button per page to tick it off; once every page is ticked, the countdown turns
into "✓ done" like any other finished row. Limited-time exchange shops are listed there too, with
their closing dates.

**Mission pass.** Under Extras, drag the slider to your live mission points and the tool says
whether you are ahead (and when you would finish), on track, or need to catch up (and by how much a
day). "What if I buy Colorful+ now?" shows the same with double points from today (Free-to-play
hides the Colorful+ parts). Paid Connect Live concerts are listed there too: a countdown to the
first show, "ongoing" while one is on, then the time to the next or last rerun.

**No full pity saved?** Tick "I don't have the equivalent of 90,000 crystals saved" in the gacha
section (exchange tickets count) and the banners that take free crystals move into a separate,
folded list, with a short reminder about the hard pity before it opens. What stays in the main list
is labelled "Free & paid-only gachas": the banners that never touch your free crystals.

**Crystal badges.** Press **💎 Load crystal amounts** at the top of a column and each task shows what
it is worth, straight from the game's own reward data: "💎 500" beside the item exchange, "💎 300"
beside the virtual show, each bonus mission's own amount (the story mission counts the episodes'
crystals too), the free track of the mission pass, and the ranked season's range. The final bonus
mission reads "up to 100", since 100 crystals is one of the rewards you can pick. A badge greys out
once you tick its row. The download is about 1.2 MB on EN, 1.4 MB on JP and 0.4 MB on CN, once; it is
kept, and the button then shows its age so you can refresh it. You can switch the badges off in
Settings.

**Calendar.** Each deadline has a **+cal** link that opens a pre-filled Google Calendar entry you
can edit before saving. **Export to calendar** at the bottom of a column puts several at once into
one file for Google Calendar, Apple Calendar or Outlook. You pick the entries, rename them if you
like, and choose the reminders.

Tick a row when you have dealt with it, or when you have decided you do not care. It greys out and
stops competing for attention. Check-offs are keyed to the specific event, season or month, so they
clear themselves when the next one starts. Once every row for an event is ticked, the tool offers
to move you to the next event.

## Things worth knowing

**Event and gacha names appear in the server's own language.** A JP event shows its Japanese name,
because that is what your game client shows you. This is deliberate — matching your client is the
point, and translating it would make cross-checking harder.

**Data use is small, and it tells you before it isn't.** A full refresh is a few hundred kilobytes.
Gacha timing and crystal amounts are the only large downloads — gacha timing about 2.8 MB on EN,
3.4 MB on JP, 322 KB on CN; crystal amounts about 1.2 MB, 1.4 MB and 0.4 MB — and each only happens
when you ask for it, after a prompt showing the exact current size. You can set the threshold, or
turn the prompt off, in Settings.

**Everything stays on your device.** There is no account, no server, no analytics. Your settings
and check-offs live in your browser's local storage, which also means they do not sync between
devices, and clearing site data clears them.

**v1 covers EN, JP and CN.** TW and KR mirrors exist and the code is ready for them, but every
timing rule here was verified against a live client, and the author does not play those two. They
will be added once the details can be confirmed rather than guessed.

## Feedback

**[Send feedback — no account needed](https://forms.gle/6v2fyvQp7VQJujkE6)**. That is the main
channel, and the form is deliberately login-free so anyone can use it.

If you do have a GitHub account, [Issues](https://github.com/YMDSan/pjsk-last-call/issues) work
too and are easier to have a back-and-forth in. Either is fine — bug reports, wrong times, missing
deadlines, and "this was confusing" are all useful.

## Data source

Timing data comes from the community-maintained [Sekai-World](https://github.com/Sekai-World)
master-database mirrors, fetched directly by your browser at runtime. This project does not
redistribute game data, and is enormously indebted to that project for keeping the mirrors current.

## Roadmap

- **TW and KR servers.** The mirrors exist and the code is ready for them; what is missing is
  verification against a live client, which needs someone who actually plays them.
- **Works offline once installed.** Cached deadline data already survives with no connection, but
  the page itself still needs one to load.
- **More interface languages.** The groundwork is done — every string is already in one table, so
  adding a language is translation work rather than code work.
- **Opening up contributions**, including publishing the test suite and the design notes that
  explain why several "obvious" data choices here are wrong.

## Development

The tool is `index.html` — one file, vanilla JS and CSS, no build step and no dependencies. That is
a hard constraint rather than an accident: it is what lets it run straight from a `file://` URL with
no server, and keep working offline.

There is a jsdom test suite covering the parts that are easy to get quietly wrong — the DST-exact
server-day maths, the verified field mappings, the check-off behaviour — but it is not published
yet. Until it is, the feedback form and Issues are the best way to report something.

## Licence

[MIT](LICENSE) for the code.

---

**Unofficial fan project.** PJSK Last Call is not affiliated with, endorsed by, or sponsored by
SEGA Corporation, Colorful Palette Inc., or Crypton Future Media. *Project SEKAI COLORFUL STAGE!
feat. Hatsune Miku* and all related names, characters, and assets are trademarks of their
respective owners. This tool displays scheduling data fetched at runtime from the
community-maintained [Sekai-World](https://github.com/Sekai-World) master-database mirrors; it
does not redistribute game data or assets.
