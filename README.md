# Property Rental Agency (PRA) Database Project

## Project Description
The Property Rental Agency (PRA) facilitates mediating between property Owners and Tenants across multiple cities in India. The system has different types of users, including Owners, Tenants, Managers, and a single superuser who is the Database Administrator (DBA). Users have login credentials and may have both owner and tenant roles. The system allows users to register properties they want to give for rent and capture details of properties rented to tenants.

## Entities
1. User: Represents both Owners and Tenants with adharID, name, age, address, and multiple phone numbers.
2. Property: Can be residential (independent-house/flat) or commercial (shop or warehouse) with a unique ID. Each property has an owner and various property details.
3. PropertyRent: Contains details of properties rented to tenants, such as rent per month, start_date, end_date, yearly hike in rent, agency commission, etc.

## Functionality
1. **Adding Users:** The DBA adds users to the database with necessary privileges. Managers can also add users with limited permissions.
2. **Property Management:** DBA and Managers can add, delete, and update any property record. Owners can only manage their own property records.
3. **Property Rent Details:** Admin and Managers can add property rent details after a property is rented to a tenant.
4. **Rent History Report:** Generate a report on the rent history of a specific property.
5. **Property Search:** Allow users to search for available properties for rent within a given city/locality/price range.
6. **Property Status Check:** Users can check the status of a property using its ID.
7. **Tenant Privileges:** Tenants can only view available properties for rent and cannot modify any data in the database.

## Entities Attributes
- User: adharID (PK), name, age, address, phone numbers, login credentials
- Property: propertyID (PK), owner (FK to User.adharID), available from date, available till date, rent per month, annual hike in rent, total area, plinth area, number of bedrooms (for residential), number of floors, year of construction, locality, address, facilities, property type
- PropertyRent: rentID (PK), propertyID (FK to Property.propertyID), tenant (FK to User.adharID), rent per month, start_date, end_date, yearly hike in rent, agency commission, other info

## Project Scope
The project involves ER/EER Modeling, relational schema design, and refinement (Normalization). It includes creating database tables with constraints and inserting initial data. SQL/PL-SQL code will be written for data entry, updates, generating reports, and enforcing complex constraints or rules. The database will be used to manage property rentals, users, and rental history across multiple cities in India.
