# DELIVERABLE_PRUEBA_DESEMPE-O_2026


This project is part of EventFlow’s data modernization initiative.
The goal is to transform an Excel-based flat data structure into a properly designed relational database that enables efficient storage, consistency and analytical queries.

Previously, all information was stored in spreadsheets where information was mixed into the same records.
This caused several problems:

Data duplication
Inconsistent ticket prices
Difficult reporting and analysis
Lack of data integrity

To solve these problems, a relational database schema was designed in MySQL following the principles of normalization.

Database design
Design approach

The flat dataset contains the following columns:


TransactionID
TransactionDate
AttendeeName
AttendeeEmail
AttendeeCity
EventName
EventCategory
EventDate
VenueName
VenueCity
TicketType
TicketPrice
Quantity
OrganizerName
OrganizerEmail


Since this structure mixes information from multiple real-world entities, the first step was to identify the central entities in the system.

The main entities identified were:

Attendees
Organizers
Events
Places
Ticket types
Transactions
Transaction details

The scheme was designed following the Third Normal (3NF) to eliminate redundancy and ensure data integrity.

Entity relationship model

The database structure separates data into multiple related tables.
Main relationships:

An event can have multiple ticket types
A participant can make multiple transactions
A transaction can contain multiple ticket purchases

Conceptual structure:

Attendees
Transactions
TransactionDetails
TicketTypes
Events
Organizers
Places

This structure avoids duplication and ensures that each entity is stored only once.
