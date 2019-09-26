# SCHEMA

## Tables
- user: contains information on users
  - id: a unique identifier for a user (pk)
  
- offer: contains information on offers
  - id: a unique identifier for a user (pk)
  - user_id: a reference to the user that received this offer (fk to user)
  - company_id: a reference to the company that extended this offer (fk to company)
  - academic_year_id: a reference to the academic year of the student (fk to academic_year)
  - location_id: a reference to the state that the offer is for (fk to location)
  - notes: a text string of any notes added by the student
  
- compensation: contains information on compensation
  - id: a unique identifier for a compensation (pk)
  - offer_id: the offer that this compensation applies to (fk to offer)
  - type_id: the type of compensation (fk to compensation_type)
  - amount: the amount of this compensation
  - repeat_rate: the repeat rate of the compensation
  
- compensation_type: an enum of different types of compensation
  - id: a unique identifier for a compensation_type (pk)
  - name: the name of the compensation_type

- location: contains information on locations
  - id: a unique identifier for a location (pk)
  - state: the state name in the US
  - city: the city name

- company: contains information on companies
  - id: a unique identifier for a company (pk)
  - name: the name of a company
  
- academic_year: an enum the academic year (freshman, sophomore, etc...)
  - id: a unique identifier for an academic year (pk)
  - name: the name of an academic year
  
 ## Legend
 - pk = primary key
 - fk = foreign key
