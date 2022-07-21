CREATE database AddressBook_Service;
use AddressBook_Service;
CREATE table AddressBook (
FirstName     varchar(45) Not Null,
LastName      varchar(45) Not Null,
Address       varchar(45) ,
City          varchar(45) ,
State         varchar(45) ,
ZipCode       varchar(45) ,
PhoneNumber   varchar(45) ,
EmailId       varchar(45) ,
Primary key(PhoneNumber) );
Select * From AddressBook;
Insert into AddressBook (FirstName, LastName, Address, City, State, ZipCode, PhoneNumber, EmailId) 
values     ('Nikita','Singh','Andheri', 'Mumbai','Maharastra ' ,'673455','78965345734','nikita43@orkut.com'),
	   ('Rajesh','Sharma','BTM Layout','Bangalore','Karnataka','568882','973660014','rajesh@gmail.com'),
	   ('Anjali','Negi','Kotdwar','Dehradun','Uttarakhand','200342','9256178014','anjaliNegi@gmail.com'),
	   ('Sandeep','Rawat','Kormangala','Bangalore','Karnataka','500812','9655534014','Sandeep.rawat@gmail.com'),
	   ('Shikha','Chauhan','Navi Village','Lucknow','Uttar Pradesh','317702','7913260014','shikha@gmail.com');
Update AddressBook set PhoneNumber = '9246143520' where FirstName = 'Shikha';
Update AddressBook set Address = 'UBCity' where LastName = 'Rawat';
Delete From AddressBook where FirstName='Sandeep';
Select * From AddressBook;
Insert into AddressBook (FirstName, LastName, Address, City, State, ZipCode, PhoneNumber, EmailId) 
values      ('Rashmi','Das','Hinjewadi', 'Pune','Maharastra ' ,'600155','9219345734','rashmi@orkut.com'),
            ('Shivam','Chopra','Kormangala','Bangalore','Karnataka','500122','8654190014','shivam99@gmail.com');
Select FirstName From AddressBook where City = 'Bangalore' or State = 'Uttarakhand';
Select Count(City) From AddressBook;
Select Count(State) From AddressBook;
Insert into AddressBook (FirstName, LastName, Address, City, State, ZipCode, PhoneNumber, EmailId) 
values      ('Vidita','Kumari','Whitefield', 'Bangalore','Karnataka' ,'459755','6700345734','viditaK@outlook.com'),
	    ('Ankit','Rawat','Indiranagar','Bangalore','Karnataka','6130122','9843490014','ankit04@gmail.com');
Select FirstName From AddressBook where City = 'Bangalore' order by FirstName;
Select FirstName From AddressBook where City = 'Bangalore' order by FirstName ASC;
Select FirstName From AddressBook where City = 'Bangalore' order by FirstName DESC;
Alter table AddressBook add AddressBookName varchar(45) Not Null after EmailId;
Alter table AddressBook add AddressBookType varchar(45) Not Null after AddressBookName; 
Update AddressBook set AddressBookName= 'AddressBook1' where FirstName  = 'Rajesh' or FirstName  = 'Vidita';
Update AddressBook set AddressBookName ='AddressBook2' where FirstName  = 'Ankit' or FirstName  = 'Anjali' or FirstName  = 'Nikita' or FirstName  = 'Shivam';
Update AddressBook set AddressBookName = 'AddressBook3' where FirstName  = 'Rashmi' or FirstName  = 'Shikha';
Update AddressBook set AddressBookType = 'Family' where FirstName  = 'Rajesh'  or FirstName  = 'Vidita';
Update AddressBook set AddressBookType = 'Friends' where FirstName  = 'Ankit' or FirstName  = 'Anjali' or FirstName  = 'Nikita' or FirstName  = 'Shivam';
Update AddressBook set AddressBookType = 'Profession' where FirstName  = 'Rashmi' or FirstName  = 'Shikha'; 