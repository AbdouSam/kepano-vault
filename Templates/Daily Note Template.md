---
tags:
  - daily
---
<%*
const title = tp.file.title;
// Parse the date from the note title (works with or without weekday)
let fileDate = moment(title, ["YYYY-MM-DD-dddd", "YYYY-MM-DD"]);
// Year (clickable link to [[2026]])
const year = fileDate.format("YYYY");
// Month link: points to [[2026-01]] and displays "January"
const monthLink = fileDate.format("YYYY-MM");
const monthName = fileDate.format("MMMM");
// Week number (plain text, no link)
const weekNum = fileDate.format("WW");
// Previous day link (in YYYY-MM-DD format)
const prevDay = fileDate.clone().subtract(1, "days").format("YYYY-MM-DD");
%>
**[[<% year %>|<% year %>]] / [[<% monthLink %>|<% monthName %>]] / Week <% weekNum %>**
[[<% prevDay %>]]
---
# Notes

![[Daily.base]]

#  End of Day Report
## 📜 Quick Day review
  
 _Did  I do all the habits am building/removing?_
> Yes
> stuff

_What did I do well?_
> Workout [[at home]]
> 

_What did I not do well?_  
> Socialize
> Drink enough water

_What can I do better tomorrow / Next time?_  
> Read [[Quran]] more

_Did I do all my Non-Negotiables?_
> I did not set any negotiables
> (Bad or Good?)

_What is the one Leverageable task if I only have 60 minutes to spend on tomorrow, that is ideal and actionable for me to get closer to my goal tomorrow?_  
> Learn business
> Other Stuff

Closing Thoughts
> Nothing specific

# ⏭️ Next Day

🎯 **1-3 To Dos for Next Day**  

1. a
2. b
3. c

-------------------------------------------------------------------
**Agenda (Follow to the T.):**  

1. Review your Weekly Goals, daily.
2. Define the daily goals for the next day
3. Prepare all the tasks for the next day, eliminate friction
4. Clear out undone tasks & tie loose ends
5. Shut OFF from brain activating tasks!