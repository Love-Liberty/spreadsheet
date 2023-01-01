# spreadsheet
A possible future of the spreadsheet

Everyone has access to a spreadsheet. Google sheets or Microsoft Excel are both available as are others.

The spreadsheet is ideal for accountants who want to list incomes and expenses month by month. The months are put as the headings of columns and the expenses are put as headings of rows. Then you type in the amount of each expense in each month. The totals show per month in the bottom row and per expenses in the final colum.

The spreadsheet is optimised for that accountancy task and can be used for other tasks which are very similar.

The analogy in programming is a two dimensional array or 2 dimensional table.

But lots of tasks don't fit neatly into rows and columns. Data often doesn't fit neatly into a 2 dimensional array.

If you want to create a table of cities with population, density, car ownership and traffic accidents, this isn't a simple rows and columns task.

In programming it is likely we would use structured data, something like this:

cities {

name: 

pop: 

density: 

cars:  

accidents: 

}

What I envisage is that the future spreedsheet (let's call is a 'datasheet') has the same ability to handle structured data. (The current spreadsheet would become a subset, an option, within the datasheet.)

Opening a datasheet would allow the user to opt for the traditional spreedsheet format or for the structured data format. There would be some ability to auto-swap the manipulation of data between the two formats.

-----------------------------------

**Using structured data format**

First you define the fields you want to input and manipulate. This would be a name for the structure ("Cities") then the labels of the values ("name", "pop" etc)

Data could be output as jason files or csv etc.

Manually inputting data would be filling in forms that show:

 City 434 // autogenerated internal unique identifier

City.name = ________________ (text)

City.pop = ________________ (integer)

City.density _______________ (index)

City.cars _______________ (integer)

City.accidents __________  (integer)

(The detail of data types could include specialist indexes or rates per something)

If uploading a csv file end-of-line would probably means end of the specific structure. Commas would separate the individual values.

-----------------------------

**Manipulating data**

Current spreadhsheets use code such as "=M15 + J34" to say take the value in the cell where column M intersects row 15, add the value in the cell where column J interescts row 34 and place the sum in the current cell (where this code is being typed)

In the data sheet this would become

"=city432.cars + city433.cars" to say take the value in city432.cars, add it to the value in city433.cars and place it in the current position.

So what is the current position if it isn't a cell?

It is a results box.

----------------------------------

**Creating a results box**

When the data struture has been defined, we can also define result boxes.

Click the create a result box option. Give it a name and define what it is the result of.

-------------

Result box name: Number of cities

Result box definition: =sum(Cities)

-------------

Result box name: Number of accidents

Result box definition: sum(Cities.accidents)

--------------

Result box name: Total population

Result box definition: sum(Cities.pop)

-------------

Many of these could be autogenerated as basic options, but ones that are more task specific could include

-------------

Result box name: average city population

Result box definition: Total population/Number of Cities

----------------------


Result box name: Total average accidents per person

Result box definition: Total Accidents/Total population

-----------------

**Manipulation within structures**

Going back to the original structure

 City 434 // autogenerated internal unique identifier

City.name = ________________ (text)

City.pop = ________________ (integer)

City.density _______________ (index)

City.cars _______________ (integer)

City.accidents __________  (integer)

This could include manipulations within the structure (like classes can have methods)

City.accidents/City.pop = City.accidents/City.pop (math auto computed)

City.accidents/City.cars = City.accidents/City.cars (math auto computed)

**Is this possible?**

Yes, it is possible. Has it already been done?
