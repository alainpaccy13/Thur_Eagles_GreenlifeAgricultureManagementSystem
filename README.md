

# GreenLife Urban Agriculture Management System
## Project Overview
**The GreenLife Urban Agriculture Management System** enables GreenLife to efficiently track farm locations, crop details, volunteer and employee data, harvest records, and resource inventory. 
The database supports decision-making and operations, ensuring each farm has the necessary resources and workforce to maintain crop health and distribute produce effectivelly.

**Entities and Attributes**
## 1. Farm Locations
### Purpose: Stores details about each farm location.
**Attributes:**
- Location_ID (Primary Key): Unique ID for each farm location.
- Address: Address of the farm.
- Type: Type of space (e.g., rooftop, garden).
- Size: Farm size in square meters.
- Sunlight_Availability: Hours of sunlight per day.
- Water_Source: Availability of water.

## 2. Crops
### Purpose: Contains details of crops grown at each farm.
**Attributes:**
- Crop_ID (Primary Key): Unique ID for each crop.
- Farm_ID (Foreign Key): Links to the associated farm location.
- Crop_Type: Type of crop (e.g., tomatoes, lettuce).
- Planting_Date: Date the crop was planted.
- Expected_Harvest_Date: Expected date for harvest.
- Care_Requirements: Specific care needs for each crop.

## 3. Workforce
### Purpose: Stores information on workers, both volunteers and employees.
**Attributes:**
- Worker_ID (Primary Key): Unique ID for each worker.
- Name: Worker’s name.
- Role: Position or role (e.g., volunteer, employee).
- Tasks_Assigned: Tasks the worker is assigned to.
- Hours_Worked: Total hours worked.
- Special_Skills: Relevant skills (e.g., planting, maintenance).

## 4. Harvest Records
### Purpose: Tracks harvest details, including amounts and distribution.
**Attributes:**
- Harvest_ID (Primary Key): Unique ID for each harvest record.
- Crop_ID (Foreign Key): Links to the crop being harvested.
- Farm_ID (Foreign Key): Links to the farm location of the crop.
- Harvest_Date: Date of harvest.
- Quantity: Amount of produce harvested.

## 5. Inventory and Resources
### Purpose: Manages supplies needed for farming.
**Attributes:**
- Item_ID (Primary Key): Unique ID for each item.
- Item_Name: Name of the inventory item.
- Quantity: Current stock level.
- Cost: Cost per unit of the item.
- Supplier_Info: Information about the item supplier.

## Relationships Between Entities

- A Farm Location can grow multiple Crops.
- Each Crop is associated with a single Farm Location.
- Workers can be assigned to multiple farms and various tasks.
- Each Harvest Record links to a specific Crop and Farm Location.
- Inventory supports multiple farms by supplying necessary resources.

## Keys and Constraints

- Primary Keys: Unique identifiers for each entity, such as Location_ID in Farm Locations and Crop_ID in Crops.
- Foreign Keys: Establish relationships between tables (e.g., Farm_ID in Crops links to Location_ID in Farm Locations).
- Constraints:
  - NOT NULL: Ensures essential fields are always filled.
  - UNIQUE: Ensures fields like Worker_ID have unique values.

## ER Diagram
The ER diagram visually represents the relationships between entities and highlights the primary and foreign keys used to maintain database integrity.

![Screenshot 2024-11-14 at 16 14 12](https://github.com/user-attachments/assets/09014c21-3b20-460a-9f96-1b5778623a15)
