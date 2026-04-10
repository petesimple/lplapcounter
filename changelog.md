Changelog April 10, 2026

Upcoming

LP Run Lap Counter
	•	Added club affiliation as a real submitted field instead of hiding it only in notes
	•	Added automatic Finish tab generation in Google Sheets from incoming race data
	•	Added special awards extraction in Finish
	•	Overall Winner
	•	Masters Winner
	•	Clydesdale 1 and 2
	•	Rubens 1 and 2
	•	Added age group sorting inside Finish
	•	Added team totals based on Club Affiliation
	•	Added Archive tab workflow for older data when needed
	•	Confirmed current live testing path uses three spreadsheet tabs
	•	2026 for raw intake
	•	Finish for organized finish processing
	•	Archive for older data storage
	•	Need live testing against Jim’s real workflow to confirm that the spreadsheet logic matches his existing sorting method
	•	Need outlier testing
	•	unusual distances
	•	missing partials
	•	odd age group edge cases
	•	club scoring edge cases
	•	duplicate submissions
	•	Consider whether team scoring should count all club runners or only top N scorers
	•	Confirm whether overall and special award winners should be removed from age groups or still appear there
	•	Confirm whether masters should always mean age 40+
	•	Reset button should fully clear all runner and race state, not preserve fields from the prior run

Spreadsheet / Apps Script
	•	Added Club Affiliation column to the raw intake structure
	•	Updated Apps Script payload handling to accept clubAffiliation
	•	Updated buildRow(payload) to store Club Affiliation
	•	Added automatic Finish tab rebuild after new submission
	•	Added automatic Finish tab rebuild after partial save
	•	Need continued validation that deployed Apps Script version matches latest source after each update

General testing notes
	•	Test with clean new entries only
	•	Compare 2026 raw intake against Finish output
	•	Compare actual outcomes against Jim’s email-described sort flow
	•	Gather feedback from Jim on what feels right, what feels wrong, and what needs to change

Notes
	•	Current spreadsheet share link is maintained separately for testing and review
	•	Redeploying the Apps Script web app is required after script changes or the live endpoint may still use older logic
