Term Definitions and Abbreviations
=====================================================

Introduction
------------

This document provides comprehensive definitions of terms and abbreviations used in the ``CCC Digital Key Standard`` and related vehicle access technologies. Understanding this terminology is essential for anyone working with digital key implementations, from developers and engineers to product managers and certification specialists.

General Terms
-------------

``Digital Key``
    - A secure credential stored on a mobile device (smartphone, smartwatch, etc.) that enables keyless vehicle access, starting, and control functions through wireless communication.

``Owner Pairing``
    - The initial secure binding process between a vehicle and the owner's mobile device, establishing the primary digital key relationship.

``Friend Key``
    - A digital key credential that can be shared by the vehicle owner with other users, granting temporary or permanent access to the vehicle with configurable permissions.

``Key Sharing``
    - The process of securely distributing digital key credentials from the owner to other authorized users.

``Pairing``
    - The cryptographic process of establishing a trusted relationship between a mobile device and a vehicle's digital key system.

``Mailbox``
    - A secure server-based storage mechanism for temporarily holding digital key credentials and messages during the sharing process.

Device and Hardware Terms
--------------------------

``Mobile Device / End-Entity Device``
    - The smartphone, smartwatch, or other personal device that stores and uses the digital key credential.

``Secure Element (SE)``
    - A tamper-resistant hardware component in a mobile device that securely stores cryptographic keys and executes sensitive operations.

``Embedded Secure Element (eSE)``
    - A secure element permanently integrated into a device's hardware.

``Universal Integrated Circuit Card (UICC)``
    - A smart card used in mobile devices (SIM card) that can function as a secure element for digital key storage.

``Key Applet``
    - The application software running within the secure element that manages digital key operations and cryptographic functions.

``Vehicle Head Unit``
    - The vehicle's central computing and communication system that manages digital key authentication and access control.

``Passive Entry Passive Start (PEPS)``
    - Traditional keyless entry system using radio frequency key fobs; digital keys often integrate with or replace PEPS systems.

Communication Technologies
---------------------------

``Near Field Communication (NFC)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Short-range wireless technology (typically <10 cm) used for secure communication between a mobile device and vehicle, often for backup access when BLE is unavailable.

``Bluetooth Low Energy (BLE)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Energy-efficient wireless protocol used for passive vehicle access, enabling automatic unlock as the device approaches the vehicle.

``Ultra-Wideband (UWB)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Advanced wireless technology providing precise distance measurement and spatial awareness for secure proximity-based vehicle access.

``Ranging``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - The process of accurately measuring the distance between a mobile device and vehicle using UWB or other technologies to prevent relay attacks.

``Passive Entry``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Automatic vehicle unlocking when an authorized device comes within range, without requiring user interaction.

``Active Entry``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Vehicle access requiring explicit user action, such as tapping the device against an NFC reader.

Security and Cryptography Terms
--------------------------------

``Attestation``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Cryptographic proof verifying the authenticity and integrity of a device, secure element, or digital key credential.

``Mutual Authentication``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Two-way authentication process where both the vehicle and mobile device verify each other's identity before granting access.

``Public Key Infrastructure (PKI)``
    - A framework of cryptographic keys, certificates, and certificate authorities used to establish trust in digital key systems.

``Certificate Authority (CA)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - A trusted entity that issues digital certificates to verify the identity of devices and entities in the digital key ecosystem.

``Elliptic Curve Cryptography (ECC)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Modern cryptographic algorithm used in digital key systems for efficient public key operations.

``Advanced Encryption Standard (AES)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Symmetric encryption algorithm used to protect digital key communications and stored data.

``End-to-End Encryption (E2EE)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Security mechanism ensuring that key sharing communications are encrypted from sender to recipient, preventing intermediary access.

``Secure Channel``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - An encrypted communication path between two entities, protecting data from eavesdropping and tampering.

``Key Diversification``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Process of generating unique cryptographic keys for different contexts or users from a master key.

``Anti-Relay Protection``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Security measures (typically using UWB ranging) to prevent attackers from relaying signals between a device and vehicle to gain unauthorized access.

Operational Terms
-----------------

``Transaction``
~~~~~~~~~~~~~~~~~~~~
    - A complete authentication and command exchange sequence between a mobile device and vehicle.

``Authorization``
~~~~~~~~~~~~~~~~~~~
    - The process of verifying that a device has permission to perform specific vehicle operations.

``Access Control``
    - System managing which users and devices can access the vehicle and what operations they can perform.

``Revocation``
~~~~~~~~~~~~~~~~
    - The process of invalidating a digital key credential, preventing further access.

``Key Lifecycle``
~~~~~~~~~~~~~~~~~
    - The complete process from key creation, provisioning, usage, updating, to eventual revocation and deletion.

``Provisioning``
~~~~~~~~~~~~~~~~
    - The process of securely installing a digital key credential onto a mobile device's secure element.

``Key Tracking``
~~~~~~~~~~~~~~~~
    - Monitoring and logging of which digital keys exist, who has them, and their current status.

``Remote Key Management``
~~~~~~~~~~~~~~~~~~~~~~~~
    - Server-based system for managing digital keys, including creation, sharing, revocation, and monitoring.

Protocol and Standard Terms
----------------------------

``Application Protocol Data Unit (APDU)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Command and response messages exchanged between applications and secure elements.

``Over-The-Air (OTA)``
~~~~~~~~~~~~~~~~~~~~~~
    - Wireless delivery and update of software, credentials, or configuration to devices or vehicles.

``Key Management System (KMS)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Backend infrastructure managing digital key lifecycle, user accounts, and access policies.

``Trust Service Provider (TSP)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Entity providing secure credential provisioning and management services for digital keys.

``Original Equipment Manufacturer (OEM)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Vehicle manufacturer integrating digital key capabilities into their vehicles.

``Tier 1 Supplier``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    - Companies providing major automotive systems and components to OEMs, often including digital key hardware.

Abbreviations
-------------

.. list-table::
   :header-rows: 1
   :widths: 20 80

   * - Abbreviation
     - Full Form
   * - CCC
     - Car Connectivity Consortium
   * - BLE
     - Bluetooth Low Energy
   * - NFC
     - Near Field Communication
   * - UWB
     - Ultra-Wideband
   * - SE
     - Secure Element
   * - eSE
     - Embedded Secure Element
   * - UICC
     - Universal Integrated Circuit Card
   * - PKI
     - Public Key Infrastructure
   * - CA
     - Certificate Authority
   * - ECC
     - Elliptic Curve Cryptography
   * - AES
     - Advanced Encryption Standard
   * - E2EE
     - End-to-End Encryption
   * - APDU
     - Application Protocol Data Unit
   * - OTA
     - Over-The-Air
   * - KMS
     - Key Management System
   * - TSP
     - Trust Service Provider
   * - OEM
     - Original Equipment Manufacturer
   * - PEPS
     - Passive Entry Passive Start
   * - RKE
     - Remote Keyless Entry
   * - API
     - Application Programming Interface
   * - SDK
     - Software Development Kit
   * - TLS
     - Transport Layer Security
   * - FIPS
     - Federal Information Processing Standards
   * - ISO
     - International Organization for Standardization
   * - IEEE
     - Institute of Electrical and Electronics Engineers
   * - ECDSA
     - Elliptic Curve Digital Signature Algorithm
   * - HMAC
     - Hash-based Message Authentication Code
   * - UUID
     - Universally Unique Identifier
   * - MAC
     - Message Authentication Code (or Media Access Control)

Usage Notes
-----------

- Terms may have slightly different meanings in different contexts; refer to the specific CCC Digital Key specification section for precise definitions
- Some abbreviations are used differently in other industries; this document focuses on digital key and automotive contexts
- New terms and abbreviations are regularly added as the technology evolves

Related Resources
-----------------

- ``CCC Digital Key Specification``: Complete technical definitions
- ``RFC 2119``: Key words for requirement levels
- ``ISO/IEC Standards``: International automotive and security standards
- ``Bluetooth SIG Specifications``: BLE protocol details
- ``NFC Forum Specifications``: NFC technical standards
- ``FIRA Consortium``: UWB specifications and standards