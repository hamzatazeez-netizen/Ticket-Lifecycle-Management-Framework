# GRC Exception & Risk-Remediation
Ticket Lifecycle Management Framework
A GRC portfolio project — Meridian Trust Financial (fictional Canadian fintech)
Prepared by Paul Azeez Tunde Hamzat
Cybersecurity GRC Analyst
July 2026
 Table of Contents
Table of Contents	1
1. Executive Summary	1
2. Purpose and Scope	1
3. Organizational Context	1
4. Ticket Lifecycle Overview	1
5. Roles and Responsibilities (RACI)	1
6. SLA and Escalation Model	1
7. Metrics and KPIs	1
8. Control Framework Mapping	1
9. Continuous Improvement	1
10. Appendix	1

 
1. Executive Summary
This framework documents how Meridian Trust Financial manages GRC exception tickets: policy exceptions, risk acceptances, standard deviations, and temporary waivers raised when a business or technical constraint prevents full conformance with an approved control. It defines a seven-stage lifecycle, assigns clear ownership at each stage, sets service level targets by residual risk, and maps the process to ISO/IEC 27001:2022 and NIST SP 800-53/800-161 requirements.
A companion workbook, GRC_Exception_Ticket_Tracker.xlsx, operationalizes this framework with a live ticket register, lookup lists, an SLA matrix, and a dashboard. Together, the two artifacts demonstrate an end-to-end exception management capability suitable for audit walkthroughs, control self-assessments, and third-party risk reviews.
2. Purpose and Scope
Purpose: to provide a consistent, auditable method for identifying, assessing, approving, remediating, and closing out any instance where an information security or risk control cannot be met as designed.
Scope: this framework applies to all business units, systems, and third parties within Meridian Trust Financial's information security management system (ISMS) boundary. It covers exceptions arising from technical constraints (e.g. legacy systems), business urgency (e.g. emergency changes), and third-party limitations (e.g. delayed vendor attestations). It does not cover routine change requests that fully conform to policy, which follow the standard change management process.
Out of scope: incident response tickets and standard access requests are tracked through separate processes and are only referenced here where they intersect with a risk exception (for example, a compensating control implemented in response to an incident).
3. Organizational Context
Meridian Trust Financial is a fictional mid-size Canadian fintech offering digital banking and payment services, used here purely to give the framework a realistic setting. It maintains an ISMS aligned to ISO/IEC 27001:2022 and reports risk posture to an executive Risk Committee. The GRC function sits within the second line of defense, reporting to the Chief Risk Officer (CRO), with the CISO owning technical security exceptions and the CRO owning broader enterprise and third-party risk exceptions.
4. Ticket Lifecycle Overview
Every exception ticket moves through seven stages. A ticket may loop back from Verification to Remediation Planning if a compensating control fails re-testing; this reopens the ticket rather than closing it.
Stage	What happens	Primary owner
1. Intake and logging	Ticket is raised in the register with a unique ID, requesting party, affected system, and supporting evidence attached.	Requestor / GRC Analyst
2. Risk triage	GRC analyst assesses inherent likelihood, impact, and urgency, and assigns a control domain and reference.	GRC Analyst
3. Approval / risk acceptance	Risk owner (or Risk Committee for Critical/High items) formally approves, approves with conditions, or rejects the exception.	Risk Owner / CRO / CISO
4. Remediation planning	A remediation owner is assigned, a plan and target closure date are documented, and compensating controls are confirmed.	Remediation Owner
5. Implementation	Compensating controls and/or the permanent fix are put in place. Progress is tracked against the target date.	Remediation Owner
6. Verification and testing	GRC or internal audit confirms the control is now operating effectively, or that compensating controls remain adequate.	GRC Analyst / Internal Audit
7. Closure and review	Ticket is closed with evidence archived. A next review date is set for periodic re-certification of any residual risk accepted.	GRC Analyst / Risk Owner

5. Roles and Responsibilities (RACI)
Activity	Requestor	GRC Analyst	Risk Owner	CISO / CRO	Risk Committee
Raise ticket	R	A	I	I	-
Risk triage	C	R/A	I	I	-
Approve exception	I	C	A	A (High/Critical)	A (escalations)
Define remediation plan	C	C	A	I	-
Implement remediation	R	I	A	I	-
Verify and test	I	R/A	C	I	-
Close and archive evidence	I	R/A	C	I	-
R = Responsible, A = Accountable, C = Consulted, I = Informed.
6. SLA and Escalation Model
Turnaround targets and re-certification frequency scale with residual risk rating, so that higher-risk exceptions receive the closest attention and the most frequent revalidation.
Residual risk	SLA target (days to closure)	Review frequency	Escalation trigger
Critical	15	Every 90 days	No remediation owner assigned within 2 business days
High	30	Every 180 days	50% of SLA elapsed with no remediation plan on file
Medium	60	Annually	SLA breached by more than 10 days
Low	90	Annually	SLA breached by more than 20 days

Critical and High-rated exceptions require Risk Committee visibility; the GRC Analyst escalates automatically once a ticket's SLA status turns Overdue in the tracker.
7. Metrics and KPIs
•	Open exception count by residual risk rating, tracked monthly to show whether the overall exception book is growing or shrinking.
•	SLA adherence rate: percentage of tickets closed within their target window, segmented by risk rating.
•	Average days open and longest open ticket, to surface aging exceptions before they become audit findings.
•	Reopen rate: proportion of tickets that fail verification and cycle back to remediation planning, an early signal of weak compensating controls.
•	Exceptions by control domain, to identify systemic gaps (for example, repeated third-party attestation delays) that may warrant a policy or vendor-management fix rather than repeated one-off exceptions.
•	Upcoming re-certifications due in the next 30/60/90 days, so accepted risks are periodically revalidated rather than accepted indefinitely.
8. Control Framework Mapping
Framework	Reference	How this framework addresses it
ISO/IEC 27001:2022	Clause 6.1.3, Annex A.5.36	Formal risk treatment and compliance review process for deviations from the Statement of Applicability.
ISO/IEC 27001:2022	Annex A.8.9	Configuration and change exceptions logged, approved, and time-bound.
NIST SP 800-53 Rev. 5	CA-5 (POA&M)	Ticket register functions as a plan of action and milestones for each open control gap.
NIST SP 800-53 Rev. 5	PM-4	Centralized tracking and management of the organization-wide POA&M process.
NIST SP 800-161	SR-2, SR-6	Structured handling of supply chain and third-party risk exceptions with defined interim controls.
NIST RMF	Step 6: Monitor	Periodic re-certification of accepted risk supports continuous authorization monitoring.
9. Continuous Improvement
The GRC function reviews exception trends quarterly with the Risk Committee. Recurring exceptions in the same control domain (for example, repeated vendor attestation delays) trigger a root-cause review to determine whether the underlying policy, vendor selection criteria, or technical standard should change, rather than continuing to accept the same risk on a rolling basis.
10. Appendix
Companion artifact: GRC_Exception_Ticket_Tracker.xlsx, containing the Ticket Register, Lookup Lists, SLA Matrix, and Dashboard tabs referenced throughout this document.
Ticket ID convention: RXT-YYYY-NNN (RXT = risk exception ticket, YYYY = year raised, NNN = sequential number).
This document and its companion workbook were produced as a demonstration portfolio project and reference a fictional organization; they are intended to illustrate GRC process design and documentation capability.
