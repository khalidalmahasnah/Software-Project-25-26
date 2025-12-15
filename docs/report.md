# Parking Management and Guidance System

## 1. System Description

### Problem Statement

In high-density environments such as universities, shopping malls, and city centers, finding a parking space fast is really frustrating and inefficient. Drivers waste alot of time and fuel circling lots searching for open spots, which contributes to traffic congestion and increased carbon emissions.

Currently, most parking facilities rely on manual management or outdated legacy systems. These systems suffer from several critical issues:
1.  **Lack of Visibility:** Drivers dont know if a spot is available before arriving.
2.  **Inefficient Entry/Exit:** Manual ticketing and cash payments create bottlenecks at gates.
3.  **Poor Management Data:** Administrators lack real-time insights into occupancy rates, making it difficult to optimize pricing or manage peak hours effectively.

There is an urgent need for an integrated **Parking Management and Guidance System** that leverages IoT sensors and mobile technology to automate access, streamline payments, and guide users to available spots in real-time.
### Stakeholders

#### 1. Primary Actors (Direct Users)
* **Drivers / Vehicle Owners:** The primary end-users who interact with the mobile app and kiosks to find parking, make reservations, and pay fees. Their main interest is convenience and time-saving.
* **Parking Administrators:** Staff members who use the web dashboard to monitor occupancy, set pricing models, and view financial reports.
* **Security Personnel:** Staff who may receive alerts regarding unauthorized parking or barrier malfunctions.

#### 2. Secondary Stakeholders (Business & Technical)
* **Facility Management (e.g., University or Mall Management):** The owners of the parking facility. They are interested in maximizing revenue, optimizing space usage, and reducing traffic congestion on their premises.
* **System Maintenance & IoT Technicians:** The technical team responsible for ensuring that physical sensors, cameras, and barriers remain operational and connected to the central database.
* **Developers (Our group):** The software engineering team responsible for designing, building, and maintaining the system architecture.

* ### Main Requirements

#### Functional Requirements
1.  **Real-Time Monitoring:** The system must utilize IoT sensors and cameras to detect vehicle presence and update the database with the current status (Occupied/Free) of every parking spot instantly.
2.  **Reservation Management:** Registered users must be able to search for available spots and reserve a specific location for a defined time slot via the mobile application.
3.  **Automated Access Control:** The entry/exit barriers must automatically open upon recognizing a valid license plate or scanning a valid reservation QR code.
4.  **Guidance System:** The system must provide visual navigation (via app or on-site displays) to guide the driver to their assigned or nearest available spot.
5.  **Payment Processing:** The system must calculate parking fees based on duration and allow users to make secure payments using credit cards or digital wallets.
6.  **Admin Dashboard:** Administrators must be able to view live occupancy heatmaps, generate revenue reports, and configure pricing rules (e.g., peak vs. off-peak hours).

#### Non-Functional Requirements
1.  **Performance:** The system must update parking spot availability status on the user app within 5 seconds of a sensor state change.
2.  **Scalability:** The backend architecture must support the addition of new sensors and parking zones without requiring significant system downtime.
3.  **Reliability:** The system must maintain 99.9% uptime, with a failover mechanism for the barrier gates in case of network loss (e.g., manual override).
4.  **Security:** All payment transactions and user data (including license plates and passwords) must be encrypted in transit and at rest.
5.  **Usability:** The mobile application interface should be intuitive, requiring no more than 3 clicks to reserve a spot.


### Assumptions

1.  **Hardware Availability:** We assume that the necessary hardware infrastructure (IoT ultrasonic sensors, ANPR cameras, and automated barrier gates) is already installed and functional at the parking facility.
2.  **Network Connectivity:** The parking facility is equipped with a stable, high-speed internet connection to ensure real-time communication between the local sensors and the central cloud server.
3.  **User Technology:** All users (drivers) possess a smartphone with an active internet connection to access the mobile application for reservations and payments.
4.  **Payment API Integration:** A third-party Payment Gateway API (PayPal) is available for integration and handles the actual processing of credit card transactions securely.
5.  **Single Vehicle per Spot:** The physical parking spots are standard-sized, and one spot accommodates exactly one passenger vehicle.
6.  **Regulatory Compliance:** It is assumed that storing license plate data and user records complies with local privacy regulations and that users consent to data collection upon registration.
