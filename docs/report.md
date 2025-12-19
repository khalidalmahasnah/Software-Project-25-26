# Parking Management and Guidance System

## 1. System Description

### Problem Statement

In high-density environments such as universities, shopping malls, and city centers, finding a parking space quickly is inefficient. Drivers waste significant time and fuel circling lots searching for open spots, contributing to traffic congestion and carbon emissions.

Currently, most parking facilities rely on manual management or outdated legacy systems. These suffer from critical issues:
1.  **Lack of Visibility:** Drivers do not know if a spot is available before arriving.
2.  **Inefficient Entry/Exit:** Manual ticketing creates bottlenecks.
3.  **Poor Management Data:** Administrators lack real-time insights into occupancy and revenue.
4.  **Security Gaps:** Manual checks often miss vehicle violations or unauthorized access attempts.

There is an urgent need for an integrated **Parking Management and Guidance System** that leverages IoT sensors, ANPR (Automatic Number Plate Recognition), and mobile technology to automate access, enforce security protocols, and guide users in real-time.

### Stakeholders

#### 1. Primary Actors (Direct Users)
* **Drivers / Vehicle Owners:** The primary end-users who interact with the system to register, find parking, make reservations, and pay fees. They can be "Walk-in" users or "Registered" users.
* **Parking Administrators:** Staff who use the web dashboard to monitor occupancy, manage pricing models, and view financial reports.
* **Security Staff:** Personnel who are automatically notified by the system in cases of unauthorized entry, unresolved violations, or payment refusals at the exit.

#### 2. Secondary Stakeholders (Business & Technical)
* **Payment System:** An external system actor responsible for processing transaction requests and verifying payment status during reservations and exit procedures.
* **Facility Management:** The owners interested in revenue maximization and space optimization.
* **System Maintenance Team:** Responsible for IoT sensors and barrier hardware.

### Main Requirements

#### Functional Requirements
1.  **User Account Management:** The system must allow drivers to **register and login** to personal accounts. Registered users must be able to manage their profile and **view reservation history**.
2.  **Real-Time Monitoring & Availability Check:** The system must check parking availability instantly for both reservation requests and walk-in vehicles, displaying a "Parking Full" message if no spots are available.
3.  **Reservation Management:** Users can search for availability, **select a specific parking spot**, and pay in advance. The system must support **modification** and **cancellation** of reservations, including refund/penalty calculations.
4.  **Automated Entry Control:**
    * **Identification:** Identify the vehicle via ANPR.
    * **Authorization:** Verify if the vehicle has a valid reservation or if a walk-in spot is available.
    * **Violation Check:** The system must check for existing violations (e.g., unpaid fines). If a violation exists, it prompts for resolution; if unresolved, entry is denied and security is called.
5.  **Automated Exit Control:**
    * **Fee Calculation:** Calculate the parking duration and fee upon exit.
    * **Payment Verification:** Verify if payment is completed. If not, request payment; if denied/failed, the barrier remains closed and security is notified.
6.  **Dynamic Pricing Management:** Administrators must be able to modify pricing rules and apply new pricing models based on operational data.
7.  **Admin Dashboard:** A secured interface for administrators to monitor occupancy, view financial reports, and manage user accounts.

#### Non-Functional Requirements
1.  **Performance:** The system must update parking spot availability on the user app within 5 seconds of a sensor state change.
2.  **Reliability:** The system must maintain 99.9% uptime, with a failover mechanism for barrier gates (e.g., manual override).
3.  **Security:** All payment transactions and user credentials must be encrypted. Access to the Admin Dashboard must be secured via authentication.
4.  **Scalability:** The architecture must support the addition of new sensors and parking zones without significant downtime.
5.  **Usability:** The mobile interface should be intuitive, allowing users to complete a reservation in under 3 clicks.

### Assumptions

1.  **Hardware Availability:** The facility is equipped with functioning IoT ultrasonic sensors, ANPR cameras for vehicle identification, and automated barrier gates.
2.  **Network Connectivity:** A stable high-speed internet connection exists to link local sensors with the central database.
3.  **User Technology:** Users possess smartphones with internet access for the app.
4.  **Payment Integration:** A third-party Payment System is available to verify status and process transactions in real-time.
5.  **Violation Data:** The system has access to a database or logical rule set to define and identify "vehicle violations" (e.g., previous unpaid fees).
6.  **Regulatory Compliance:** Data storage complies with local privacy laws regarding license plate data.
