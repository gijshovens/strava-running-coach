# Running Coach (Strava)

A Claude skill that builds a personal running training plan from your own
Strava data, then keeps adjusting it as you train.

## What it does

- Reads 12 months of your Strava runs: volume, consistency, races, heart rate.
- Works out your real max heart rate and checks it for watch or strap glitches
  before using it. It doesn't just apply an age formula.
- Sets your heart-rate and pace zones and checks them with you before
  planning anything.
- Builds a week-by-week plan around the days you can actually run, for any
  goal from a first 5K to an ultra, or general fitness with no race.
- Makes a race-day pacing plan from how you've raced before: whether you
  start slow, fade, or kick.
- Publishes the plan as a web page that opens on your next session, so it's
  quick to check on your phone.
- Checks Strava after your runs (on a schedule, or whenever you ask) and
  adjusts the next one or two weeks.

## What you need

- Claude with skills enabled.
- The **Strava connector**, connected in Claude. The skill won't run without it.
- Optional: a Claude Project for the plan. The plan and check-in history are
  kept there between chats.

## Install

**In the Claude app (web, desktop, mobile):**

1. Download [`running-coach.zip`](running-coach.zip) from this repo.
2. In Claude, open **Customize > Skills** and upload the zip.
3. Make sure the skill is switched on.

**In Claude Code:** copy the `running-coach` folder into `~/.claude/skills/`.

## Use

Start a chat and say something like:

> "Build me a training plan for the Rotterdam Marathon using my Strava data."

Claude asks a quick health check, then your goal, target date and available
days. It pulls your data and shows you its read of your fitness and zones.
You confirm or correct those before it writes the plan.

## Good to know

- This is training guidance, not medical advice. If you have a heart
  condition, are pregnant or are injured, check with a doctor first.
- Your plan page is private to you until you share it.
- If you want sessions on your watch, the skill checks whether your watch can
  import workouts. If it can't, you get step-by-step workouts to enter by hand
  in your watch's app.

## Repo contents

- `running-coach/SKILL.md`: the skill itself
- `running-coach.zip`: the same folder, zipped for upload

## License

MIT. See [LICENSE](LICENSE).
