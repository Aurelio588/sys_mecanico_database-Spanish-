# sys_mecanico_database-Spanish-
#  Mechanics Workshop Management System (`svs_mecanicos`)

This repository contains the data modeling and the MySQL SQL script for managing a mechanic workshop, covering the control of clients, vehicles, mechanics, repairs, spare parts, and service details.

---

##  Database Structure

The system consists of the following main tables:

*   **`cliente`**: Stores personal and contact information for clients. Includes a unique key (`UNIQUE`) for the email address.
*   **`vehiculo`**: Registers automobile details (brand, model, year, license plate, color) linked to a client via a foreign key with cascade on delete and update (`ON DELETE CASCADE ON UPDATE CASCADE`).
*   **`mecanico`**: Contains information about the technical staff and their specialization.
*   **`reparacion`**: Manages service orders, linking vehicles and responsible mechanics, along with dates, diagnostics, status, and labor cost.
*   **`detalle_reparacion`**: Allows detailing additional descriptions and costs associated with each repair.
*   **`repuestos`**: Catalog of parts and inventory available in the workshop (code, price, stock).
*   **`repuesto_reparacion`**: Intermediate table that resolves the many-to-many relationship between repairs and spare parts, recording the quantity used and unit price.

---

##  Technologies Used

*   **MySQL** (Relational database management system).
*   **SQL** (DDL for table creation, `CONSTRAINT` definitions, and foreign keys).
*   **Draw.io / Mermaid** (For Entity-Relationship modeling).

---

##  How to Run the Script

1. Clone this repository or copy the SQL code.
2. Open your preferred database manager (such as **MySQL Workbench**, **DBeaver**, or MySQL console).
3. Run the complete script to create the `svs_mecanicos` database and all its tables with their respective referential integrity constraints.
