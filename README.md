Project Purpose
The purpose of this project is to implement a collection of calendars that manage one or more appointments. The program allows users to create and modify appointments and calendars, add appointments to a calendar, and read or write appointments to a text file. Additionally, the program automatically checks for scheduling conflicts when adding an appointment to a specific calendar.

Implementation Description
The project consists of six classes:

Appointment Class:
This class allows for the creation of appointments by passing parameters such as date, time, duration, person to meet, and location. To meet the project specification of representing the date in the format dd-mm-yyyy and the time in hh:mm, two formatters are used in the constructor to convert the input strings into valid date and time objects.

Calendar Class (Agenda):
This class allows for the creation of a calendar (agenda) that has a name and a collection of appointments. The class provides a method to add appointments to a calendar, which relies on another method to check for scheduling conflicts with existing appointments. Additionally, the user can modify any field of an existing appointment, and changes to the date or time will trigger a re-check for conflicts. Appointments can also be searched by date or by the name of the person being met. The class implements an iterator to allow iteration over the collection of appointments.

CalendarManager Class (GestoreAgende):
This class manages a collection of calendars. It provides methods to add a new calendar to the collection by specifying its name, as well as methods to write appointments to and read them from a text file, given the file path. The class also includes a method to display appointments in chronological order and a method to delete a calendar by name.

DateComparator Class (ConfrontoDate):
This class implements Comparator<Appuntamento> to compare two appointments and determine which one occurs first chronologically. This is essential for implementing the method that prints appointments in temporal order within the CalendarManager class.

TestAgenda Class:
This class contains tests to verify the correct implementation of the program's methods.

UserInterface Class (InterfacciaUtente):
This class implements the main program, allowing the user to interact with the calendar management system.

