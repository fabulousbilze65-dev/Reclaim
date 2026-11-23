
PRODUCT REQUIREMENTS DOCUMENT (PRD)

Reclaim

Verified Campus Lost &amp; Found Platform

| **Field**              | **Details**                        |
|------------------------|------------------------------------|
| **Product Name**       | Reclaim                            |
| **Document Version**   | 1.1 (MVP + User Anatomy)           |
| **Status**             | Draft for Academic Review          |
| **Platform**           | Mobile-First Web Application (PWA) |
| **Target Environment** | University / College Campus        |
| **Date**               | November 23, 2026                  |

## 1. Executive Summary


Product Vision

Reclaim is a centralized, campus-only web platform that connects students who lose valuable items with the finders who recover them. By replacing chaotic, unsearchable departmental and hostel WhatsApp broadcasts with structured item listings, hidden-detail ownership verification, and an optional finder reward system, Reclaim increases item recovery rates while protecting student privacy and safety.

## 2. Problem Statement

Students who misplace high-value or essential items on campus—such as smartphones, student ID cards, AirPods, laptops, and chargers—currently have no organized, trustworthy system to recover them.

- **Fragmented Communication:** "Who lost this?" messages posted across departmental, faculty, and hostel WhatsApp groups are quickly buried under daily chatter and never reach students outside those specific groups.

- **No Ownership Verification:** Broadcasting full item details in public group chats makes it easy for bad actors to falsely claim items that do not belong to them.

- **Lack of Finder Incentive & Friction:** Honest finders around lecture halls, cafeterias, and sports complexes often have no easy way to identify the owner and little motivation to spend time tracking them down.

## 3. User Anatomy

This section breaks down the core users of Reclaim across three dimensions: User Persona Anatomy (who the users are and how they behave), User Story Anatomy (what they need the system to accomplish), and User Autonomy (how they retain control over their data and interactions).

### 3.1 Target Audience Overview

| **Persona**                            | **Description**                                                                                                    | **Primary Goal**                                                                                                         | **Key Pain Point**                                                                                   |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **The Distressed Owner ("Lost" User)** | A student who just realized their phone, ID card, or charger is missing after leaving a lecture hall or cafeteria. | Broadcast a verified alert quickly, track potential matches, and safely retrieve their item.                             | Spamming 10+ WhatsApp groups with no way to know if anyone found the item.                           |
| **The Campus Finder ("Found" User)**   | A student or staff member who picks up a forgotten item at a sports complex, library, or hostel common area.       | Log the found item in under 60 seconds, verify the real owner without hassle, and optionally receive a thank-you reward. | Doesn't know who owns the item and doesn't want to share their personal phone number with strangers. |
| **Campus Admin / Moderator**           | Student Affairs officer, hostel warden, or campus security staff managing physical drop-off points.                | Log items turned in at the security desk, resolve disputed claims, and archive old posts.                                | Paper logbooks that students never check and piles of unclaimed ID cards and electronics.            |

### 3.2 User Persona Anatomy

**A. The Distressed Owner ("Lost" User)**

- **Identity & Context:** An undergraduate student living on campus or commuting daily who regularly carries high-value essentials (smartphones, AirPods, laptops, student ID cards, chargers) between lecture halls, cafeterias, libraries, and hostels.

- **Goals & Motivations:** Broadcast a verified lost-item report immediately, discover if someone has already found the item, and recover it safely without paying scammers or waiting days.

- **Pain Points & Frustrations:** Posting across 10+ departmental and hostel WhatsApp groups where messages get buried within minutes; anxiety over identity theft if an ID card photo circulates publicly; uncertainty about whether an item was stolen or simply misplaced.

- **Current Behaviors:** Sends panicked broadcasts in WhatsApp chats, asks friends to repost on WhatsApp statuses, and physically retraces steps around lecture halls or the Student Affairs office.

- **Technical Environment:** Smartphone-first user relying on mobile browsers over campus 3G/4G data; requires a fast, low-data interface that takes under 60 seconds to submit a report.

**B. The Campus Finder ("Found" User)**

- **Identity & Context:** A student or staff member who notices an unattended item in a shared campus space (lecture hall, sports complex, library, or hostel common area).

- **Goals & Motivations:** Log the found item quickly, hand it back to the verified owner with minimal personal disruption, and optionally receive a thank-you reward or campus reputation recognition.

- **Pain Points & Frustrations:** No reliable way to identify the owner; reluctance to share their personal phone number in public group chats; fear of handing an item to a dishonest student making a false claim; lack of incentive to spend time hunting down the owner.

- **Current Behaviors:** Either leaves the item with a security guard or class representative, or drops a quick "Who owns this?" message in a single WhatsApp group and forgets about it.

- **Technical Environment:** Mobile browser user on the move between classes; needs a 3-step posting flow with built-in privacy protection.

**C. Campus Admin / Moderator**

- **Identity & Context:** Student Affairs officer, hostel warden, or campus security personnel responsible for physical lost-and-found drop-off points.

- **Goals & Motivations:** Digitally log items handed in at the security desk, resolve disputed claims fairly, prevent spam or fraudulent accounts, and keep the active item feed clean.

- **Pain Points & Frustrations:** Manual paper logbooks that students rarely check; storage shelves piling up with unclaimed ID cards, keys, and chargers; time wasted mediating ownership disputes.

- **Current Behaviors:** Writes found items in a physical register and waits for students to walk in and ask.

- **Technical Environment:** Desktop or tablet browser at an admin desk; requires search, moderation, and archiving tools.

### 3.3 User Story Anatomy & Acceptance Criteria

Each core feature of Reclaim follows the standard Agile user story anatomy: As a [User Role], I want to [Action], so that [Benefit], paired with measurable acceptance criteria.


Story 1: Verified Campus Sign-Up

User Story:

As a university student, I want to register using my official institutional email or matriculation number, so that only verified members of my campus community can access the platform.

Acceptance Criteria:

•
 The sign-up form rejects non-institutional email domains.

•
 Users receive a verification badge on their profile after confirming their email.

•
 Personal phone numbers remain hidden from public listings by default.


Story 2: Reporting a Lost Item with Reward Pledge

User Story:

As a distressed student who lost my AirPods, I want to post a structured lost-item alert with the campus zone and an optional reward badge, so that finders across campus can easily identify my item and be motivated to return it.

Acceptance Criteria:

•
 The form requires Item Title, Category, Campus Zone, Date/Time, and Description.

•
 Users can optionally enter a reward pledge (e.g., "₦5,000" or "Appreciation Gift"), which displays as a badge on the listing.

•
 Upon submission, the system immediately surfaces any matching Found items in the same category and campus zone.


Story 3: Logging a Found Item with Hidden Verification

User Story:

As a campus finder who picked up a student ID card in a lecture hall, I want to attach a hidden verification question to my listing, so that I can verify the real owner without exposing sensitive card details publicly.

Acceptance Criteria:

•
 The Report Found Item form requires a hidden verification question before allowing submission.

•
 The verification question and expected detail are never visible on the public feed.

•
 Sensitive categories (such as ID cards) warn the finder against uploading unblurred photos.


Story 4: Claiming &amp; Safe Handover

User Story:

As an item owner, I want to answer the finder's hidden security question and confirm receipt using a 6-digit Handover PIN, so that I can prove ownership and close the ticket safely at a public campus location.

Acceptance Criteria:

•
 Claimants must submit an answer to the hidden question before the finder is notified.

•
 Contact details or in-app chat unlock only after the finder clicks Approve Claim.

•
 Entering the 6-digit Handover PIN updates the listing status to Returned and removes it from the active feed.


Story 5: WhatsApp Funnel Sharing

User Story:

As a student posting a lost or found item, I want to generate a clean WhatsApp share link, so that I can post it in hostel or departmental group chats and direct claimants back to Reclaim's verified process.

Acceptance Criteria:

•
 Every active listing includes a Share to WhatsApp button.

•
 The generated message summarizes the item title, campus zone, and a direct link to the Reclaim listing without exposing private contact details.


Story 6: Admin Moderation &amp; Archiving

User Story:

As a Campus Admin, I want to log items dropped off at the security desk and archive unresolved posts older than 30 days, so that students can see physically stored items and the feed remains accurate.

Acceptance Criteria:

•
 Admins can create "Drop-Off Desk" listings tagged with the physical pickup location.

•
 Admins can flag, remove, or ban accounts involved in fraudulent claims.

•
 Listings unresolved for 30 days are automatically moved to the archive.

### 3.4 User Autonomy & Privacy Controls

To maintain student trust and safety, Reclaim embeds user autonomy directly into the workflow:

- **Contact Privacy:** Finders and owners never have their phone numbers exposed publicly; communication unlocks only when a finder explicitly approves a claim.

- **Listing Control:** Users can edit details, update reward pledges, or delete/close their own posts at any time.

- **Voluntary Rewards:** Reward pledges in v1.0 are strictly optional and settled face-to-face at physical handover.

- **Safe Meetup Choice:** Users can decline or cancel a handover if anything feels unsafe and default to high-traffic campus zones (Library Front Desk, Student Affairs Office, or Campus Security Post).

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

## 6. Core User Flows

**Flow A: Reporting & Recovering a Lost Item**

 **1. Sign In:** Student logs into Reclaim with their verified school email.
 **2. Submit Report:** Selects Report Lost Item, enters category (AirPods), location (Sports Complex), description, and pledges an optional reward.

**3. Instant Match Check:** System checks existing Found posts and immediately surfaces any matching items in the same category and zone.

 **4. Submit Claim:** Student finds a matching listing, clicks Claim Item, and answers the finder's hidden security question.

**5. Approval & Meetup:** Finder approves the answer; both agree to meet at the Main Library entrance.

 **6. Verified Handover:** At handover, the owner inspects the item, hands over the reward, and shares their 6-digit PIN. The finder enters the PIN, updating the post status to Returned.

**Flow B: Logging a Found Item**

 **1. Item Discovery:** Finder picks up a student ID card in a lecture hall.

 **2. Quick Log:** Opens Reclaim, taps Report Found Item, selects ID Card and Lecture Hall A.

 **3. Set Security Challenge:** Sets a hidden verification question ("What is your matriculation number?") instead of posting a full photo of the card publicly.

**4. Verify & Return:** Receives a notification when the owner submits the correct answer, approves the claim, and completes handover.

## 7. Non-Functional Requirements

- **Security & Privacy:** All passwords hashed; HTTPS enforced; personal phone numbers and sensitive ID card details masked from public view. Uploaded photos stripped of EXIF GPS metadata.

- **Performance:** Feed and search results must load in under 2 seconds on standard campus 3G/4G mobile connections. Images automatically compressed on upload to save student data.

- **Usability (Mobile-First):** Fully responsive web design optimized for smartphones, allowing a student walking out of a lecture hall to post an item in 3 steps or fewer.

- **Reliability:** 99% uptime during active academic semesters, with automated daily database backups.

## 8. Out of Scope for Version 1.0 (MVP)

To ensure timely delivery for the academic project, the following features are deferred to future releases:

- **Native Mobile Apps:** Native iOS and Android applications (v1.0 will be a mobile-first web app).

- **Live Payment Escrow:** Automated in-app financial escrow and bank payouts (v1.0 uses reward pledges settled at physical handover to avoid financial compliance bottlenecks).

- **AI Visual Matching:** AI image recognition for automatic photo-to-photo matching.

- **Hardware Tracking:** Bluetooth/GPS hardware tracker integration.

## 9. Risks & Mitigations

| **Risk**                                                  | **Impact**                                        | **Mitigation Strategy**                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Fraudulent Claims**                                     | High — Items handed to thieves instead of owners. | Mandatory hidden verification question per found item; institutional account verification; ban policy for repeat offenders.                   |
| **Reward Disputes (Owner refuses to pay pledged reward)** | Medium — Erodes finder trust and motivation.      | Clearly label v1.0 rewards as "Voluntary Pledges" settled face-to-face at handover; track user reliability ratings; introduce escrow in v2.0. |
| **Low Initial Adoption ("Everyone still uses WhatsApp")** | High — Empty feed leads to abandonment.           | Built-in Share to WhatsApp button that posts a clean link to hostel/departmental chats, turning WhatsApp into a traffic funnel for Reclaim.   |
| **Exposure of Sensitive Data (ID Cards / Bank Cards)**    | High — Identity theft or privacy breach.          | Warn finders not to upload unblurred photos of ID numbers; default to text-only + hidden verification for ID/card categories.                 |

## 10. Suggested MVP Tech Stack & Rollout Plan

**Recommended Tech Stack**

- **Frontend:** React (or Next.js) with Tailwind CSS for a fast, mobile-first UI.

- **Backend & Database:** Firebase (Firestore + Authentication + Storage) or Supabase (PostgreSQL + Auth + Storage) for rapid development and real-time updates.

- **Deployment:** Vercel or Netlify (free tier suitable for campus MVP).
