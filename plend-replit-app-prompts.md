# Plend Replit App Prompts

## Note
You asked for a document that will surface **two prompts**, but only specified the first one:

1. Client facing mobile app

So I created the first prompt properly and left a clean slot for the second prompt once you define it.

---

## Prompt 1. Client-facing mobile app

Build a polished **mobile-first app** for **Plend**, a premium local business that provides:
- themed decoration for kids birthday parties
- rental of toddler-safe game stations / soft play setups
- delivery, setup, supervision, teardown, and pickup

### Business context
Plend serves families with children **under 6 years old**.
Initial service area:
- Gavà Mar
- Castelldefels

The app should feel like a **premium boutique party planning experience**, not a generic party marketplace.

### Main goal
Create a client-facing mobile app where parents can:
- discover Plend packages
- browse themes
- understand pricing starting points
- see examples of setups
- request a quote
- select preferred date, location, child age, and event details
- chat or contact Plend easily
- submit a booking inquiry

### Product requirements

#### Core screens
1. **Home screen**
   - strong hero section
   - premium visual presentation
   - short explanation of the service
   - CTA to explore packages or request a quote

2. **Packages screen**
   - show launch packages:
     - Mini Deco
     - Mini Play
     - Signature Plend
     - Premium Plend
   - each package should include:
     - summary
     - ideal use case
     - key inclusions
     - starting price

3. **Themes screen**
   - show launch themes with beautiful cards
   - each theme should have:
     - name
     - visual placeholder/image area
     - short description
     - age fit / vibe

4. **Gallery / Inspiration screen**
   - showcase party setups and visual inspiration
   - optimized for mobile browsing
   - elegant, image-forward layout

5. **Quote request screen**
   - form fields:
     - parent name
     - phone
     - email
     - child age
     - event date
     - location
     - preferred package
     - preferred theme
     - number of children
     - indoor/outdoor
     - notes
   - submit as inquiry, not instant booking

6. **Service area / FAQ screen**
   - explain where Plend operates
   - simple FAQs about setup, supervision, duration, safety, and booking flow

7. **Contact screen**
   - WhatsApp CTA
   - email CTA
   - Instagram CTA

### UX / UI direction
- mobile-first design
- premium, soft, elegant visual style
- not childish in a tacky way
- warm, polished, modern
- use soft colors, rounded cards, clean spacing
- make the brand feel trustworthy and worth paying for

### Functional behavior
- app can be a frontend MVP with mocked data first
- package and theme data should come from local JSON or seed data
- quote requests can initially store submissions locally or send to a mock backend endpoint
- architecture should be easy to evolve into a real production app

### Technical requirements
- build this as a **mobile app MVP** that can run well in Replit
- prefer a stack that Replit can handle smoothly
- if native mobile is too heavy for MVP, use a **React-based mobile-first web app** that behaves like an app and can later become a PWA
- code should be clean, modular, and easy to extend
- separate components, data models, and screens clearly

### Suggested MVP data model
- Package
  - id
  - name
  - summary
  - startingPrice
  - inclusions
  - idealFor
- Theme
  - id
  - name
  - description
  - image
- Inquiry
  - id
  - parentName
  - phone
  - email
  - childAge
  - eventDate
  - location
  - packageId
  - themeId
  - guestCount
  - indoorOutdoor
  - notes

### Copy direction
Use language like:
- beautiful birthday moments for little ones
- safe play, beautiful parties, zero stress
- boutique under-6 birthday setups
- we handle the setup so parents enjoy the day

### Deliverable
Generate:
- app structure
- core screens
- reusable components
- sample seed data
- clean styling system
- working inquiry form flow

The output should feel like the **first real MVP for a premium Plend customer experience**.

---

## Prompt 2. Backoffice website to manage the business

Build a **backoffice web application** for **Plend** to manage the day-to-day operation of the business.

Plend is a premium local kids birthday service business that provides:
- themed decoration
- toddler-safe game station / soft play rental
- delivery and setup
- on-site supervision
- teardown and pickup

The backoffice should help the business operate cleanly, not just store random information.

### Main goal
Create an internal admin system where Plend can manage:
- leads and inquiries
- bookings
- customers
- packages and themes
- calendar and availability
- staff assignments
- inventory and assets
- logistics and setup checklists
- payments / quote status

### Product vision
This should feel like a lightweight but serious business control panel.

Not an enterprise monster.
Not a toy CRUD demo.

It should help a small local team run the business with clarity.

### Core modules

#### 1. Dashboard
Show:
- upcoming events
- pending inquiries
- bookings by status
- revenue snapshot
- items requiring attention
- inventory alerts or missing assets

#### 2. Leads / inquiries
Manage incoming quote requests from the client-facing app or manual entry.

Each inquiry should include:
- parent name
- phone
- email
- child age
- location
- date
- preferred package
- preferred theme
- number of kids
- notes
- inquiry status

Statuses can include:
- new
- contacted
- quoted
- won
- lost

#### 3. Bookings
Convert accepted inquiries into bookings.

Each booking should include:
- customer details
- event address
- event date and time
- selected package
- selected theme
- assigned staff
- add-ons
- setup time
- teardown time
- supervision duration
- booking status

Statuses can include:
- draft
- confirmed
- in preparation
- completed
- canceled

#### 4. Calendar / scheduling
Provide a calendar view for:
- booked events
- setup windows
- pickup windows
- staff assignments
- blocked dates

#### 5. Packages and themes management
Allow admin to:
- create/edit packages
- create/edit themes
- update starting prices
- manage package inclusions
- manage visible/hidden status

#### 6. Inventory and assets
Track reusable event assets such as:
- soft play modules
- ball pits
- mats
- signs
- balloon structures
- decor props
- storage bins

Each asset should support:
- name
- category
- quantity
- condition
- storage location
- assigned event
- notes

#### 7. Event operations / checklists
Each booking should have task checklists for:
- prep
- loading
- setup
- supervision
- teardown
- cleaning/reset
- storage return

#### 8. Customer records
Store customers and their past events so Plend can:
- see repeat clients
- track preferences
- improve upsells
- remember previous themes and child ages

#### 9. Financial tracking light module
Not full accounting, just operational money tracking.

Track:
- quote amount
- deposit status
- payment status
- total booking value
- notes

### UX / UI direction
- clean admin dashboard feel
- fast and practical
- mobile responsive but optimized for desktop/tablet backoffice use
- visually aligned with Plend brand, but more functional than decorative
- use cards, tables, filters, and clear statuses

### Technical requirements
- build it in a Replit-friendly stack
- prefer a modern web stack such as React + backend API
- can start as a full-stack MVP with local/mock persistence first
- structure code so a real database can be added cleanly later
- keep components modular and business entities explicit

### Suggested data model
- Customer
- Inquiry
- Booking
- Package
- Theme
- Asset
- StaffMember
- Checklist
- PaymentRecord

### Suggested MVP deliverable
Generate:
- admin dashboard
- inquiry management
- booking management
- package/theme management
- inventory module
- event checklist module
- sample seed data
- clear navigation structure

### Important business logic
- inquiries and bookings are different entities
- one inquiry can become one booking
- inventory should be assignable to events
- event operations must be checklist-based
- package and theme definitions should be editable by admin

### Output style
The final output should feel like the **first real internal operating system for Plend**, built for a small premium events business that needs operational control without complexity bloat.

---

## Prompt 3. Master Replit prompt for both apps in one system

Build a **single unified system for Plend** that includes:
1. a **client-facing mobile-first app** for parents
2. a **backoffice web app** for the internal business team

Both should belong to the same product system, share the same core data model, and be designed so the business can evolve from MVP to a real operating platform.

### Business context
Plend is a premium local children’s birthday service business focused on:
- themed decoration
- toddler-safe game station / soft play rental
- delivery, setup, supervision, teardown, and pickup

Target customer:
- families with children under 6 years old

Initial service area:
- Gavà Mar
- Castelldefels

### System objective
Build one system with two experiences:

#### A. Client-facing app
Used by parents to:
- discover packages
- browse themes
- see examples and inspiration
- submit booking / quote inquiries
- understand pricing starting points
- contact Plend easily

#### B. Backoffice app
Used by Plend staff/admin to:
- manage inquiries
- convert inquiries into bookings
- manage customers
- manage packages and themes
- manage event schedule and availability
- assign staff
- manage inventory and reusable assets
- run setup / teardown / cleaning checklists
- track quote and payment status

### Product architecture requirement
This should **not** be built as two unrelated apps.

It should be one coherent system with:
- shared backend logic
- shared core entities
- separate frontends or separate app sections as needed
- one source of truth for inquiries, packages, themes, bookings, and assets

### Recommended MVP architecture
Build a Replit-friendly full-stack system, such as:
- frontend for client-facing experience
- frontend for backoffice experience
- shared backend API
- local JSON / mock DB or lightweight database for MVP
- clean path to upgrade to real persistence later

If needed, the client-facing app can be implemented as a **mobile-first responsive web app / PWA** rather than a fully native mobile app for the MVP.

### Shared core entities
At minimum, define and use these entities across the system:
- Customer
- Inquiry
- Booking
- Package
- Theme
- Asset
- StaffMember
- Checklist
- PaymentRecord

### Required business logic
- a user inquiry should be created from the client-facing app
- the inquiry must appear in the backoffice
- an admin can convert an inquiry into a booking
- bookings should be assignable to dates, staff, themes, packages, and assets
- event operations should include checklist flows
- package and theme content should be editable in the backoffice and reflected in the client-facing app

### Client-facing app requirements

#### Main screens
- Home
- Packages
- Themes
- Gallery / Inspiration
- Quote Request
- FAQ / Service Area
- Contact

#### Experience goals
- premium
- soft, elegant, mobile-first
- trustworthy
- not tacky or generic
- easy for a parent to understand and inquire quickly

#### Core CTA
- request a quote
- send event details
- contact via WhatsApp / email / Instagram

### Backoffice app requirements

#### Main modules
- Dashboard
- Inquiries
- Bookings
- Calendar
- Customers
- Packages
- Themes
- Inventory / Assets
- Event Checklists
- Payments / Quote Status

#### Experience goals
- practical
- fast
- clean
- good for desktop/tablet
- easy for a small local business to operate daily

### UX/UI direction

#### Client-facing app
- mobile-first
- rounded cards
- soft premium palette
- emotionally warm
- image-forward

#### Backoffice app
- clean admin layout
- strong information hierarchy
- cards, filters, tables, status badges
- operational clarity over decoration

### MVP deliverables
Generate a working MVP with:
- app structure
- shared data model
- backend routes / API structure
- client-facing screens
- backoffice screens
- sample seed data
- inquiry submission flow
- inquiry-to-booking conversion flow
- package/theme management flow
- inventory assignment concept
- checklist concept per booking

### Technical expectations
- code must be modular and maintainable
- components should be separated cleanly
- data types / interfaces should be explicit
- avoid monolithic messy files
- optimize for clarity and future extension

### Output style
The result should feel like the **first real Plend digital operating system**, with one polished customer-facing experience and one practical internal business interface, both built from the same foundation.
