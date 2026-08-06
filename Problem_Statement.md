Problem Statement

1. Title

Smart Parking & Slot Booking Platform

---

2. Domain

Smart Mobility / Urban Transportation / Parking Management

---

3. Who is the user?

Driver / Vehicle Owner

- Search for available parking slots
- Book and cancel parking reservations
- View booking history and parking usage

Parking Attendant

- Verify vehicle entry and exit
- Update parking session status
- Monitor occupied and available slots

Admin

- Manage parking lots and parking slots
- Configure pricing and booking rules
- View occupancy reports and usage analytics

---

4. What problem are we solving? 

Finding a parking space in crowded areas such as shopping malls, hospitals, colleges, and office complexes is often difficult and time-consuming. Drivers usually enter parking areas without knowing whether any slots are available, which leads to unnecessary traffic congestion, fuel wastage, and frustration. Parking operators also face challenges in managing occupancy efficiently and preventing multiple users from reserving the same slot simultaneously. The proposed system provides a centralized digital platform that enables users to check real-time parking availability, reserve slots in advance, and track parking usage securely and efficiently.

---

5. Proposed Solution

The Smart Parking & Slot Booking Platform will provide the following features:

- User registration and secure login using JWT authentication
- Real-time display of parking lot and slot availability
- Smart slot allocation for booking requests
- Parking slot booking for a selected date and time range
- Booking cancellation and automatic slot release
- Vehicle check-in and check-out management
- Occupancy and usage analytics dashboard for administrators
- Email notifications for booking confirmation and cancellation
- Responsive web interface accessible from desktop and mobile browsers

---

6. Core Entities / Database Tables

1. users – stores driver, attendant, and admin details
2. parking_lots – stores parking location information
3. parking_slots – stores individual slot details and availability status
4. bookings – stores reservation information
5. parking_sessions – stores actual vehicle entry and exit records
6. payments – stores payment or transaction details
7. audit_logs – stores important system activity logs

---

7. User Roles & Permissions

Role| Permissions
Admin| Manage users, parking lots, slots, pricing, reports, and analytics
Driver| Register, login, search availability, book slots, cancel bookings, and view booking history
Parking Attendant| Verify bookings, check vehicles in/out, and update slot occupancy

---

8. Success Criteria

- A driver should be able to find and book an available parking slot in under one minute.
- The system should prevent double-booking of the same slot during concurrent booking requests.
- Slot availability should update immediately after booking or cancellation.
- Administrators should be able to view accurate occupancy statistics and booking reports.
- The application should function correctly on both desktop and mobile devices.

---

9. Out of Scope

- Native Android or iOS mobile applications
- Integration with physical parking barriers or IoT sensors
- Real-time GPS vehicle tracking
- Online payment gateway with actual financial transactions
- AI-based vehicle number plate recognition (can be considered as a future enhancement feature)

---

10. Chosen Track

Java (Spring Boot)

- Frontend: React.js + Tailwind CSS + Axios
- Backend: Spring Boot 3.x + Spring Security + JWT
- Database: PostgreSQL 15
- API Documentation: Swagger / OpenAPI
- Deployment: Render (Backend), Vercel (Frontend), Railway PostgreSQL (Database)