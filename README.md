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

<img width="525" alt="image" src="https://github.com/user-attachments/assets/27910753-239d-4ee3-a820-7b48ac9f1f82" />

----------------------------------------------------------------------------------------------------
Query 2 ~ 
This query pulls up all reservations linked to a specific guest, showing details like check-in/check-out dates, room type, and payment status. Keeping track of guest reservations helps managers offer better service to returning guests, quickly resolve past booking issues, and make sure VIPs or loyal customers get priority treatment. Plus, it helps spot booking trends so hotels can offer special promotions or discounts to frequent guests.

<img width="780" alt="image" src="https://github.com/user-attachments/assets/d3e03c47-9101-4c77-a241-7f7c881e5648" />

----------------------------------------------------------------------------------------------------

Query 3 ~ 
This query calculates the total outstanding payment amount from all reservations where the payment status is marked as "Pending." Managing pending payments is crucial for financial stability. A manager would use this information to follow up with guests who have unpaid balances. They could also assess financial performance and cash flow, implement strategies like upfront payments or payment reminders to reduce outstanding dues. This also allows theme to identify potential risks of non-payment and take necessary actions.

<img width="761" alt="image" src="https://github.com/user-attachments/assets/cb4f77a4-c681-4534-a3cd-dfaf80b5f4cc" />

----------------------------------------------------------------------------------------------------

Query 4 ~ 
This query adds up all the outstanding payments from reservations where the payment status is "Pending." Keeping track of pending payments is super important for financial stability. A manager could use this info to follow up with guests who haven’t paid yet, check on overall financial performance, and improve cash flow. They might also come up with strategies like requiring upfront payments or sending reminders to reduce unpaid balances. Plus, it helps them spot potential risks of non-payment and take action before it becomes a bigger issue.

<img width="668" alt="image" src="https://github.com/user-attachments/assets/b3fb97ba-76cc-4572-8d6f-3f5eeaa3eb87" />


## Complex Queries

Query 1 ~ 
???? insert explanation ????
???? insert images ????

Query 2 ~ 
???? insert explanation ????
???? insert images ????

Query 3 ~ 
???? insert explanation ????
???? insert images ????

Query 4 ~ 
???? insert explanation ????
???? insert images ????

Query 5 ~ 
???? insert explanation ????
???? insert images ????

Query 6 ~ 
???? insert explanation ????
???? insert images ????


# Database Information

<img width="830" alt="image" src="https://github.com/user-attachments/assets/cf2f7366-3ec1-4004-95d2-73d8daaa1f67" />

