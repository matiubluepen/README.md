# COMP 1080SEF GROUP PROJECT
## default testing data
these data are preset as the testing data

default user accounts (username, password)
- s1410346, 12345
- s1427615, 12345678
- s1388048, vip888

attendance text file (e.g. s1388048_attend.txt)
65	← total classes in a term
0:0	← classes had : classes attended
0	← total tokens used
0	← number of $5 coupons
0	← number of $10 coupons

class schedule text file (e.g. s1388048_schedule.txt)
11~28~09:00-10:50~COMP1080SEF L01~JCC D0212	← a line in text file
month~day~time~course~venue
(lessons recorded only contains October and November)

(The three testing accounts are planned to be created by the school side, and at the same time the attendance and schedule text file are planned to be created when the account is created. Therefore, only these three accounts are available for testing the functions of the system.)
each account has two text file, attend.txt and schedule.txt
for the whole system and testing cases, 7 text files and one python file are needed

## testing the system
In the system, most of the functions are chosen by inputting their according numbers to run the corresponding function. If there is invalid input, the system will get back to the previous page.
Also, the system can't run smoothly if it is run by IOS/MacOS, since the command os.system("cls") (clear screen) can't be found with using IOS/MacOS system.

### login page
there are create account, login and exit

create account: accounts can be created, but can't be used for the main system functions.
login: input both the username and password correctly to get into the main menu
exit: end the system

### attendance taking
it is used for making data for attendance calculations. Not expected to be used as a formal attendance taking function.

press "yes" or "no" to choose whether you have attended a lesson or not.
it will affect the "class had" and class attended" in attend.txt

### attendance calculator
it will show the total attendance of the users, and can exchange coupons through tokens gained through attending classes.

trade system:
tokens haved = classes attended / total classes in a term
(70% attendance = + 10 tokens, 80% attendance = + another 10 tokens)
$5 coupons = 20 tokens
$10 coupons = 35 tokens

### navigation
it is used for users to find out the distance and travel time of their origin and destination

the starting point and the detination have to be input by the user (e.g. hkmu, jcc)
and choose the travel mode (walk, public transport, drive)
then a link to Google Map will be generated. users can click on it and find out the info. they want

### timetable
user's schedule will be read through schedule.txt. the events will be shown on a 2025 calendar.
the text file only contains October and November events of the user.

(the calendar is displayed according to the terminal size. therefore, full screen is recommended. and the events may not be fully shown because of the size of the cells)

users can switch month (Jan-Dec), add events, view events, and back to main menu
add events: users can choose a date, add their own events by typing it themselves (e.g. 9:30-11:30COMP exam) (can't input the symbol "~")
view events: users can choose a date, and view all the events through an ordered list
