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
* [cite_start]**Drivers / Vehicle Owners:** The primary end-users who use the system to find parking, make reservations, and pay fees[cite: 253, 267, 273]. [cite_start]They can be "Walk-in" users or "Registered" users with reservations[cite: 256].
* [cite_start]**Parking Administrators:** Staff who use the dashboard to monitor occupancy, manage pricing models, and view financial reports[cite: 268, 270, 271].
* [cite_start]**Security Staff:** Personnel who are automatically notified by the system in cases of unauthorized entry, unresolved violations, or payment refusals at the exit[cite: 263, 266, 283].

#### 2. Secondary Stakeholders (Business & Technical)
* [cite_start]**Payment System:** An external system actor responsible for processing transaction requests and verifying payment status during reservations and exit procedures[cite: 253, 300, 301].
* **Facility Management:** The owners interested in revenue maximization and space optimization.
* **System Maintenance Team:** Responsible for IoT sensors and barrier hardware.

### Main Requirements

#### Functional Requirements
1.  [cite_start]**Real-Time Monitoring & Availability Check:** The system must check parking availability instantly for both reservation requests and walk-in vehicles, displaying a "Parking Full" message if no spots are available[cite: 256, 257, 285].
2.  **Reservation Management:** Users can search for spots, enter details (date/duration), and pay in advance. [cite_start]The system must support **modification** and **cancellation** of these reservations, including refund/penalty calculations and updating the reservation register[cite: 274, 278, 279].
3.  **Automated Entry Control:**
    * [cite_start]**Identification:** Identify the vehicle via ANPR[cite: 254].
    * [cite_start]**Authorization:** Verify if the vehicle has a valid reservation or if a walk-in spot is available[cite: 255, 256].
    * **Violation Check:** The system must check for existing violations. [cite_start]If a violation exists, it prompts for resolution; if unresolved, entry is denied and security is called[cite: 261, 263].
4.  **Automated Exit Control:**
    * [cite_start]**Fee Calculation:** Calculate the parking duration and fee upon exit[cite: 280, 281].
    * **Payment Verification:** Verify if payment is completed. [cite_start]If not, request payment; if denied, call security[cite: 282, 283].
5.  [cite_start]**Dynamic Pricing Management:** Administrators must be able to modify pricing rules and apply new pricing models based on operational data[cite: 271].
6.  [cite_start]**Admin Dashboard:** A secured interface for administrators to monitor occupancy, view financial reports, and manage user accounts[cite: 269, 270, 298].

#### Non-Functional Requirements
1.  **Performance:** The system must update parking spot availability on the user app within 5 seconds of a sensor state change.
2.  **Reliability:** The system must maintain 99.9% uptime, with a failover mechanism for barrier gates (e.g., manual override).
3.  **Security:** All payment transactions and user credentials must be encrypted. [cite_start]Access to the Admin Dashboard must be secured via authentication[cite: 268, 296].
4.  **Scalability:** The architecture must support the addition of new sensors and parking zones without significant downtime.
5.  **Usability:** The mobile interface should be intuitive, allowing users to complete a reservation in under 3 clicks.

### Assumptions

1.  **Hardware Availability:** The facility is equipped with functioning IoT ultrasonic sensors, ANPR cameras for vehicle identification, and automated barrier gates.
2.  **Network Connectivity:** A stable high-speed internet connection exists to link local sensors with the central database.
3.  **User Technology:** Users possess smartphones with internet access for the app.
4.  [cite_start]**Payment Integration:** A third-party Payment System is available to verify status and process transactions in real-time[cite: 301].
5.  [cite_start]**Violation Data:** The system has access to a database or logical rule set to define and identify "vehicle violations" (e.g., previous unpaid fees)[cite: 261].
6.  **Regulatory Compliance:** Data storage complies with local privacy laws regarding license plate data.
