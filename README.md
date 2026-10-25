# PROG101_Assignment1_Nyuma_Sumaila_905006571; Child Fever Referral and Follow-up System
## Project overview
This project presents a logical design for helping community health workers (CHWs) record fever reports in children under five, communicate referral guidance based on locally approved danger-sign screening, and follow up on whether a child reached a trained health provider.
The design responds to malaria’s high health burden in Sierra Leone, especially for young children. It is an academic programming-logic assignment: it describes how a referral-tracking system could work, but it is not a deployed application or a clinical decision tool.
## Problem addressed
Distance to health facilities, limited communication, and incomplete records can make it harder to coordinate referrals and confirm follow-up. This design gives CHWs a consistent sequence for recording a report, directing urgent cases, tracking referral completion, and preparing community summaries.
## Proposed workflow
1. Enter the child’s age.
2. If the child is under five, enter the danger-sign response from a locally approved checklist.
3. Display an immediate-referral message when a danger sign is present, or a prompt-assessment message when none is reported.
4. Record a non-identifying case ID, community, and report time. These details are captured once after the referral message and linked to the case ID.
5. During follow-up, enter the case ID and whether care was reached. Set the case status to `PENDING` or `CLOSED`.
6. For weekly reporting, enter the community, reporting period, total fever reports, urgent referrals, and completed referrals. Display the aggregated summary.
The case ID connects follow-up to the original intake record, so community and report time do not need to be entered again during follow-up.
## Logical design
The assignment demonstrates:
- **Input and output:** collect age, danger-sign response, case ID, community, report time, referral status, reporting period, and summary totals.
- **Data types:** integers for age and counts, Boolean values for danger signs and referral completion, and strings for case ID, community, time, status, and reporting period.
- **Selection:** route cases based on age, danger-sign response, and whether care was reached.
- **Repetition:** review multiple pending cases and produce summaries for reporting periods.
- **Modular design:** separate intake, danger-sign screening, referral tracking, follow-up, and summary reporting.
## Flowcharts
The report contains three Flowgorithm-style flowcharts. Each begins with `Main` and ends with `End`.
1. **Child fever intake and referral:** checks age and danger signs, displays a referral message, then records case ID, community, and report time.
2. **Referral outcome and follow-up:** uses the case ID and a `True`/`False` care-reached response to set `PENDING` or `CLOSED`.
3. **Weekly referral summary:** collects community, reporting period, and aggregate counts, then displays the summary.
The diagrams are visual logical designs embedded in the report. They are not executable source-code files. To create editable Flowgorithm programs for a repository, recreate each chart in Flowgorithm and save its `.fprg` file.
## Safety, privacy, and scope
- The system does **not** diagnose malaria, interpret test results, prescribe medicines, or replace clinical judgment.
- Trained health providers remain responsible for assessment, testing, and treatment under current Sierra Leone guidance.
- Danger-sign questions, referral instructions, destinations, and follow-up timelines require approval from local health authorities before real use.
- Record only information needed for referral and follow-up. Restrict identifiable case details to authorized workers and use aggregated counts for routine summaries.
- The design can be used with paper records or adapted for offline entry where connectivity or electricity is unreliable.
- Urgent referral must not be delayed to complete nonessential data entry.
## Sustainable Development Goals
The project supports **SDG 3: Good Health and Well-being**, particularly Target 3.2 on preventable deaths among children under five and Target 3.3 on combating malaria. It is an information and coordination design; it cannot ensure transport, facility capacity, or clinical treatment.
## Open source and Digital Public Goods
The design could be published under an approved open-source licence so students and local developers can inspect and adapt its nonclinical workflow. Any clinical content must be reviewed by qualified local health authorities.
This project is **not represented as a formally recognized Digital Public Good**. Formal recognition requires review against the Digital Public Goods Standard, including requirements related to open licensing, documentation, privacy, and security.
