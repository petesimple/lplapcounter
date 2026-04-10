# LP Run Lap Counter

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
Submit to the sheet.  
Share instantly.

No login. Minimal friction. Built to be useful.

## What It Does

Built for the 33:20 LP Run format.

1. Stopwatch with countdown
2. One big Start button
3. One big Lap button
4. Auto lap splits
5. Total lap count
6. Distance calculation
7. Average lap pace
8. Undo last lap
9. Finalize workflow for partial distance after the horn
10. Share via native phone Share Sheet
11. CSV export
12. Auto saves progress if the page refreshes
13. Uses real clock time so the timer stays accurate if the page is backgrounded or reopened later
14. Submits results to Google Sheets
15. Supports club affiliation for team scoring
16. Auto assigns lane based on age and division

Works great on iPhone and Android.

## Current Event Logic

The app is set up around the LP Run workflow and currently includes:

1. Event duration default of 33:20
2. Automatic lane assignment
   1. Rubens and Clydesdale use Lane 1
   2. Age 40 and up uses Lane 1
   3. Under 40 uses Lane 5
3. Fixed lap distance by lane
4. Partial distance entry after the horn
5. Finalize before submit so the official result does not drift after time expires

## Default Settings

1. Event Duration: 33:20
2. Lane 1 distance: 1312.3 feet
3. Lane 5 distance: 1400.9 feet
4. Club affiliation default: NA - No Affiliation

## How To Use

1. Open the link.
2. Enter runner name.
3. Enter age.
4. Choose division.
5. Confirm sex and club affiliation.
6. Hit Start at the gun.
7. Tap Lap every time the runner crosses.
8. When time expires, enter the partial distance after the horn.
9. Finalize the result.
10. Tap Submit + Share.

If you miss one:

1. Tap Undo Lap
2. Keep rolling
3. No panic required

## Finalize Flow

When time runs out, the app prompts for the partial lap distance after the horn.

That value is used to complete the official result before submission.

The finalize flow is there to prevent the classic post race problem:

"Wait, were they 200 feet past the line or 300?"

You can:

1. Finalize with an entered partial
2. Finalize with 0 partial if needed

Once finalized, the result is treated as official for submission and sharing.

## Google Sheets Workflow

The app submits results to a Google Sheet backend.

Current spreadsheet structure includes three main tabs:

1. `2026`  
   Raw intake tab where app submissions land first

2. `Finish`  
   Organized finish processing tab for cleaner review and sorting

3. `Archive`  
   Storage for older data when needed

The sheet currently supports:

1. Raw submission capture
2. Club affiliation as a dedicated field
3. Automatic Finish tab rebuild
4. Special awards extraction
5. Age group sorting
6. Team totals by club affiliation

## Finish Tab Logic

The `Finish` tab is designed to move toward Jim's working method.

Current logic includes:

1. Women section
2. Men section
3. Open or Other section if needed
4. Special awards extraction, including:
   1. Overall Winner
   2. Masters Winner
   3. Clydesdale 1 and 2
   4. Rubens 1 and 2
5. Age group sorting
6. Team totals based on Club Affiliation

This is still intended to be tested against real edge cases and refined from actual use.

## Background Timing

This app is built so the timer stays accurate even if the page is no longer visible.

That means if someone switches apps, locks the phone, or comes back later, the elapsed time and countdown will catch up correctly using real wall clock time.

A couple reality checks:

1. You still cannot tap Lap while the page is hidden
2. The display does not visibly animate while backgrounded
3. But when you come back, the timer tells the truth

Which is really what we need from a lap counter and from a friend.

## Sharing

When you hit Submit + Share, it tries to:

1. Save the result to Google Sheets first
2. Share summary and CSV through the native Share Sheet
3. Share text summary if file sharing is not available
4. Fall back to:
   1. copying summary to clipboard
   2. downloading CSV

CSV output includes lap and timing data suitable for later analysis.

Useful for:

1. Google Sheets
2. Rankings
3. Post race flexing
4. Data nerd conversations
5. Figuring out exactly where everything went beautifully or terribly

## Reset Behavior

The Reset button is intended to clear everything for the next runner.

That includes:

1. Current timer state
2. Laps
3. Partial distance
4. Runner details
5. Club selection
6. Submission state
7. Local saved state for the current run

In other words, reset should mean reset and not "sort of spiritually reset."

## Why I Built This

The LP Run format puts lap counting responsibility on the runner or a companion.

This tool removes:

1. Clipboards
2. Separate stopwatches
3. Guessing
4. "Wait was that 26 or 27?"
5. Loose scraps of paper trying to become data

It helps keep the stands organized and the vibes intact.

## Tech

1. Single HTML file
2. Vanilla JavaScript
3. No dependencies
4. Runs entirely in the browser
5. Hosted on GitHub Pages
6. Uses localStorage to preserve state between refreshes
7. Uses a Google Apps Script backend for sheet submission
8. Uses JSONP for broad mobile browser compatibility with sheet submission

## Current Testing Focus

1. Confirm results match real LP Run workflow
2. Compare `2026` raw intake against `Finish` output
3. Test edge cases and outliers
4. Validate team scoring behavior
5. Refine sorting based on real race use
6. Confirm spreadsheet logic matches Jim's current method closely enough to be useful

## Future Add Ons

1. Big Glare Mode
2. Audio beep on lap
3. Multi runner tracking
4. Distance projection during run
5. LP themed UI
6. More finish and team scoring options
7. Additional export formats
8. More testing around weird race day outliers

## License

MIT

Use it. Fork it. Improve it. Share it.
