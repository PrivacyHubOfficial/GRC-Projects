Exactly. Then **don't study GRC first**. Do a **3-day GRC bootcamp by doing the work**, and learn terminology only when you hit it.

Your goal after 3 days should be:

> **Given a company, I can identify risks, map requirements to controls, request/test evidence, identify gaps, document findings, assess vendors, and present the result to management.**

That's a much better target.

## The 3-day practical GRC sprint

### DAY 1 — Be the GRC analyst

**Scenario:** You have just joined a fictional fintech called **Northstar Payments**.

You are told:

> "We need to understand whether our security controls are adequate and prepare for an external audit."

You start with **no framework**.

#### Exercise 1 — Understand the business

Create a one-page company profile:

* What does the company do?
* What data does it hold?
* What systems does it use?
* Who are the important third parties?
* What could seriously hurt the business?

You'll naturally discover terms like:

**asset, threat, vulnerability, impact, risk, control, stakeholder.**

Don't memorize them beforehand.

---

#### Exercise 2 — Build a risk register

I'll give you situations such as:

> An employee leaves the company but their Microsoft 365 account remains active for four days.

You decide:

* What's the risk?
* What's the impact?
* How likely is it?
* What control should exist?
* Who owns it?
* What's the remediation?

Do **10–15 risks**.

By the end of this exercise, you will understand risk management better than someone who spent a day reading definitions.

---

#### Exercise 3 — Build your first control library

Take those risks and turn them into controls.

Example:

**Risk:** Former employees retain access.

**Control:** Employee access is disabled within 24 hours of termination.

Then specify:

* control owner
* frequency
* evidence
* control type
* testing method

Now you're doing actual GRC.

---

### DAY 2 — Audit the company

Now I'll give you **evidence**.

Not theory.

Things like:

> `employee_termination_report.xlsx`

> `Q2_access_review.pdf`

> `AWS_IAM_export.csv`

> `vendor_questionnaire.pdf`

> `incident_log.xlsx`

Your job is to determine:

**Pass / Fail / Partial / Not applicable**

And explain **why**.

This is where you learn the difference between:

> "The company says it does this"

and

> "I have sufficient evidence that the control operated effectively."

That distinction is huge.

---

### Then we'll deliberately give you bad evidence.

For example:

**Control:**

> Quarterly privileged-access review is performed.

**Evidence:**

A spreadsheet showing:

| User  | Role  | Reviewer |
| ----- | ----- | -------- |
| John  | Admin | Sarah    |
| Maria | Admin | Sarah    |

But there's:

* no review date
* no approval
* no evidence of remediation
* no indication that this is the complete population

You have to decide:

> **Is this sufficient evidence?**

This teaches you **control testing**.

---

### Exercise 2 — Write audit findings

You'll find problems.

You then write:

**Finding:** Privileged access review evidence is incomplete.

**Risk:** Unauthorized privileged access may remain undetected.

**Root cause:** No standardized evidence-retention procedure.

**Recommendation:** Establish a documented quarterly review process with population reconciliation and evidence retention.

**Owner:** IAM Manager

**Due date:** 30 days

**Severity:** Medium

Now you're doing **audit/compliance work**.

---

### Exercise 3 — Framework mapping

**Only now** do we introduce frameworks.

I'll take the controls you've already created and show you where they fit:

**NIST CSF 2.0**
**ISO 27001**
**SOC 2**
**DORA**

Instead of memorizing hundreds of requirements, you'll see:

> "Ah — this control maps to these requirements."

That's the right way to learn frameworks.

---

# DAY 3 — Become the GRC person management actually needs

Now we move beyond security controls.

### Exercise 1 — Third-party risk

I'll give you a vendor:

> Cloud analytics provider
> Processes customer information
> Hosted in AWS
> No SOC 2 report
> ISO 27001 certified
> Wants production API access

You perform a **vendor risk assessment**.

You'll determine:

* inherent risk
* data classification
* criticality
* security requirements
* due diligence
* contractual requirements
* residual risk
* approval/escalation

That's **Third-Party Risk Management (TPRM)**.

Very relevant to banks and large enterprises.

---

### Exercise 2 — Incident

I'll give you:

> "At 09:15 the SOC detects unusual activity from a privileged account."

You have to work through:

**Detection → triage → containment → investigation → notification → recovery → lessons learned**

You'll encounter:

* incident severity
* escalation
* incident owner
* business impact
* regulatory notification
* evidence preservation

Again, terminology comes **after the practical problem**.

---

### Exercise 3 — Business continuity

I'll tell you:

> "Your payment processing platform is unavailable for 8 hours."

You determine:

* critical business process
* maximum tolerable downtime
* RTO
* RPO
* dependencies
* recovery strategy
* alternate processes

Now you understand **BCP/DR** practically.

---

# Final exercise: the executive meeting

This is the part I'd really emphasize.

You have:

**42 controls tested**

* 31 passed
* 7 partially effective
* 4 failed

You have:

**12 risks**

* 2 critical
* 3 high
* 5 medium
* 2 low

You have:

**8 vendors**

* 2 high-risk
* 4 medium
* 2 low

Now you're the GRC analyst presenting to the CISO/CRO.

You need to answer:

> **"Are we compliant?"**

And here's where you learn one of the most important GRC lessons:

**You don't simply say yes/no.**

You say something like:

> "Based on the controls tested, we have several material gaps. The highest-risk issue is privileged-access management, where two controls were ineffective. We recommend remediation within 30 days. The remaining exceptions are within the organization's current risk tolerance, subject to management acceptance."

**That's GRC.**

---

# And Vanta?

On **Day 3**, I'd introduce Vanta.

Not before.

Because once you've manually done:

**Risk → Control → Evidence → Test → Finding → Remediation**

you'll immediately understand what Vanta is doing.

You'll look at Vanta and think:

> "Oh. It's automating evidence collection, control monitoring, questionnaires, workflows, and reporting around this process."

Exactly.

Then I'd show you **Drata, ServiceNow GRC and Archer** briefly so you understand how the tooling landscape differs.

---

## Your three-day deliverable

By the end, you should have your own mini **GRC case file**:

```text
Northstar Payments
│
├── Company Profile
├── Asset Register
├── Risk Register
├── Control Library
├── Framework Mapping
│   ├── ISO 27001
│   ├── NIST CSF
│   ├── SOC 2
│   └── DORA
├── Evidence Repository
├── Control Testing
├── Audit Findings
├── Remediation Tracker
├── Vendor Risk Assessment
├── Incident Assessment
├── BIA / BCP
└── Executive Risk Report
```

And importantly, **you'll be able to explain every item in an interview.**

Not:

> "I know ISO 27001."

But:

> "I can perform a risk assessment, establish controls, map those controls to ISO 27001/NIST/SOC 2 requirements, define evidence, test operating effectiveness, document deficiencies, assign remediation and report residual risk."

That's the level I'd aim for.

**If you want, we can start Day 1 right now.** I'll act as your **CISO/GRC manager**, give you the fictional company's information and the first real assignment, and you do the work. I won't teach you terminology until you encounter it.
