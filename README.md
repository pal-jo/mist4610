# MIST Group Project - Group 2 71552

# Team Members:
* Ayush Aggarwal, [@ayu086](https://github.com/ayu086/group-project-1)
* Palak Joshi, [@pal-jo](https://github.com/pal-jo/mist4610)
* Soha Nathani, [@SohaNathani16](https://github.com/SohaNathani16/mist-4610)
* Vinay Polaku, [@vinay-polaku](https://github.com/vinay-polaku/mist4610)
* Christine Shen, [@xixi922](https://github.com/xixi922/group2-project?tab=readme-ov-file#group2-project)
  


# Scenario Description

This database model is designed to support core hotel operations and is crucial for tracking hotel-customer interactions. It facilitates the management of guest information, including personal details and contact information. The system also handles hotel and room management, tracking details such as hotel locations, room types, and real-time availability. Reservations are a central component, with the database storing reservation details like check-in dates, total amounts, payment status, and links to relevant hotel, guest, room, and payment information. Payment processing is also supported, with the system recording payment transactions, dates, and methods. Importantly, this structure efficiently organizes and analyzes data, revealing trends and insights into key hotel operations. By providing a foundation for managing key aspects of a hotel's business, from guest interactions and bookings to room management and financial transactions, this model enables hotels to efficiently organize and navigate data, make informed decisions, and ultimately leads to improved efficiency, increased profitability, and a better overall customer experience.

# Data Model
The data model is designed to support the hotel's core operations, including customer management, room reservations, hotel information, staff management and payment processing. To make sure the system can monitor and handle consumer interactions, the Guest entity keeps track of personal data. The hotel entity keeps track of the hotel's name, address, and room count, among other basic details. The hotel is linked to the room entity, which keeps track of details like the kind of room and its availability. Two interconnected tables are used to record reservation data: Reservations, which contains general reservation information including check-in date, total amount, and payment status; and Payments, which contains payment details for individual reservations, such as payment date and method. Finally, the Employee entity associates employees with the hotel, supporting human resource management and operational tracking. The relationships between these entities ensure comprehensive data storage to efficiently manage the day-to-day operations of the hotel.

A key component of the entire paradigm is the Reservation entity, which houses information like the check-in date, total cost, and payment status. A guest and a room are linked to each reservation record, which may also be linked to a payment record.

The Hotel entity forms a one-to-many relationship with Rooms and Staff. A hotel can have multiple rooms and staff, each of which belongs to a specific hotel.

The Room entity forms a one-to-many relationship with Reservation, where a room can be booked multiple times at different times, but each booking record can only correspond to a specific room.

Additionally, the Guest entity and Reservation have a one-to-many relationship in which a guest may make several reservations for various rooms, but only one guest is associated with each reservation record.

Each Reservation has a Payment record that contains details like the date and mode of payment because the Payment entity maintains transaction data and has a one-to-one relationship with the Reservation.

The Hotel and the Staff entity have a one-to-many relationship, meaning that a hotel may have several employees who are all affiliated with the same hotel. This makes it possible for hotels to more effectively manage their workforce and work assignments.
  
<img width="542" alt="image" src="https://github.com/user-attachments/assets/f7312931-8158-439e-9fb7-78a0849394e5" />



# Data Dictionary
<img width="715" alt="image" src="https://github.com/user-attachments/assets/f54a6079-9ec1-43ff-b421-d260a09ffded" />
<img width="721" alt="image" src="https://github.com/user-attachments/assets/a45fc409-7c4a-490a-869a-e04cde3b285a" />
<img width="718" alt="image" src="https://github.com/user-attachments/assets/72f96201-05f8-4049-8881-e026ba077417" />

# Queries

## Simple Queries

Query 1 ~ 
This query retrieves all records from the “room” table where the “room_availability” column is marked as "Available." This means it fetches details of all rooms that are currently unoccupied and can be booked. A hotel manager needs to monitor room availability to optimize occupancy rates. By knowing which rooms are available, they can assign rooms to incoming guests efficiently. It also enables them to plan marketing strategies to promote vacant rooms and coordinate with housekeeping to prepare rooms for future bookings.

<img width="809" alt="image" src="https://github.com/user-attachments/assets/cb9c7c4c-daaa-470f-8d60-89688bebb19b" />

----------------------------------------------------------------------------------------------------
Query 2 ~ 
This query pulls up all reservations linked to a specific guest, showing details like check-in/check-out dates, room type, and payment status. Keeping track of guest reservations helps managers offer better service to returning guests, quickly resolve past booking issues, and make sure VIPs or loyal customers get priority treatment. Plus, it helps spot booking trends so hotels can offer special promotions or discounts to frequent guests.

<img width="894" alt="image" src="https://github.com/user-attachments/assets/59bbb5d3-3bee-4e1d-aafd-c69d67ed7569" /> 

----------------------------------------------------------------------------------------------------

Query 3 ~ 
This query calculates the total outstanding payment amount from all reservations where the payment status is marked as "Pending." Managing pending payments is crucial for financial stability. A manager would use this information to follow up with guests who have unpaid balances. They could also assess financial performance and cash flow, implement strategies like upfront payments or payment reminders to reduce outstanding dues. This also allows theme to identify potential risks of non-payment and take necessary actions.

<img width="800" alt="image" src="https://github.com/user-attachments/assets/6ead87f8-0e7f-4a69-9357-3049b4063083" />

----------------------------------------------------------------------------------------------------

Query 4 ~ 
This query calculates the total number of guests in the hotel's system, including both past and current visitors. Knowing the total guest count helps managers understand customer trends and demographics. It also gives insight into hotel popularity, retention rates, and staffing needs while helping evaluate the effectiveness of marketing and loyalty programs.

<img width="800" alt="image" src="https://github.com/user-attachments/assets/3f194de9-0fc1-4524-98ef-8d9252f18021" />


## Complex Queries

Query 1 ~ 
This query helps managers identify which room types are the most frequently booked. By knowing which room types are in high demand, managers can make informed decisions about pricing, promotions, and even which room types to prioritize for maintenance or upgrades. The results are ordered from the most booked to the least booked, making it easy to see which room types are the most popular.
  
<img width="543" alt="image" src="https://github.com/user-attachments/assets/99050853-11a5-4673-b9b0-c2b4c3c09856" />

----------------------------------------------------------------------------------------------------

Query 2 ~ 
This query provides insights into the total revenue generated for each check-in date. By analyzing this data, managers can identify peak booking periods and understand revenue trends over time. This information is crucial for planning staffing levels, setting room rates, and optimizing marketing strategies to maximize revenue during high-demand periods.
  
<img width="649" alt="image" src="https://github.com/user-attachments/assets/9fc198d8-b62c-4a1e-91d9-d79e490abfe9" />

----------------------------------------------------------------------------------------------------

Query 3 ~ 
This query helps managers identify the top loyal guests by spending. This can allow hotel managers to identify which customer relationships are strong and encourage repeat business, customer satisfaction and overall revenue. It also allows hotels to focus marketing efforts on high-value guests, maximizing profitability.
  
<img width="1266" alt="image" src="https://github.com/user-attachments/assets/c5563e30-fb80-40d2-9331-4a1732929d9c" />
<img width="208" alt="image" src="https://github.com/user-attachments/assets/0b955c45-2e07-4b59-a52c-e72e41171304" />

----------------------------------------------------------------------------------------------------

Query 4 ~ 
This query calculates the occupancy rate, which is the percentage of rooms that are currently occupied. By knowing the occupancy rate, managers can assess how well the hotel is utilizing its available rooms. This information is crucial for making decisions about pricing strategies, marketing efforts, and even potential expansions or renovations to meet demand
  
<img width="754" alt="image" src="https://github.com/user-attachments/assets/b9994d3b-c536-4cc5-8caf-28e365d72abe" />

----------------------------------------------------------------------------------------------------

Query 5 ~ 
This query identifies the busiest month for hotel bookings. Understanding which month has the highest number of bookings helps managers prepare for peak periods by ensuring adequate staffing, inventory, and services. It also aids in planning promotional activities and optimizing room rates to maximize revenue during high-demand times.
  
<img width="610" alt="image" src="https://github.com/user-attachments/assets/799c6740-91f8-4f01-808f-8a4687e05c30" />

----------------------------------------------------------------------------------------------------

Query 6 ~ 
This query lists the hotel name along with the highest paid staff member. By identifying the highest paid employee, managers can review compensation structures and ensure that salaries are competitive and aligned with the employee's role and performance. This information can also be useful for budgeting and financial planning within the hotel.
  
<img width="678" alt="image" src="https://github.com/user-attachments/assets/1e6bae3b-28d1-4d4a-908d-467f37e233e7" />


# Database Information

<img width="830" alt="image" src="https://github.com/user-attachments/assets/1011ffa4-ad4c-4a4b-b22e-8325b0cf2d34" />

