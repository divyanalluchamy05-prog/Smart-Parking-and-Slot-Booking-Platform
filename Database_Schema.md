# Database Schema

## users

| Column | Type |
|---|---|
| user_id | INT |
| name | VARCHAR |
| email | VARCHAR |
| password | VARCHAR |
| role | VARCHAR |

## parking_lots

| Column | Type |
|---|---|
| lot_id | INT |
| lot_name | VARCHAR |
| location | VARCHAR |
| total_slots | INT |

## parking_slots

| Column | Type |
|---|---|
| slot_id | INT |
| slot_number | VARCHAR |
| status | VARCHAR |
| lot_id | INT |

## bookings

| Column | Type |
|---|---|
| booking_id | INT |
| booking_time | TIMESTAMP |
| start_time | TIMESTAMP |
| end_time | TIMESTAMP |
| user_id | INT |
| slot_id | INT |

## parking_sessions

| Column | Type |
|---|---|
| session_id | INT |
| check_in | TIMESTAMP |
| check_out | TIMESTAMP |
| booking_id | INT |

## payments

| Column | Type |
|---|---|
| payment_id | INT |
| amount | DECIMAL |
| payment_status | VARCHAR |
| booking_id | INT |

## Relationships

- One *User* can have many *Bookings*
- One *Parking Lot* can contain many *Parking Slots*
- One *Parking Slot* can have many *Bookings*
- One *Booking* generates one *Parking Session*
- One *Booking* can have one *Payment*