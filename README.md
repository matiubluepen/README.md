# COMP 1080SEF GROUP PROJECT
## default testing data
these data are preset as the testing data

default user accounts (username, password)
- s1410346, 12345
- s1427615, 12345678
- s1388048, vip888

attendance text file (e.g. s1388048_attend.txt)<br>
65	← total classes in a term<br>
0:0	← classes had : classes attended<br>
0	← total tokens used<br>
0	← number of $5 coupons<br>
0	← number of $10 coupons

class schedule text file (e.g. s1388048_schedule.txt)<br>
<pre>
'''
11~28~09:00-10:50~COMP1080SEF L01~JCC D0212	← a line in text file<br>
month~day~time~course~venue<br>
'''
</pre>
(lessons recorded only contains October and November)

(The three testing accounts are planned to be created by the school side, and at the same time the attendance and schedule text file are planned to be created when the account is created. Therefore, only these three accounts are available for testing the functions of the system.)<br>
each account has two text file, attend.txt and schedule.txt<br>
for the whole system and testing cases, 7 text files and one python file are needed

## testing the system
In the system, most of the functions are chosen by inputting their according numbers to run the corresponding function. If there is invalid input, the system will get back to the previous page.<br>
Also, the system can't run smoothly if it is run by IOS/MacOS, since the command os.system("cls") (clear screen) can't be found with using IOS/MacOS system.

### login page
there are create account, login and exit

create account: accounts can be created, but can't be used for the main system functions.<br>
login: input both the username and password correctly to get into the main menu<br>
exit: end the system

### attendance taking
it is used for making data for attendance calculations. Not expected to be used as a formal attendance taking function.

press "yes" or "no" to choose whether you have attended a lesson or not.<br>
it will affect the "class had" and class attended" in attend.txt

### attendance calculator
it will show the total attendance of the users, and can exchange coupons through tokens gained through attending classes.

trade system:<br>
tokens haved = classes attended / total classes in a term<br>
(70% attendance = + 10 tokens, 80% attendance = + another 10 tokens)<br>
$5 coupons = 20 tokens<br>
$10 coupons = 35 tokens

### navigation
it is used for users to find out the distance and travel time of their origin and destination

the starting point and the detination have to be input by the user (e.g. hkmu, jcc)<br>
and choose the travel mode (walk, public transport, drive)<br>
then a link to Google Map will be generated. users can click on it and find out the info. they want<br>

### timetable
user's schedule will be read through schedule.txt. the events will be shown on a 2025 calendar.<br>
the text file only contains October and November events of the user.

(the calendar is displayed according to the terminal size. therefore, full screen is recommended. and the events may not be fully shown because of the size of the cells)

users can switch month (Jan-Dec), add events, view events, and back to main menu<br>
add events: users can choose a date, add their own events by typing it themselves (e.g. 9:30-11:30COMP exam) (can't input the symbol "~")<br>
view events: users can choose a date, and view all the events through an ordered list