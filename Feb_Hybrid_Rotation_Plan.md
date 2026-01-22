# February 2026: Hybrid Founder Rotation Plan

**Objective:**  
Secure agency cash flow in Week 1 so you can *“buy”* a guilt-free week of deep SaaS work in Week 2.

---

## 🟢 Week 1: Agency “Cash Sprint” (Feb 2 – Feb 8)

**Role:** Service Provider  
**Focus:** Apex Web Solutions  

**Rule:**  
🚫 Zero new SaaS code  
⏱️ Only 30 mins/day for critical server checks

### Tasks
- [ ] **Monday:** Conduct “State of the Union” meetings with all active agency clients. Set expectations.
- [ ] **Tuesday:** Dedicate full day to the highest-priority client deliverable (the one blocking payment).
- [ ] **Wednesday:** Invoicing Day. Chase every cent owed. Ensure runway is clear for next week.
- [ ] **Thursday:** Clear the “Quick Fix” queue (small CSS tweaks, content updates, plugin updates).
- [ ] **Friday:** “Handover Preparation.” Send updates to clients so they don’t bother you next week.
- [ ] **Weekend:** Rest. Do **not** touch the laptop.

---

## 🔵 Week 2: SaaS “Build” Sprint (Feb 9 – Feb 15)

**Role:** CTO / Lead Dev  
**Focus:** Tender Track 360  

**Goal:**  
🚀 Ship Role-Based Access Control (RBAC)

**Rule:**  
📧 Agency Email Auto-responder:  
> *“I am in a scheduled development sprint. I will respond to non-emergencies on Feb 16.”*

### Tasks
- [ ] **Mon (Backend):**  
  Finalize logic in `src/lib/auth/permissions.ts`.  
  Ensure `hasPermission` checks work correctly for `admin` vs `member`.

- [ ] **Tue (Frontend):**  
  Update  
  `src/app/(dashboard)/dashboard/settings/profile/components/organization-info.tsx`  
  to display the user’s role badge correctly.

- [ ] **Wed (Integration):**  
  Wire up the **Invite Member** flow in  
  `src/components/shared/modals/invite-member-modal.tsx`  
  to assign the selected role in the DB.

- [ ] **Thu (Testing):**  
  Run the simulation test:  
  `src/server/__tests__/rbac-simulation.test.ts`  
  Fix failures if any.

- [ ] **Fri (Deployment):**  
  Push RBAC to production. Verify live data.

- [ ] **Sat/Sun:**  
  Optional *“Joy Bucket”* coding  
  (e.g. tweaking animations in `src/styles/animations.css`) if energized.

---

## 🔴 Week 3: Operations & Systems (Feb 16 – Feb 22)

**Role:** COO  
**Focus:** Removing Friction (*The “Suck” Bucket*)  

**Goal:**  
🧹 Stop doing manual tasks.

### Tasks
- [ ] **Mon (SaaS Onboarding):**  
  Review `docs/ONBOARDING_FLOW_REPORT.md`.  
  Pick the top 3 friction points.

- [ ] **Tue (SaaS Dev):**  
  Implement `progress-tracker.tsx` in the dashboard home to guide new users  
  (e.g. *Complete Profile*, *Upload First Tender*).

- [ ] **Wed (Agency Ops):**  
  Create/refine a **New Client Onboarding Form** to stop chasing content via WhatsApp/Email.

- [ ] **Thu (SaaS Docs):**  
  Update `docs/03-user-guide/user-roles.md` to reflect new RBAC features.

- [ ] **Fri (Cleanup):**  
  Run `scripts/fix-db-schema.ts` to ensure local dev is perfectly synced with prod.

---

## 🟡 Week 4: Growth & Strategy (Feb 23 – Feb 28)

**Role:** CMO / CEO  
**Focus:** Marketing & Sales  

**Goal:**  
🎯 Get **5 Beta Testers / Sales Conversations**

### Tasks
- [ ] **Mon (Content):**  
  Write one high-quality blog post for  
  `src/app/blog/page.tsx`  
  on *“Common Pitfalls in Tender Management”*.

- [ ] **Tue (Outreach):**  
  Cold DM 10 prospects on LinkedIn.  
  **Script:**  
  > “Building a tool to stop missing tender deadlines. Want a free admin account?”

- [ ] **Wed (Landing Page):**  
  Polish `src/components/home-page/HeroSection.tsx`.  
  Ensure the value prop is clear:  
  **“Never Miss a Tender Deadline.”**

- [ ] **Thu (Network):**  
  Post a *Building in Public* update on LinkedIn showcasing the new RBAC feature.

- [ ] **Fri (Review):**  
  Review `docs/dev-plan.md`.  
  Did you hit the goals? Plan March rotation.

- [ ] **Sat (Feb 28):**  
  🚫 **Mandatory Day Off**

---

## 🚨 Emergency Protocol (The 45-Second Rule)

If an agency crisis hits during **Week 2 (SaaS Week)**:

1. **Assess:** Is the site actually down?
   - **Yes:** Fix it immediately (*Suck Bucket*), then return to SaaS work.
   - **No:** (e.g. *“I don’t like this blue”*)  
     Reply:  
     > “Noted. I’ve added this to the queue for the week of Feb 16.”
