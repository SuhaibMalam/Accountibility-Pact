# Accountability Pact: Rules

These are the decisions the code and the database are built on. If a rule changes, change it here first.

## 1. What makes a pact "broken"?
A pact is BROKEN when a week ends (Sunday, IST) with fewer valid study days than the pact's weekly quota; idle days alone only trigger nudges and buddy alerts.

## 2. What is a week and a day?
A week runs Monday to Sunday and a day is a calendar day in IST (UTC+05:30), with all timestamps stored in UTC and converted to IST only in the logic layer.

## 3. What is a valid session?
A session is valid when its duration is at least the pact's minimum minutes and its note is not empty.

## 4. Where does "lessons completed" come from?
Each session stores its own `lessons_completed` number, and a pact's completed lessons is the sum of that field across its valid sessions, so the total is always computed and never stored on the pact.
