---
sidebar_position: 2
---


# Data Types

GOAT handles a wide range of geometry types for spatial data. This capability is achieved by using a [PostgreSQL](https://www.postgresql.org/docs/) database enhanced with the [PostGIS](https://postgis.net/documentation/) extension. GOAT stores all geometries in the **PostGIS geometry type** (PostGIS geometry type is a way to store and work with various shapes and locations on a map within a PostgreSQL database. It allows to keep details about points (such as landmarks), lines (such as roads), and areas (such as districts) directly in your database) within the **EPSG:4326** coordinate reference system. However, for operations involving length or area measurements, the PostGIS geography type is used. This type allows calculations in metres and offers higher accuracy.

Furthermore, GOAT adopts a structured approach to data management by categorizing the data types. This categorization is intended to optimize the database schema for enhanced performance and scalability. The current schema includes a limited number of columns per data type:

| Data Type  | Description | Maximum Number of Columns |
|------------|-------------|--------------|
| integer    | Whole numbers without any decimal points (e.g., 1, 100, -5) |  15 |
| bigint     | Very large whole numbers, larger than what 'integer' can store | 5  |
| float      | Numbers with decimal points that need precision (e.g., 3.14, -0.001) | 10 |
| text       | Any kind of text, including letters, numbers, and symbols | 20 |
| timestamp  | Specific dates and times, including year, month, day, hour, minute, and second | 3  |
| arrfloat (Array of Floats)   | A list of numbers with decimal points, stored together as one entry | 3  |
| arrint (Array of Integers)   | A list of whole numbers, stored together as one entry | 3  |
| arrtext (Array of Text)   | A list of text items, stored together as one entry | 3 |
| jsonb (Binary JSON)    | 	Data formatted as JSON (a way to store information in an organized, easy-to-access manner), stored in an efficient binary format | 3  |
| boolean    | True or false values, used for decisions or to indicate if something is on or off |3 |
