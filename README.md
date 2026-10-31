# DBSE_Hackathon

# ChargeShare – Peer-to-Peer EV Charging Network

## 1. Project Overview

ChargeShare is a web-based Peer-to-Peer Electric Vehicle (EV) Charging Platform designed to connect EV owners who need charging facilities with homeowners who have available private EV charging stations.

The system provides a centralized platform where EV owners can search for nearby home charging facilities, check availability, compare charging prices, and reserve charging slots.

Homeowners who have charging facilities can register their charging stations, manage availability, set charging prices, and earn money by sharing their charging facilities with EV owners.

The platform aims to reduce range anxiety, improve accessibility to EV charging facilities, and make better use of existing private charging infrastructure.

## 2. Problem Statement

Electric vehicle owners often face difficulties finding available charging stations during long journeys, especially when the nearest public charging station is far away.

For example, an EV owner travelling with low battery power may find that the nearest public charging station is 80 km away.

At the same time, many homeowners already have EV charging facilities that remain unused for several hours.

Currently, there is no convenient centralized platform connecting EV owners who need charging with nearby homeowners who have available charging facilities.

ChargeShare aims to solve this problem through a location-based peer-to-peer EV charging platform.

## 3. Objectives

* Provide a platform connecting EV owners with homeowners who have charging facilities.
* Help EV owners discover nearby home charging stations.
* Reduce dependency on public charging stations.
* Allow homeowners to share their unused charging facilities.
* Enable homeowners to earn money through charging services.
* Provide real-time or updated charging slot availability.
* Allow EV owners to reserve charging slots.
* Ensure compatibility between vehicles and charging connectors.
* Maintain charging session and booking history.
* Improve accessibility and convenience for EV users.

## 4. Main Features

### EV Owner Module

* EV owner registration and login.
* Manage personal profile.
* Add electric vehicle details.
* Search nearby home charging stations.
* View charging stations on a map.
* Check distance from the current location.
* Filter stations based on price, charging speed and availability.
* Check connector compatibility.
* View homeowner details and ratings.
* Reserve available charging slots.
* View booking confirmation.
* Track booking and charging session history.
* Cancel reservations.

### Homeowner Module

* Homeowner registration and login.
* Manage homeowner profile.
* Register home charging facilities.
* Add charging station location.
* Specify charging connector type.
* Enter charging power capacity (kW).
* Set charging prices.
* Manage available charging time slots.
* Accept or reject booking requests.
* View upcoming reservations.
* Manage charging sessions.
* View earnings and booking history.

### Admin Module

* Admin login.
* Manage EV owner accounts.
* Manage homeowner accounts.
* Verify charging station listings.
* Monitor registered charging stations.
* View all reservations.
* Monitor charging sessions.
* Manage reported issues.
* View platform statistics and reports.

### Location-Based Matching

* Detect the EV owner's current location.
* Identify nearby registered home charging stations.
* Calculate the distance between the EV owner and charging stations.
* Check connector compatibility.
* Check charging station availability.
* Compare charging prices.
* Display suitable charging options based on user requirements.

### Payment and Booking Module

* Select a charging station.
* Choose an available date and time slot.
* Confirm charging reservations.
* Calculate estimated charging costs.
* Maintain payment status.
* Generate booking details and transaction history.

### Future Smart Features

* Intelligent charging station recommendations.
* Route-based charging suggestions.
* Dynamic charging price recommendations.
* Real-time charging availability.
* Smart charging session monitoring.

## 5. Technology Stack

| Component               | Technology                      |
| ----------------------- | ------------------------------- |
| Frontend                | React.js                        |
| Structure               | HTML                            |
| Styling                 | CSS / Bootstrap                 |
| Programming Language    | JavaScript                      |
| Backend                 | Node.js                         |
| Backend Framework       | Express.js                      |
| Database                | MongoDB                         |
| Database Connectivity   | Mongoose                        |
| API Communication       | REST APIs                       |
| Authentication          | JWT                             |
| Location Services       | Google Maps API / OpenStreetMap |
| Payment Integration     | Payment Gateway Sandbox         |
| API Testing             | Postman                         |
| Development Environment | VS Code                         |
| Version Control         | Git and GitHub                  |

React.js is used to develop the frontend interface, while Node.js and Express.js handle backend operations and REST API development.

MongoDB stores user information, vehicle details, charging station information, reservations, charging sessions and payment records.

## 6. System Architecture

The application follows a three-tier architecture.

1. **Presentation Layer** – React.js frontend.
2. **Application Layer** – Node.js and Express.js backend.
3. **Database Layer** – MongoDB database.

### Architecture Flow

EV Owner / Homeowner / Admin

↓

React.js Frontend

↓

Node.js + Express.js REST APIs

↓

Business Logic and Location-Based Matching

↓

MongoDB Database

↓

External Services (Maps API / Payment Gateway / Notifications)

## 7. Database Design

The database is named `chargeshare`.

The planned database consists of the following collections:

| Collection Name    | Description                                            |
| ------------------ | ------------------------------------------------------ |
| users              | Stores EV owner, homeowner and admin information       |
| vehicles           | Stores EV details and connector information            |
| charging_stations  | Stores homeowner charging station details              |
| availability_slots | Stores available charging dates and time slots         |
| reservations       | Stores charging booking information                    |
| charging_sessions  | Stores charging session details and energy consumption |
| payments           | Stores payment and transaction information             |
| reviews            | Stores ratings and feedback from EV owners             |

## 8. Charging Station Specifications

Each registered charging station contains the following information:

* Charging station name.
* Homeowner details.
* Charging station location.
* Latitude and longitude.
* Connector type.
* Charging power capacity (kW).
* Price per unit of electricity (kWh).
* Available charging time slots.
* Operating availability.
* Station description.
* Host verification status.
* User ratings and reviews.

## 9. Booking Status

Every reservation can have one of the following statuses:

* PENDING
* CONFIRMED
* CANCELLED
* COMPLETED
* REJECTED

### Charging Session Status

* NOT_STARTED
* IN_PROGRESS
* COMPLETED

These statuses help EV owners and homeowners track the complete booking and charging process.

## 10. Smart Location-Based Matching

The location-based matching system is one of the main features of ChargeShare.

When an EV owner searches for a charging station, the system identifies suitable nearby homeowners.

The matching process considers:

1. **Location:** Identify charging stations near the EV owner's current location.
2. **Distance:** Calculate the distance between the vehicle and charging station.
3. **Compatibility:** Check whether the charging connector supports the EV.
4. **Availability:** Identify charging stations with available time slots.
5. **Charging Speed:** Compare charging power capacity.
6. **Price:** Display charging costs for comparison.
7. **Ratings:** Consider homeowner ratings and verification.

The system displays suitable charging stations so that EV owners can select and reserve the most convenient option.

## 11. Team Responsibilities

### Member 1 – Frontend Development

* Develop React.js user interface.
* Design landing page.
* Create EV owner dashboard.
* Create homeowner dashboard.
* Design admin dashboard.
* Develop charging station search interface.
* Create booking and reservation pages.
* Integrate frontend with backend APIs.

### Member 2 – Backend Development

* Develop Node.js and Express.js application.
* Create REST APIs.
* Implement user authentication.
* Develop charging station management logic.
* Implement location-based matching logic.
* Handle booking and reservation operations.
* Implement charging session management.
* Connect backend with MongoDB.

### Member 3 – Database, Integration and Testing

* Design and manage MongoDB database.
* Create database collections and relationships.
* Manage vehicle and charging station records.
* Implement booking and payment data management.
* Integrate location services.
* Test backend APIs using Postman.
* Perform frontend and backend integration testing.
* Prepare technical documentation.

## 12. Expected Outcomes

* Improved accessibility to EV charging facilities.
* Reduced range anxiety for EV owners.
* Easy discovery of nearby private charging stations.
* Better utilization of unused home charging facilities.
* Additional income opportunities for homeowners.
* Convenient charging slot reservations.
* Transparent charging prices.
* Improved peer-to-peer connectivity between EV owners and homeowners.
* Support for wider electric vehicle adoption.

## 13. Future Enhancements

* Real-time charging station availability.
* GPS-based route optimization.
* AI-powered charging station recommendations.
* Dynamic charging price calculation.
* Online payment gateway integration.
* Live charging session monitoring.
* IoT-based smart charger integration.
* Mobile application for Android and iOS.
* Notification services through SMS and email.
* Advanced analytics for charging station usage.

## 14. Project Conclusion

ChargeShare aims to create a community-driven EV charging ecosystem by connecting electric vehicle owners with homeowners who have available charging facilities.

By combining location-based discovery, charger compatibility checking, slot reservations and charging management, the platform provides an alternative way to access EV charging facilities.

The system uses React.js, Node.js, Express.js and MongoDB to provide a scalable web-based solution.

ChargeShare helps EV owners find convenient charging options while allowing homeowners to generate additional income from their existing charging infrastructure.

**ChargeShare – Share Your Charger. Power Every Journey.**
