# gm_sorter
sorting class schedules to make trip clusters

## How to use it:
1. In your Google Sheet, select all (Ctrl+A) → Copy (Ctrl+C)
2. Paste into the tool → click Parse Schedule
3. Choose filter options, then Group into Trips

## What it handles automatically:
+ Recognizes course code rows like 16410.12H and uses them as labels for the sessions below
+ Skips any row where Col A = X (Time conflict / Past Cutoff Date) — togglable
+ Optionally skips sessions showing 0 seats
+ Extracts the start date from the 3/20/2026 8:00 AM to 3/20/2026 5:00 PM format in Col B
+ Groups by Training Center name (Col D) by default — you can switch to City+State if you want a looser grouping (e.g., treating Dallas GM and Houston GM as the same "TX" trip isn't helpful here, but city+state helps if you ever want to see all Garland, TX vs all Livermore, CA)

## Each trip card shows:
+ Location, date span, nights on-site
+ Each session: date, course code, seats available
+ ⚠ gap warnings if consecutive sessions have a day off between them
