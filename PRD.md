# Product Requirements Document (PRD)

## Reclaim

*Verified Campus Lost & Found Platform*

| **Field**              | **Details**                        |
|------------------------|------------------------------------|
| **Product Name**       | Reclaim                            |
| **Document Version**   | 1.0 (MVP)                          |
| **Status**             | Draft for Academic Review          |
| **Platform**           | Mobile-First Web Application (PWA) |
| **Target Environment** | University / College Campus        |
| **Date**               | November 23, 2026                  |

## 1. Executive Summary

**Product Vision**

 Reclaim is a centralized, campus-only web platform that connects students who lose valuable items with the finders who recover them. By replacing chaotic, unsearchable departmental and hostel WhatsApp broadcasts with structured item listings, hidden-detail ownership verification, and an optional finder reward system, Reclaim increases item recovery rates while protecting student privacy and safety.

## 2. Problem Statement

Students who misplace high-value or essential items on campus—such as smartphones, student ID cards, AirPods, laptops, and chargers—currently have no organized, trustworthy system to recover them.

- **Fragmented Communication:** "Who lost this?" messages posted across departmental, faculty, and hostel WhatsApp groups are quickly buried under daily chatter and never reach students outside those specific groups.

- **No Ownership Verification:** Broadcasting full item details in public group chats makes it easy for bad actors to falsely claim items that do not belong to them.

- **Lack of Finder Incentive & Friction:** Honest finders around lecture halls, cafeterias, and sports complexes often have no easy way to identify the owner and little motivation to spend time tracking them down.

## 3. Target Audience & User Personas

| **Persona**                            | **Description**                                                                                                    | **Primary Goal**                                                                                                         | **Key Pain Point**                                                                                   |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **The Distressed Owner ("Lost" User)** | A student who just realized their phone, ID card, or charger is missing after leaving a lecture hall or cafeteria. | Broadcast a verified alert quickly, track potential matches, and safely retrieve their item.                             | Spamming 10+ WhatsApp groups with no way to know if anyone found the item.                           |
| **The Campus Finder ("Found" User)**   | A student or staff member who picks up a forgotten item at a sports complex, library, or hostel common area.       | Log the found item in under 60 seconds, verify the real owner without hassle, and optionally receive a thank-you reward. | Doesn't know who owns the item and doesn't want to share their personal phone number with strangers. |
| **Campus Admin / Moderator**           | Student Affairs officer, hostel warden, or campus security staff managing physical drop-off points.                | Log items turned in at the security desk, resolve disputed claims, and archive old posts.                                | Paper logbooks that students never check and piles of unclaimed ID cards and electronics.            |

## 4. Product Goals & Success Metrics (KPIs)

| **Goal**                      | **Metric (KPI)**                                                | **MVP Target (First Semester)** |
|-------------------------------|-----------------------------------------------------------------|---------------------------------|
| **Increase Item Recovery**    | Percentage of reported lost items marked as "Returned"          | At least 35% recovery rate      |
| **Reduce Time-to-Match**      | Median time between posting a found item and owner verification | Under 24 hours                  |
| **Drive Campus Adoption**     | Active verified student accounts                                | 15% of campus student body      |
| **Prevent Fraudulent Claims** | Percentage of claims flagged as fraudulent or disputed          | Less than 2% of total claims    |
| **Encourage Reporting**       | Average time to submit a Lost or Found report                   | Under 60 seconds                |

## 5. Functional Requirements

Requirements are prioritized using the MoSCoW framework: P0 = Must-Have for MVP, P1 = Should-Have, and P2 = Nice-to-Have.

### 5.1 Campus Identity & Authentication

- **[P0] Verified Student Sign-Up:** Users must register using an official institutional email address (e.g., @university.edu) or a verified Student Matriculation/ID number to restrict access to campus members.

- **[P0] Basic User Profile:** Stores name, department, faculty, and verification badge. Personal contact details (phone number/WhatsApp) remain hidden until a claim is approved.

### 5.2 Reporting Lost & Found Items

- **[P0] Structured Reporting Form:** Separate flows for "I Lost Something" and "I Found Something" capturing:

- **Item Title & Category:** Phones, ID Cards, Audio/AirPods, Chargers/Cables, Keys, Books, Bags, Other.

- **Campus Zone:** Lecture Halls, Cafeteria, Library, Sports Complex, Hostels, Admin Block.

- **Date & Approximate Time:** Timestamp of when the item was lost or found.

- **Public Description & Optional Photo Upload:** Auto-blurred or cropped for sensitive items like ID cards.

- **[P0] Verification Challenge Field (Anti-Fraud):** When posting a Found item, the finder adds one hidden verification question (e.g., "What is the lock screen wallpaper?" or "What sticker is on the back of the AirPods case?"). This detail is never shown publicly.

### 5.3 Search, Discovery & Smart Matching

- **[P0] Unified Searchable Feed:** Two distinct tabs (Lost and Found) with keyword search and filters for Category, Campus Zone, Date Posted, and Reward Offered.

- **[P1] Automated Match Alerts:** When a new Lost report matches an existing Found report by Category and Campus Zone (within a 7-day window), the system sends an in-app or email notification to both users.

- **[P1] WhatsApp Share Card Generator:** Generates a clean, formatted summary link (e.g., "Found: White AirPods Case near Science Lecture Hall — Claim on Reclaim") so students can still share a single link into hostel WhatsApp groups that funnels claimants back to the verified platform.

### 5.4 Claim Verification & Safe Handover

- **[P0] Claim Submission Flow:** A student claiming a found item must answer the finder's hidden verification question (and optionally upload proof of ownership, such as a receipt or photo of themselves with the item).

- **[P0] Finder Approval & Masked Contact Unlock:** The finder reviews the claimant's answer. Only after clicking Approve Claim does the platform unlock an in-app chat or reveal a designated handover contact.

- **[P0] Safe Campus Handover Points:** The system prompts users to meet in high-traffic public campus zones (e.g., Student Affairs Office, Library Front Desk, or Security Post) and provides a 6-digit Handover PIN that the owner gives the finder upon receiving the item to officially close the ticket.

### 5.5 Finder Reward (Bounty) System

- **[P0] Optional Reward Pledge:** Owners reporting a lost item can attach an optional reward amount (e.g., "Reward Offered: ₦5,000" or "Appreciation Gift") displayed as a badge on the listing to incentivize finders.

- **[P1] Reward Confirmation & Trust Score:** Once the 6-digit Handover PIN is entered, both parties confirm whether the pledged reward was honored. Finders earn "Campus Hero" reputation points/badges on their profile.

- **[P2] In-App Escrow Wallet (Post-MVP):** Hold pledged rewards via a local payment gateway (e.g., Paystack/Flutterwave) and auto-release funds to the finder only when the owner confirms item handover via PIN.

### 5.6 Admin Moderation & Drop-Off Desk

- **[P1] Admin Dashboard:** Allows authorized campus staff to log items dropped off physically at the security/admin desk, moderate flagged listings, ban repeat false claimants, and auto-archive unresolved posts after 30 days.



## 6. Non-Functional Requirements

- **Security & Privacy:** All passwords hashed; HTTPS enforced; personal phone numbers and sensitive ID card details masked from public view. Uploaded photos stripped of EXIF GPS metadata.

- **Performance:** Feed and search results must load in under 2 seconds on standard campus 3G/4G mobile connections. Images automatically compressed on upload to save student data.

- **Usability (Mobile-First):** Fully responsive web design optimized for smartphones, allowing a student walking out of a lecture hall to post an item in 3 steps or fewer.

- **Reliability:** 99% uptime during active academic semesters, with automated daily database backups.

## 7. Out of Scope for Version 1.0 (MVP)

To ensure timely delivery for the academic project, the following features are deferred to future releases:

- **Native Mobile Apps:** Native iOS and Android applications (v1.0 will be a mobile-first web app).

- **Live Payment Escrow:** Automated in-app financial escrow and bank payouts (v1.0 uses reward pledges settled at physical handover to avoid financial compliance bottlenecks).

- **AI Visual Matching:** AI image recognition for automatic photo-to-photo matching.

- **Hardware Tracking:** Bluetooth/GPS hardware tracker integration.

## 8. Risks & Mitigations

| **Risk**                                                  | **Impact**                                        | **Mitigation Strategy**                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Fraudulent Claims**                                     | High — Items handed to thieves instead of owners. | Mandatory hidden verification question per found item; institutional account verification; ban policy for repeat offenders.                   |
| **Reward Disputes (Owner refuses to pay pledged reward)** | Medium — Erodes finder trust and motivation.      | Clearly label v1.0 rewards as "Voluntary Pledges" settled face-to-face at handover; track user reliability ratings; introduce escrow in v2.0. |
| **Low Initial Adoption ("Everyone still uses WhatsApp")** | High — Empty feed leads to abandonment.           | Built-in Share to WhatsApp button that posts a clean link to hostel/departmental chats, turning WhatsApp into a traffic funnel for Reclaim.   |
| **Exposure of Sensitive Data (ID Cards / Bank Cards)**    | High — Identity theft or privacy breach.          | Warn finders not to upload unblurred photos of ID numbers; default to text-only + hidden verification for ID/card categories.                 |

## 9. Suggested MVP Tech Stack & Rollout Plan

### Recommended Tech Stack

- **Frontend:** React (or Next.js) with Tailwind CSS for a fast, mobile-first UI.

- **Backend & Database:** Firebase (Firestore + Authentication + Storage) or Supabase (PostgreSQL + Auth + Storage) for rapid development and real-time updates.

- **Deployment:** Vercel or Netlify (free tier suitable for campus MVP).

