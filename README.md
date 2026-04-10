# Smart Elevator Control System ERD

## Overview

This project presents an **Entity Relationship Diagram (ERD)** for a smart elevator control platform used in large multi-building infrastructures such as corporate towers, malls, airports, hospitals, and residential complexes.

The system manages elevator operations including **floor requests, ride allocation, elevator status tracking, maintenance management, and ride history logging**.

---

##  Key Features

- Handles complete flow: **floor request → assignment → ride execution → logging**
- Supports **multiple buildings with multiple elevators**
- Enables **real-time elevator status tracking**
- Allows **multiple elevators serving multiple floors**
- Tracks **pending, assigned, and completed requests**
- Maintains **ride history for analytics and optimization**
- Supports **maintenance scheduling without affecting history**
- Scalable for **high-traffic environments (thousands of requests daily)**

---

## Main Entities

- Buildings
- Floors
- Elevator Shafts
- Elevators
- Elevator Status
- Floor Requests
- Ride Assignments
- Ride Logs (Trips)
- Maintenance Records
- Elevator-Floor Mapping

---

##  Relationships

- Building → Floors (1:N)
- Building → Elevators (1:N)
- Building → Elevator Shafts (1:N)
- Elevator Shaft → Elevator (1:1)
- Elevator → Status Records (1:N)
- Elevator → Maintenance Records (1:N)
- Elevator → Ride Logs (1:N)
- Floor → Floor Requests (1:N) *(as source & destination)*
- Floor Request → Ride Assignment (1:1)
- Elevator → Ride Assignments (1:N)
- Elevator ↔ Floors (M:N via ElevatorFloorMap)
- Floor Request → Ride Log (1:1)
