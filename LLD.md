# Low-Level Design (LLD) for Blood Bank Management System

## User Management

### Overview

- **Responsibility**: Manages user registration, authentication, and authorization.
- **Technologies**: Django, SQLite

### Detailed Specifications

1. **User Registration**

   - Inputs: Username, Email, Password
   - Validation: Email format, strong password requirements
   - Actions: Create user record in database, send confirmation email

2. **Authentication**

   - Inputs: Username, Password
   - Validation: Verify credentials against stored records
   - Actions: Grant access to authenticated users

3. **Authorization**

   - Roles: Admin, Staff, Donor
   - Actions: Define permissions based on roles
   
## Donation Management

### Overview

- **Responsibility**: Manages blood donation appointments and records.
- **Technologies**: Django, SQLite

### Detailed Specifications

1. **Appointment Scheduling**

   - Inputs: Donor details, preferred date/time
   - Actions: Create appointment record, send confirmation to donor

2. **Donation Recording**

   - Inputs: Donor details, blood type, quantity
   - Actions: Record donation in database, update inventory

## Inventory Management

### Overview

- **Responsibility**: Tracks blood units in the inventory.
- **Technologies**: Django, SQLite

### Detailed Specifications

1. **Inventory Update**

   - Inputs: Blood type, quantity
   - Actions: Add/remove blood units, update availability status

## Transfusion Management

### Overview

- **Responsibility**: Manages blood transfusion requests and records.
- **Technologies**: Django, SQLite

### Detailed Specifications

1. **Request Processing**

   - Inputs: Hospital details, blood type, quantity
   - Actions: Process request, update inventory after approval

## Notifications

### Overview

- **Responsibility**: Sends notifications to users about appointments and inventory updates.
- **Technologies**: Celery, Email, SMS (if integrated)

### Detailed Specifications

1. **Event-Based Notifications**

   - Events: Appointment confirmation, low inventory alert
   - Actions: Send email/SMS notifications based on event triggers

