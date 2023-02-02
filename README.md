# Calendar
#This is a simple Calendar module 

import calendar

def print_calendar(year, month):
  # Create a calendar object for the given year and month
  cal = calendar.monthcalendar(year, month)

  # Print the header row of the calendar
  print("Mo Tu We Th Fr Sa Su")

  # Print each week of the month
  for week in cal:
    line = ""
    for day in week:
      if day == 0:
        line += "   "
      else:
        line += "{:2} ".format(day)
    print(line)

a=int(input("Enter the year you want to see: "))
b=int(input("Enter the Month you want to see:"))
print_calendar(a, b)
