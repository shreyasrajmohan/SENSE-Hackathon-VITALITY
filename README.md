# Problem Statement: Development of “VITALITY” – A Dynamic Student Marketplace Platform

The goal is to design and develop VITALITY, a full-stack web application tailored for college students to buy, sell, and request products/services within a secure and moderated ecosystem. The platform combines a community-driven pricing model, a time-bound auction system, and a request-fulfillment forum, ensuring fairness, engagement, and usability.

## Core Problem
Existing student marketplaces lack:
Fair, community-influenced pricing
Structured seller and product approval workflows
Transparent and controlled auction mechanisms
A system for posting and fulfilling specific product/service requests
Anonymous yet secure communication between users
Robust complaint and moderation systems
VITALITY addresses these gaps by introducing a multi-role, moderated, and interaction-driven platform.

## Objectives

### 1. User Management System
Enable user registration and login
Define three roles:
Admin
Seller
Buyer
Allow Buyers to apply for Seller role via admin approval
Enable Admins to downgrade Sellers if required

### 2. Seller Approval Workflow
Provide a rate-limited form (max 2 submissions/hour)
Collect:
Full Name
Registration Number
Phone Number
Hostel Block & Room Number
Send submissions to Admin dashboard
Notify users upon approval/rejection

### 3. Product Listing & Moderation
Sellers submit products with:
Unique Product ID
Category (For Him / For Her / For Everyone)
Name
Description
Base Price
At least one image
Admin approval required before listing
Seller notified of approval/rejection

### 4. Community-Based Pricing System
Each product has a minimum base price
Buyers suggest a fair price
System calculates average price → Listing Price

### 5. Auction System
Approved products go live daily from 12:00 PM to 11:59 PM
Product is:
Sold at listing price if no higher bids
Sold to highest bidder otherwise
Sold products remain in database but become invisible

### 6. Product Request & Fulfillment Forum (New Feature)
A dedicated forum where users can request products or services they need.
Process Flow
A Requester (Buyer) posts a requirement in the forum
Request includes:
Description of requirement
Optional images/details
A settled price they are willing to pay
Fulfillment Mechanism
Any eligible user (Completer, typically Seller) can accept the request
Assignment follows First Come First Serve (FCFS) basis
Once accepted, the request is locked for others
Anonymous Communication
Requester and Completer communicate through an anonymous in-platform chat system
Personal identities are hidden to ensure privacy
Transaction Completion via OTP
Both parties receive unique One-Time Passwords (OTPs)
Exchange is considered complete only when:
Each party enters the other party’s OTP into their account
Ensures:
Mutual confirmation
Fraud prevention
Trustless but secure exchange

### 7. Complaint & Support System
Buyers can report:
Misleading or inappropriate products
Sellers can report:
Non-cooperative buyers
Admin manages all complaints via dashboard

### 8. User Interface & Experience
Frosted glass (glassmorphism) design
Homepage split into:
For Him (Blue)
For Her (Pink)
For Everyone (Colorful)
Category-based product visibility
Smooth animations and hover effects
Custom cursor (small dot style)

## Technical Requirements
Frontend: HTML, CSS, JavaScript (React / Next.js preferred)
Backend: Node.js or Python (Django/Flask)
Database: PostgreSQL / MongoDB
Authentication: Secure login (JWT/session-based)
Real-time Features: Chat + auction updates
Security: Rate limiting, OTP verification, role-based access

## Expected Outcome
A robust, scalable, and visually engaging platform that:
Enables fair product pricing through community input
Supports auctions and direct request fulfillment
Ensures secure and anonymous transactions
Maintains trust through admin moderation
Enhances student-to-student commerce within a closed ecosystem

