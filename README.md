# medical_record
#### Video Demo:
## Description:

### an overview of the things this app does:
##### medical record is a gui app that can save the medical records of any number of users and displays it to them if they want, edits the saved data and deletes them if needed.
##### the records may contain a name (must be unique), an age, any number of conditions for each name and any number of medication for each condition.
##### records can be seen via text and can be heard via a text to voice engine.
##### any part of a record (name, age, condition, medication) can be edited in the page designed for data editing.
##### and user has three deleting options: full file deleting, condition deleting and medicine deleting.


### adding data:
##### there is two pages that are designed for adding new data; 
##### first page for adding a file, in which the user inputs name, age, and any number of conditions they want (separated with a comma and a space).
##### to lower the complexity of design, creating a file and adding new condition to existing files is done in the same page;
##### although the entry for age gets deactivated if user wants to update an existing file.
##### second page for saving medication, in which the user chooses a name and a condition and adds any number of medicine related to the specified condition.


### display data:
##### there is two pages that are designed to display the saved records to user.
##### first a condition page in which user will choose a name and open the file.
##### the name, age and all the conditions saved under that name will be shown.
##### second a medicine page in which the user will choose a name and a condition and open the text. 
##### the name, age, chosen condition and all the medication saved under that condition will be displayed.
#### there is a button that activates text to voice and all the data will be read by a robotic voice.


### edit data:
##### in the Edit page, user will choose a name and then select a page for the kind of data that needs editing; there is four pages in total.
##### first page is for editing the name, it simply displays the name chosen, and asks user to input the new name.
##### second page is for editing age, it displays the name and the age that is already saved, and requests an input to update age.
##### third page is for editing conditions, it asks the user to select which one of the conditions registered under that name he wants to update, then asks for an updated sentence.
##### the fourth page is for editing medications, it requires the user to select one of the conditions saved under chosen name, and then to choose a medicine registered under that condition, then input a fixed version of that medicine.


### delete data:
##### in the delete page, user first chooses what kind of deletion he wants to perform, there are three types of deleting: full file deleting, condition deleting, medicine deleting.
##### if the user chooses to delete a whole file, he just has to select a name and all the data saved under that name will be deleted.
##### if the user wants to make a condition disappear, he picks a name and a condition that is filed under that name and sends that condition and all the medicines registered under it to the void.
##### if the user chooses medicine delete, he inputs a name and a condition saved under that name and a medicine saved under that condition, then deletes that one data.
#### any attempt to delete a data is followed by a conformation message before finalization.


## exploring the code
##### medical record project contains four .py , one requirements.txt and one icon.ico files

### .py files:

#### project.py
##### project.py is the backbone of medical record.
##### it contains all the code that runs the sql database, from making the database to deleting files, everything is done in this file.
##### the main function of project.py creates the database;
##### it runs as soon as the gui starts running.
##### other functions run when the corresponding buttons are clicked or options have been chosen.


#### test_project.py
##### test_project.py is the unittest of this project.
##### it is designed to check if all the sql queries work properly and only take suitable data.
##### this unit test only works if the database is empty, due to some test adding, removing and calling data.
##### for the sake of this test, some code has been added to the project.py file, which weren't necessary due to gui design stopping a lot of wrong data being inputted.


#### User_interface.py
##### acting as the face of the project, User_interface.py is a tkinter based oop code that gives the user an easy interface to work with.
##### due to the nature of this app, using a gui seemed inevitable.
##### but due to the nature of me not being a graphic designer, I have made a simple but easy to use interface so any user can benefit from this kind of app.
##### User_interface.py also contains some code that stop the user from inputting wrong or empty data.
##### as well as containing the code used for the text to voice engine.
##### it might be worth knowing that the gui was first wrote using functions, because I like functions more and have a better understanding of them. but due to suggestions I changed the code to oop, plus added more stuff to it.


#### main.py
##### main.py is simply an "execute the project" file, it imports the graphical_interface.py file and runs it, this action could also be performed by running graphical_interface.py.
##### but I didn't like the idea of running the app through the gui file.


### .ico file
##### icon.ico (yup, I gave it that name) it's just an icon being used inside graphical_interface.py.


## future work

##### 1. ability to add pictures for conditions and medications (such as MRI pictures and...).
##### 2. the text widget that displays the files should change size dynamically based on how big a file is.
##### 3. better graphical interface.
##### 4. window size change based on users desktop (now the size gets messed up when using a different computer).






