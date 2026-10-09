# gatesync-casestudy
A data-driven workflow framework designed to eliminate hidden apartment gate delays, protect delivery rider safety, and provide realistic ETAs for platforms like Blinkit and Zepto.
# 🛵 GateSync: "10 Minutes" at the Society Gate

> **Candidate:** G Srikar (Roll: 26241A05M0 | Branch: CSE-H)
> **Institution:** Advanced Academic Center - GRIET
> **Live Demo:** [👉 View Live Project Website](https://vercel.app) *(Replace with your actual Vercel URL)*

---

## 📌 1. Problem Statement & Context
Quick-commerce platforms (like Blinkit and Zepto) historically promised **10-minute deliveries**, counting primarily the road transit time. However, hidden steps—such as order packing, security gate entry, taking elevators, and navigating corridors—significantly eat up the time window. 

Following gig-worker strikes on **31 December 2025** and subsequent Labour Ministry interventions, platforms dropped the "10-minute" marketing claim. However, removing the tagline does not eliminate the physical delay. 

**The GateSync Solution:** This project treats the housing society not as an external obstacle, but as an official, integrated milestone in the delivery chain. It measures transit times granularly to show customers realistic ETAs without placing unfair, unsafe speed pressures on delivery partners.

---

## 🛠️ 2. Core Architecture & Logic (How it Works)

GateSync calculates delivery time using **four distinct, measured stages** instead of a single arbitrary countdown:

$$\text{Total Time} = \text{Packing} + \text{Road Transit} + \text{Gate Processing} + \text{Building Lift/Walk} + \text{Buffer}$$

### The 6 Pillars of GateSync:
1. **Realistic ETAs:** Gate and lift times are dynamically calculated based on historical median delivery data specific to that society.
2. **Society Integration:** Connects the residential gate management app (or a lightweight QR web terminal) directly to the delivery platform. Residents select predefined drop points (*Door, Lobby Shelf, or Gate Counter*).
3. **One-Time Digital Passes:** Instant QR/OTP passes are generated per order. Security guards simply scan the code, bypassing manual phone calls to residents.
4. **Geofenced Early Alerts:** A virtual geofence boundary (**300 meters**) triggers automated entry preparation notices to both guards and residents.
5. **Fair Timer Rules:** Digital scan timestamps verify building-side delays. If delayed at the gate or lift, the rider's active countdown timer pauses.
6. **Transparency Scorecards:** Customers track live stage-by-stage progress, while housing societies receive efficiency scorecards to encourage faster gate clearance.

---

## 📊 3. Core System Workflow
The app lifecycle manages exceptions like stock shortages and invalid passes seamlessly:

