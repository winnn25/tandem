# Tandem

Health checks for astronauts who can't call a doctor.

Built for the 2026 NASA Space Apps Challenge: *Create Health Monitoring Software for Astronauts on Space Missions*.

**Live app:** https://tandem-beta-snowy.vercel.app

## What it does

On a long mission, astronauts have to notice their own health changes. Tandem helps them do that in a two-minute morning check-in.

- **Checks the readings that matter in space.** Heart rate, blood pressure, oxygen, temperature, blood sugar, sleep, exercise, food, water and mood. Heart rate and heart rate variability are compared with your own early-mission baseline; the rest are checked against safe ranges.
- **Links the cabin to your body.** Each station module has its own microbe swab. The worst one feeds everyone's immune score, modelled on NASA's ISS microbiome study (OSD-224).
- **Catches the self-read gap.** If you say you feel fine but your signals disagree, or the other way round, Tandem asks a crewmate to take a look.
- **Tells you what to do.** Every flag comes with a plain reason, a short checklist, and a report to the flight surgeon that allows for the signal delay to Mars.

It also has a tappable body map, trend charts, "how to measure" guides, check-in streaks, a crew overview, and day and night modes.

## Try it

Open the live link and tap **Show me in 30 seconds**. Or load a scenario from the Today screen: *Cabin microbe rise*, *Heart drift* or *Quiet week*.

## How it's built

One self-contained HTML file in plain HTML, CSS and JavaScript. There is no backend and no network calls, because a spacecraft can't rely on a server. Data stays in the browser.

## Data and sources

- NASA OSD-224: Whole metagenome profiles of particulates collected from the ISS ([data.nasa.gov](https://data.nasa.gov/dataset/whole-metagenome-profiles-of-particulates-collected-from-the-international-space-station-c8f80))
- NASA OSD-466: Microbiome of mice flown on Rodent Research 10 ([data.nasa.gov](https://data.nasa.gov/dataset/microbiome-profiling-of-feces-from-mice-flown-on-the-rr-10-mission))
- Be et al., *Microbiome* 5, 81 (2017) and Singh et al., *Microbiome* 6, 204 (2018)

Full references are on the app's info screen.

## Please note

This is a prototype. The crew and their readings are simulated, and the thresholds are demo values a flight surgeon would set for real. It is not a medical device.

Built with help from Claude (Anthropic) for planning, code and testing.
