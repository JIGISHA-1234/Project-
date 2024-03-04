Sure, here's the modified `schema.sql` file with camel case column names:

```sql
CREATE TABLE Trip (
    Trip_Id VARCHAR(255) PRIMARY KEY,
    Creator_User_Id VARCHAR(255),
    Vehicle_Id VARCHAR(255),
    Ride_Date DATE,
    Ride_Time TIME,
    Ride_Status VARCHAR(255),
    No_Of_Seat INT,
    Seats_Filled INT,
    From_Loc VARCHAR(255),
    To_Loc VARCHAR(255)
);

CREATE TABLE Booking (
    Booking_Id VARCHAR(255) PRIMARY KEY,
    Trip_Id VARCHAR(255),
    Number_Of_Seat INT,
    Seeker_Id VARCHAR(255),
    Status VARCHAR(255),
    FOREIGN KEY (Trip_Id) REFERENCES Trip(Trip_Id)
);
```

This `schema.sql` file creates both the "Trip" and "Booking" tables with column names in camel case format. You can place this `schema.sql` file in the `src/main/resources` directory of your Spring Boot application. Let me know if you need further assistance!
