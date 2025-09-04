## Things Accomplished

Designed the database on draw.io
Chose to integrate it using Frappe

Flow of Implementation:

1. Installed frappe, created a site for company
2. Added the tables with the suitable datatypes, and linked successfully. (On the UI)
3. Created server scripts for auto calculate, and customizable scripts for hired on
4. Created roles (Employee, User), added permissions for both.
5. Chosen the name field as the default name for 4 main tables for easy acces when selecting.
6. Tested main tables in postman, and working well, will attach postman file
7. added workflow for Employee Performance Cycle, and added a script that would update status based on certain changes but didnt test well.

## Things Not done

1. Test Employee Performance Cycle workflow
2. didnt run unit/Integration Test
3. Logging

## Attached files to test

1. pip install the requirements.txt to test it easily
2. json file added to main folder, import on postman and you'll find data ready
3. screenshots available in the folder, some snippets from frappe

# Company-Management-System

A Company Management System that is implemented using Frappe.

# Installation

1.  Create a clean venv for frappe

python3 -m venv frappe-bench-env

2.  Activate it

source frappe-bench-env/bin/activate # Mac/Linux

.\frappe-bench-env\Scripts\activate # Windows

3.  Install bench inside this env

## Steps I ran at the beginning

1. Create a New Bench

   bench init company_mgmt_bench
   cd company_mgmt_bench

2. Create a New Site

   bench new-site company.localhost

3. Add to hosts file

   127.0.0.1 company.localhost

4. Get the Frappe Framework Running

   bench start [Running the server]

5. Open In Browser

   http://company.localhost:8000

6. Create Custom App

   bench new-app company_mgmt

7. Install app on site

   bench --site company.localhost install-app company_mgmt

8. Create Doctypes (Database Models)
   bench --site company.localhost execute frappe.new_doc --args "('DocType', {'doctype':'Company'})"

   But easier: use Frappe Developer UI:

   1. Go to Developer > DocType in the UI.
   2. Create new DocType inside Computer Management System Module.

## Steps to run the project

cd company_mgmt_bench

source env/bin/activate

bench start

## Common field types you’ll use the most

    •	Data → simple text (like name, email, phone).
    •	Text → longer text (single block).
    •	Text Editor → long rich text with formatting (like descriptions, notes).
    •	Int → whole numbers (like age, quantity).
    •	Float → decimal numbers (like salary, price).
    •	Currency → number shown with currency formatting (linked to system currency).
    •	Check → yes/no (boolean).
    •	Date → calendar date.
    •	Datetime → date + time.
    •	Time → only time.
    •	Select → dropdown with predefined options.
    •	Link → foreign key (reference another Doctype, e.g., link Employee to Department).
    •	Table → one-to-many relation (e.g., a Project has many Tasks).
    •	Attach → file upload (any type).
    •	Attach Image → image upload only.
    •	Password → masked field.
