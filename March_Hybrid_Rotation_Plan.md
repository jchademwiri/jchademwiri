# March 2026: Hybrid Founder Rotation Plan

**Objective:**  
Shift from **“Utility” (User Management)** to **“Value” (AI Features)**, while further automating the agency side.

---

## 🟢 Week 1: Agency “Cash Sprint” (Mar 2 – Mar 8)

**Role:** Service Provider  
**Focus:** Apex Web Solutions  
**Goal:** Clear Q1 deliverables and secure cash for Q2 taxes/expenses 💰

### Tasks
- [ ] **Monday:** Review all Q1 active contracts. Identify any *scope creep* and invoice for it or shut it down.
- [ ] **Tuesday:** **Deep Clean Day.** Update all client plugins, server PHP versions, and SSL certs to prevent future support tickets.
- [ ] **Wednesday:** Sales calls. Reach out to 3 past clients for **Maintenance Retainers**  
  *(Recurring agency revenue = Stability for SaaS)*.
- [ ] **Thursday:** Clear the agency backlog. Zero inbox for client requests.
- [ ] **Friday:** Finalize agency financials for Q1. Send all invoices.
- [ ] **Weekend:** Rest. Prepare mentally for AI-heavy lifting next week.

---

## 🔵 Week 2: SaaS “Build” Sprint (Mar 9 – Mar 15)

**Role:** CTO / AI Engineer  
**Focus:** Tender Track 360  
**Goal:** 🚀 Ship **AI Document Extraction (Phase 1)**  

**Context:**  
Use specs from `docs/07-ai-implementation/document-extraction.md`

**Rule:**  
📧 Agency email auto-responder **active**

### Tasks
- [ ] **Mon (Setup):**  
  Configure the Cloudflare R2 storage bucket for secure document uploads  
  *(see `docs/specs/r2-storage-implementation.md`)*.

- [ ] **Tue (Backend):**  
  Implement API route  
  `src/app/api/ai/extract/route.ts`  
  to handle PDF text extraction.

- [ ] **Wed (AI Logic):**  
  Connect the text extractor to the LLM service (OpenAI/Anthropic) to identify  
  **Submission Deadline** and **Budget** from uploaded tender PDFs.

- [ ] **Thu (UI):**  
  Update `src/components/tenders/tender-form.tsx` to allow  
  **“Auto-fill from PDF”**.

- [ ] **Fri (Integration):**  
  Test the full flow:  
  **Upload PDF → AI Scans → Form Auto-fills**.

- [ ] **Sat/Sun (Optional):**  
  Tune AI prompts using `docs/better-auth/llms.txt` to improve accuracy.

---

## 🔴 Week 3: Operations & Systems (Mar 16 – Mar 22)

**Role:** COO  
**Focus:** Reducing Support Tickets (*The “Suck” Bucket*)  
**Goal:** Enable **Self-Serve Organization Settings**

**Context:**  
Implement `docs/specs/settings-enhancement-phase-1.md`

### Tasks
- [ ] **Mon (Audit):**  
  Review Feb support emails. Count how many were *“Change my logo”* or *“Update my address”*.

- [ ] **Tue (Dev):**  
  Enhance  
  `src/app/(dashboard)/dashboard/organization/[slug]/components/settings-tab.tsx`  
  to support updating **Org Name, Slug, and Logo** without DB scripts.

- [ ] **Wed (Docs):**  
  Update the Help page  
  `src/app/help/page.tsx`  
  with FAQs about **Teams** and **AI features**.

- [ ] **Thu (Agency Ops):**  
  Automate **Maintenance Report** emails for agency clients (script or tool).

- [ ] **Fri (Cleanup):**  
  Refactor `src/components/ui`. Delete unused components to keep the repo clean.

---

## 🟡 Week 4: Growth & Strategy (Mar 23 – Mar 29)

**Role:** CMO / CEO  
**Focus:** Marketing the **Teams** Feature  
**Goal:** Leverage February’s RBAC work to land larger accounts

### Tasks
- [ ] **Mon (Outreach):**  
  Filter users/waitlist for corporate domains (exclude `gmail.com`).  
  Email them:  
  > *“We just launched Team Accounts.”*

- [ ] **Tue (Content):**  
  Record a 2-minute Loom demo of **Auto-fill from PDF** (beta is fine).  
  Post on LinkedIn.

- [ ] **Wed (Sales):**  
  Follow up with the 10 prospects from February. Ask for feedback.

- [ ] **Thu (Strategy):**  
  Plan the Q2 roadmap. Review `docs/FEATURE_ROADMAP.md`.  
  Decide if **Compliance Checker** is next.

- [ ] **Fri (Review):**  
  Quarterly review. Compare **Q1 Agency Revenue vs SaaS Revenue**.  
  Adjust April buckets if needed.

- [ ] **Sat (Mar 28):**  
  🚫 **Mandatory Day Off**

---

## 🚨 Emergency Protocol (March Edition)

### Scenario 1: Client site hacked/down during AI Week
**Response:**  
Fix it immediately. **Security is the only exception.**

### Scenario 2: Client requests a new project quote during AI Week
**Response:**  
> *“I’d love to discuss this. I have booking slots open starting March 16th.”*  

👉 Push it to **Ops Week** or **Growth Week**.
