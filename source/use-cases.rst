Digital Key Use Cases
=====================================================

Introduction
------------

The ``CCC Digital Key Standard`` defines a comprehensive set of use cases that demonstrate how digital key technology enables seamless, secure vehicle access and control. These use cases address real-world scenarios for vehicle owners, shared users, fleet operators, and service providers, showcasing the flexibility and security of digital key implementations.

This document outlines the primary use cases supported by the CCC Digital Key Standard, covering everything from basic vehicle access to advanced sharing and management scenarios.

Primary Use Cases
-----------------

``Owner Pairing and Initial Setup``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:** The vehicle owner establishes the initial digital key relationship with their primary mobile device.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner receives vehicle with digital key capability
   * - 2
     - Downloads OEM's mobile application
   * - 3
     - Authenticates identity through OEM account
   * - 4
     - Completes secure pairing process with vehicle
   * - 5
     - Digital key credential provisioned to device's secure element
   * - 6
     - Owner can now access and start the vehicle

**Key Benefits:**

- Eliminates need for physical key as primary access method
- Secure cryptographic binding between device and vehicle
- Seamless integration with owner's mobile device

**Technologies Used:** NFC, BLE, PKI, Secure Element


``Passive Vehicle Entry``
~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Automatic vehicle unlocking as the owner approaches with their mobile device, without requiring explicit user action.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner approaches vehicle with mobile device in pocket or bag
   * - 2
     - Vehicle detects authorized device via BLE
   * - 3
     - UWB ranging verifies precise device location and distance
   * - 4
     - Mutual authentication performed automatically
   * - 5
     - Vehicle unlocks doors when owner touches door handle
   * - 6
     - Owner enters vehicle and presses start button
   * - 7
     - Vehicle authenticates device again and enables engine start

**Key Benefits:**

- Hands-free convenience
- Enhanced security through distance measurement
- Protection against relay attacks via UWB ranging

**Technologies Used:** BLE, UWB, Anti-Relay Protection


``Active Vehicle Entry``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Manual vehicle access using NFC when passive entry is unavailable (e.g., device battery low, BLE disabled).

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner taps mobile device against vehicle's NFC reader (typically door handle or 
       B-pillar)
   * - 2
     - NFC transaction authenticates device
   * - 3
     - Vehicle unlocks specific door
   * - 4
     - Owner places device on wireless charging pad or NFC reader inside vehicle
   * - 5
     - Vehicle authenticates again for engine start authorization

**Key Benefits:**

- Reliable backup access method
- Works with depleted device battery (using reserved power)
- No internet connectivity required

**Technologies Used:** NFC, Secure Element


``Friend Key Sharing``
~~~~~~~~~~~~~~~~~~

**Description:**
Vehicle owner shares temporary or permanent digital key access with family, friends, or other trusted individuals.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner opens mobile app and selects "Share Key"
   * - 2
     - Owner specifies recipient (phone number, email, or contact)
   * - 3
     - Owner configures permissions and validity period:
       
       - Time restrictions (start/end date, specific hours)
       - Access level (unlock only, full access, trunk only)
       - Frequency (one-time, recurring, permanent)
   * - 4
     - Key sharing invitation sent via secure mailbox system
   * - 5
     - Recipient receives notification and accepts invitation
   * - 6
     - Friend key provisioned to recipient's device
   * - 7
     - Recipient can access vehicle according to granted permissions
   * - 8
     - Owner can monitor usage and revoke access anytime

**Key Benefits:**

- Flexible sharing with granular permission control
- No physical key exchange needed
- Real-time monitoring and remote management
- Instant revocation capability

**Technologies Used:** E2EE, Mailbox, Remote Key Management


``Valet Mode``
~~~~~~~~~~

**Description:**
Limited-access key for valet parking attendants or service personnel with restricted vehicle functions.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner creates temporary valet key in mobile app
   * - 2
     - Owner configures restrictions:
       
       - Limited driving distance or speed
       - Trunk and glove box locked
       - Infotainment system restricted
       - Time-limited access (e.g., 4 hours)
   * - 3
     - Valet receives one-time access code or limited digital key
   * - 4
     - Valet can unlock, drive, and park vehicle within restrictions
   * - 5
     - Key automatically expires after set duration
   * - 6
     - Owner receives notification when key expires or is revoked

**Key Benefits:**

- Protected privacy (locked compartments)
- Limited vehicle capabilities
- Automatic expiration
- Activity logging and tracking

**Technologies Used:** Access Control, Authorization, Key Lifecycle Management


``Fleet and Rental Vehicle Management``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Commercial fleet operators and rental companies manage vehicle access for multiple users dynamically.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Customer books rental vehicle through app or website
   * - 2
     - Fleet management system generates time-bound digital key
   * - 3
     - Digital key provisioned to customer's device at rental start time
   * - 4
     - Customer accesses vehicle using digital key during rental period
   * - 5
     - Fleet system monitors vehicle usage and location
   * - 6
     - Digital key automatically revoked at rental end time
   * - 7
     - Next customer receives new digital key for same vehicle

**Key Benefits:**

- No physical key exchange or counter visits needed
- Dynamic key assignment to any available vehicle
- Automated key lifecycle management
- Real-time fleet monitoring and control
- Reduced operational costs

**Technologies Used:** Remote Key Management, Key Tracking, Revocation, OTA


``Delegated Access for Service and Maintenance``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Temporary vehicle access granted to dealership service technicians, mechanics, or mobile service providers.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner schedules service appointment through OEM app
   * - 2
     - Owner authorizes temporary service key with specific validity period
   * - 3
     - Service provider receives notification with access details
   * - 4
     - Technician accesses vehicle at scheduled time
   * - 5
     - Service work completed with activity logged
   * - 6
     - Key automatically expires after service window
   * - 7
     - Owner receives service completion report

**Key Benefits:**

- Secure access for authorized service personnel
- No need to leave physical keys at dealership
- Automated access control and logging
- Transparency in service activities

**Technologies Used:** Authorization, Key Tracking, Time-based Access Control


``Family Vehicle Sharing``
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Multiple family members with permanent or long-term access to shared household vehicle.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Vehicle owner (primary) shares permanent keys with family members
   * - 2
     - Each family member receives full or customized access permissions:
       
       - Teenage driver: Speed/location monitoring, time restrictions
       - Spouse: Full access with equal permissions
       - Elderly parent: Full access with simplified interface
   * - 3
     - All family members can access vehicle independently
   * - 4
     - Primary owner can monitor usage and adjust permissions
   * - 5
     - Emergency access available to all authorized family members

**Key Benefits:**

- Convenient multi-user access
- Customizable permissions per user
- Usage tracking and monitoring
- Centralized family vehicle management

**Technologies Used:** Key Sharing, Access Control, Remote Key Management


``Vehicle Sharing Services (Car Sharing)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Short-term vehicle access for peer-to-peer or commercial car sharing platforms.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - User finds available vehicle on car sharing platform
   * - 2
     - User reserves vehicle for specific time slot
   * - 3
     - Platform provisions time-bound digital key to user's device
   * - 4
     - User locates vehicle and unlocks via digital key
   * - 5
     - User drives vehicle during reserved period
   * - 6
     - User returns vehicle to designated location
   * - 7
     - Digital key automatically revoked at reservation end
   * - 8
     - Next user receives new key for subsequent reservation

**Key Benefits:**

- Seamless vehicle access without key exchange
- Automated reservation-based access control
- Usage-based billing integration
- Scalable for large fleets

**Technologies Used:** Remote Key Management, Time-based Authorization, Key Lifecycle


``Emergency Access``
~~~~~~~~~~~~~~~~~~

**Description:**
Special access scenarios for emergency responders or roadside assistance.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Emergency situation detected (accident, medical emergency)
   * - 2
     - Owner or emergency responder initiates emergency access request
   * - 3
     - System generates temporary emergency key with appropriate permissions
   * - 4
     - First responders or roadside assistance access vehicle
   * - 5
     - Emergency key provides necessary access level:
       
       - Medical emergency: Full access to assist passengers
       - Towing: Unlock and neutral gear access
       - Roadside assistance: Hood/trunk access for repairs
   * - 6
     - Emergency access automatically logged and reported
   * - 7
     - Owner receives notification of emergency access event

**Key Benefits:**

- Rapid response in emergency situations
- Controlled access for specific emergency scenarios
- Complete audit trail
- Integration with emergency services

**Technologies Used:** Remote Key Management, Authorization, Emergency Protocols


``Multi-Device Support``
~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Single user manages digital keys across multiple personal devices (smartphone, smartwatch, tablet).

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner has digital key on primary smartphone
   * - 2
     - Owner adds smartwatch as secondary device
   * - 3
     - Digital key replicated to smartwatch with sync
   * - 4
     - Owner can use either device for vehicle access
   * - 5
     - If phone is lost, owner can revoke phone's key and continue using watch
   * - 6
     - Tablet added for in-vehicle infotainment control only

**Key Benefits:**

- Flexibility across multiple devices
- Redundancy if one device is unavailable
- Device-specific permissions possible
- Seamless device switching

**Technologies Used:** Key Provisioning, Multi-device Management, Secure Element


``Remote Vehicle Control``
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Owner remotely controls vehicle functions from anywhere with internet connectivity.

**Flow:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner opens mobile app while away from vehicle
   * - 2
     - Owner performs remote actions:
       
       - Lock/unlock doors
       - Start/stop engine
       - Climate control (temperature settings, fans control)
       - Open/close trunk
       - Flash lights and honk horn (vehicle location)
       - Check vehicle status (fuel, location, tire pressure)
   * - 3
     - Commands sent via secure cloud connection to vehicle
   * - 4
     - Vehicle authenticates commands and executes
   * - 5
     - Status confirmation returned to owner's device

**Key Benefits:**

- Remote climate control before entering
- Vehicle location tracking
- Security monitoring
- Convenience commands

**Technologies Used:** OTA, Remote Key Management, Secure Channel


``Key Revocation and Recovery``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:**
Owner manages lost, stolen, or compromised device scenarios.

**Flow:**

**Lost Device Scenario:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner realizes device is lost
   * - 2
     - Owner logs into OEM account from another device or web portal
   * - 3
     - Owner remotely revokes lost device's digital key
   * - 4
     - Lost device can no longer access vehicle
   * - 5
     - Owner provisions new key to replacement device
   * - 6
     - Vehicle access restored with new device

**Device Theft Scenario:**

.. list-table::
   :header-rows: 1
   :widths: 10 90

   * - Step
     - Action
   * - 1
     - Owner reports device stolen
   * - 2
     - Owner immediately revokes all keys remotely
   * - 3
     - System notifies vehicle to reject revoked credentials
   * - 4
     - Stolen device cannot access vehicle even if unlocked by thief
   * - 5
     - Owner generates new keys on secure device

**Key Benefits:**

- Immediate remote revocation capability
- No need to rekey vehicle like physical locks
- Quick recovery with new device
- Enhanced security

**Technologies Used:** Remote Key Management, Revocation, Key Lifecycle


Advanced Use Cases
---------------------

``Subscription-Based Vehicle Features``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Digital keys integrated with feature subscriptions (e.g., performance modes, autonomous driving) where key permissions dynamically enable/disable based on active subscriptions.

``Autonomous Valet Parking``
~~~~~~~~~~~~~~~~~~~~~~~~~
- Digital key authorizes vehicle to autonomously park itself in designated parking structures without driver present.

``Vehicle Delivery Services``
~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Temporary keys for delivery drivers to access vehicle trunk for package delivery while owner is away (trunk-only access).

``Corporate Fleet Management``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Enterprise-level management of hundreds or thousands of vehicles with role-based access control, reporting, and compliance monitoring.

``Hotel and Hospitality Integration``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Hotel guests receive temporary digital key for hotel-provided vehicles as part of stay package, integrated with room access systems.

Security and Privacy Considerations
------------------------------------

All use cases implement:

- **End-to-end encryption** for key sharing and communication
- **Mutual authentication** between device and vehicle
- **Anti-relay protection** using UWB ranging
- **Secure element storage** for cryptographic keys
- **Audit logging** for access events
- **Privacy protection** for location and usage data
- **Revocation capabilities** for compromised credentials

Implementation Requirements
----------------------------

To support these use cases, implementations must include:

1. **Secure Element (SE)** for credential storage
2. **Multiple wireless technologies** (BLE, NFC, UWB)
3. **Backend key management system** (KMS)
4. **Mobile application** for user interface
5. **Vehicle integration** with authentication systems
6. **Cloud connectivity** for remote management
7. **Compliance with CCC specifications** for interoperability

Conclusion
----------

The ``CCC Digital Key Standard's Use Cases`` demonstrate the technology's versatility in addressing diverse scenarios from personal vehicle ownership to commercial fleet operations. By providing secure, flexible, and convenient vehicle access solutions, digital keys are transforming how people interact with vehicles in the connected mobility ecosystem.

These use cases continue to evolve as technology advances and new requirements emerge, ensuring digital key systems remain relevant and valuable for all stakeholders in the automotive industry.