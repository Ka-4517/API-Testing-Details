Q.3. How to set CRON pattern?
cron is the time-based job scheduler in Unix-like computer operating systems. 
cron enables users to schedule jobs (commands or shell scripts) to run periodically at certain times, dates or intervals. 
It is commonly used to automate system maintenance or administration.

# ┌───────────── minute (0–59)
# │ ┌───────────── hour (0–23)
# │ │ ┌───────────── day of the month (1–31)
# │ │ │ ┌───────────── month (1–12)
# │ │ │ │ ┌───────────── day of the week (0–6) (Sunday to Saturday;
# │ │ │ │ │                                   7 is also Sunday on some systems)
# │ │ │ │ │
# │ │ │ │ │
# * * * * *

1. Jenkins > Configure > Build Triggers > Build periodically
2. */1****    -> Execute every min & update.Run build
3. 

Q.4. How to generate newman advance html report in Jenkins?
