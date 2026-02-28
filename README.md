LP Run Lap Counter

Live Tool:
https://petesimple.github.io/lplapcounter/

A simple, mobile friendly lap counter and split timer built specifically for the LP Run.

This is for the person in the stands.
The one counting.
The one yelling splits.
The one trying not to lose track at lap 23.

Tap once per lap.
Timer runs.
Splits save.
Share instantly.

No login. No backend. No nonsense.

⸻

What It Does

Built for the 33:20 LP Run format.
	•	Stopwatch with countdown
	•	One big Start button
	•	One big Lap button
	•	Auto lap splits
	•	Total lap count
	•	Distance calculation
	•	Average lap pace
	•	Undo last lap
	•	Share via native phone Share Sheet
	•	CSV export
	•	Auto saves progress if the page refreshes
	•	Uses real clock time so the timer stays accurate if the page is backgrounded or reopened later

Works great on iPhone and Android.

⸻

Default Settings
	•	Event Duration: 33:20
	•	Lap Length: 400 meters

Both editable if needed.

⸻

How To Use
	1.	Open the link.
	2.	Add runner name if you want.
	3.	Hit Start at the gun.
	4.	Tap Lap every time they cross.
	5.	Hit Share when done.

If you miss one:
	•	Tap Undo Lap
	•	Keep rolling

No panic required.

⸻

Background Timing

This app is built so the timer stays accurate even if the page is no longer visible.

That means if someone switches apps, locks the phone, or comes back later, the elapsed time and countdown will catch up correctly using real wall clock time.

A couple reality checks:
	•	You still cannot tap Lap while the page is hidden
	•	The display does not visibly animate while backgrounded
	•	But when you come back, the timer tells the truth

Which is really what we need from a lap counter and from a friend.

⸻

Sharing

When you hit Share, it tries to:
	1.	Share summary + CSV file through the native Share Sheet
	2.	Share text summary
	3.	Fall back to:
	•	copying summary to clipboard
	•	downloading CSV

CSV format:

lap,split_ms,split,total_ms,total

Perfect for:
	•	Google Sheets
	•	Rankings
	•	Post race flexing
	•	Data nerd conversations

⸻

Why I Built This

The LP Run format puts lap counting responsibility on the runner or a companion.

This tool removes:
	•	clipboards
	•	separate stopwatches
	•	guessing
	•	“Wait was that 26 or 27?”

It keeps the stands organized and the vibes intact.

⸻

Tech
	•	Single HTML file
	•	Vanilla JavaScript
	•	No dependencies
	•	Runs entirely in the browser
	•	Hosted on GitHub Pages
	•	Uses localStorage to preserve state between refreshes

⸻

Future Add Ons
	•	Big Glare Mode
	•	Audio beep on lap
	•	Multi runner tracking
	•	Distance projection during run
	•	LP themed UI

⸻

License

MIT

Use it. Fork it. Improve it. Share it.
