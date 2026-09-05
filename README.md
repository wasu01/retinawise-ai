# RetinaWise AI

Build a complete, polished, functional web application for Smart India Hackathon problem statement:

“SIH26038 — Explainable AI for Diabetic Retinopathy Screening in Rural India”

Problem Statement Owner: MathWorks.

IMPORTANT DEVELOPMENT CONSTRAINT:
I am using Lovable with a very limited credit budget. I want to build this entire application using a maximum of 5 Lovable credits total.

Therefore:

Treat this as a ONE-SHOT production-quality implementation.

Do NOT create unnecessary placeholder pages.

Do NOT over-engineer the project.

Do NOT add irrelevant SaaS features.

Do NOT require multiple clarification rounds.

Build as much as possible correctly in the first generation.

Use clean, reusable components.

Keep architecture simple enough that future edits can be made manually.

Make all major UI flows functional using realistic demo/mock data.

Prioritize the hackathon demonstration experience over enterprise backend complexity.

The result should look like a serious medical-AI product prototype that could be demonstrated live to Smart India Hackathon judges.

==================================================

PRODUCT NAME & BRANDING
==================================================

Create a strong healthcare technology product identity.

Product name:
“DrishtiAI”

Subtitle:
“Explainable Diabetic Retinopathy Screening for Rural India”

Tagline:
“Capture. Understand. Refer. Even Offline.”

Use a modern visual identity combining:

healthcare

AI

retinal imaging

rural accessibility

clinical trust

Do NOT make the interface look like a generic admin template.

Design inspiration:

premium healthcare SaaS

modern clinical dashboards

Apple-like cleanliness

subtle AI/data visualization aesthetic

minimal but sophisticated

Use:

lots of white/off-white space

dark navy text

subtle emerald/teal healthcare accents

restrained red/orange only for warnings and referral alerts

rounded cards

subtle shadows

high-quality typography

generous spacing

smooth transitions

clean icons

minimal gradients

The application must be fully responsive for:

desktop

tablet

mobile

Desktop should be the most polished because it will be used during the hackathon presentation.

==================================================
2. TARGET USERS

The application serves three main audiences.

Rural health worker / ASHA worker
Needs an extremely simple interface for:

capturing/uploading retinal image

checking image quality

seeing whether the patient needs referral

receiving simple-language instructions

Ophthalmologist
Needs:

ICDR grading

lesion information

Grad-CAM heatmap

lesion overlay

confidence score

reasoning/concordance score

review queue

ability to approve/correct AI result

Project judges / administrators
Need to understand:

workflow

novelty

offline architecture

explainable AI

clinical safety

system metrics

The UI should clearly reflect these different needs.

==================================================
3. MAIN APP STRUCTURE

Create a polished authenticated dashboard shell.

Desktop sidebar navigation:

Overview

New Screening

Screening Records

Review Queue

Offline Sync

Analytics

Model Insights

Settings

At the bottom of the sidebar show:

“AI System Status”

Model: Active

Offline Mode: Available

Last Sync: Recently

Top navbar:

current facility

connectivity indicator

language selector

notification icon

profile/avatar

Facility example:
“PHC Rampur”

Connectivity badge:
“Online”
or
“Offline Mode”

Allow the user to toggle simulated Online / Offline mode for demonstration purposes.

==================================================
4. LOGIN / LANDING EXPERIENCE

Create a polished landing/login page before the dashboard.

Hero title:

“AI-powered retinal screening that works where healthcare access is limited.”

Supporting copy:

“DrishtiAI helps frontline health workers detect diabetic retinopathy using explainable AI, on-device quality checks, uncertainty-aware referral logic and offline-first screening.”

Primary CTA:
“Start Screening”

Secondary CTA:
“View Clinical Dashboard”

Add an elegant retinal/fundus inspired visual or abstract retinal scanning graphic.

Below the hero show four capability cards:

“On-device Quality Gate”
“Explainable AI”
“Confidence-aware Referral”
“Offline-first Screening”

Also show:

“Built for SIH26038 • Problem Statement by MathWorks”

No need for a complex real authentication backend. A demo login is enough.

Demo accounts:

Health Worker

Ophthalmologist

==================================================
5. OVERVIEW DASHBOARD

Create a highly polished clinical overview.

Header:
“Good morning”
“Here’s today’s retinal screening activity.”

KPI cards:

Total Screenings
Example: 248

Referable DR
Example: 47

Pending Reviews
Example: 12

Retakes Prevented
Example: 31

Sync Pending
Example: 8

Average AI Confidence
Example: 91.4%

Add trend indicators.

Main dashboard should contain:

A. Screening Activity Chart
Line or bar chart showing daily screenings.

B. DR Grade Distribution
Donut/bar chart:

No DR

Mild

Moderate

Severe

Proliferative DR

C. Referral Status

Routine

Refer

Urgent

Human Review Required

D. Recent Screenings table
Columns:
Patient ID
Date
DR Grade
AI Confidence
Reasoning Confidence
Referral
Sync Status

E. Offline status card
Example:
“8 screenings waiting to sync”
button:
“View Offline Queue”

==================================================
6. NEW SCREENING — MOST IMPORTANT PAGE

This is the centerpiece of the demo.

Create a step-based screening workflow:

Step 1
Patient

Step 2
Capture

Step 3
Quality Check

Step 4
AI Analysis

Step 5
Explainability

Step 6
Referral & Report

Use a premium stepper/progress indicator at the top.

STEP 1 — PATIENT DETAILS

Fields:

Patient ID
Patient Name
Age
Gender
Village
Phone Number
Known Diabetes
Diabetes Duration
Last Eye Examination

Do not require all fields.

Include:
“Continue to Retinal Capture”

STEP 2 — RETINAL CAPTURE

Create a large retinal capture area.

Allow:

Upload image

Drag/drop image

Simulated camera capture

Show an elegant camera frame with:

circular retina guide

centering grid

eye-position hint

Buttons:
“Capture Image”
“Upload Fundus Image”

After image is selected show:

preview

“Run Quality Check”

Provide sample/demo retina images inside the UI if possible so the demo can be used without external files.

==================================================
7. QUALITY GATE

This is one of the MAIN DIFFERENTIATORS of the project.

Before classification, simulate an on-device retinal image quality gate.

Analyze/display four checks:

Blur

Exposure

Glare

Field of View / Centering

Show each check with:

icon

status

score

progress bar

Example good scan:

Blur
Passed
92%

Exposure
Passed
88%

Glare
Passed
95%

Field of View
Passed
90%

Overall:
“Image Quality: Good”

Use green success state.

Button:
“Continue to AI Analysis”

IMPORTANT:
Add a demo control such as:
“Simulate Poor Capture”

When activated, display:

“Image rejected”

Reason:
“Image is too blurry for reliable screening.”

Recommendation:
“Retake image and keep the camera stable.”

Button:
“Retake Image”

Also support messages such as:
“Move closer”
“Reduce glare”
“Center the retina”

This should visually demonstrate that the system rejects bad input BEFORE running the disease classifier.

==================================================
8. AI ANALYSIS PAGE

Show a brief animated analysis state:

“Analyzing retinal image…”

Substeps:

Preprocessing retinal image

Detecting retinal features

Estimating DR grade

Detecting lesions

Generating explanation

Calculating reasoning confidence

Then show result.

Example result:

ICDR Grade:
Moderate Diabetic Retinopathy

Referable DR:
Yes

AI Diagnosis Confidence:
93.2%

Referral Priority:
Specialist Review Recommended

Use a clear prominent diagnosis card.

Add probability distribution:

No DR — 2%
Mild — 4%
Moderate — 93%
Severe — 1%
Proliferative — 0%

==================================================
9. EXPLAINABILITY — MAJOR DIFFERENTIATOR

This needs to be visually impressive.

Create a retinal image viewer with tabs or toggle:

Original
Grad-CAM
Lesion Map
Combined

Original:
retinal image.

Grad-CAM:
show visual heatmap overlay highlighting suspicious retinal areas.

Lesion Map:
show colored lesion markers.

Legend:
Microaneurysms
Hemorrhages
Hard Exudates
Soft Exudates

Combined:
show Grad-CAM attention and lesion regions together.

Beside the image show:

“Why did the AI make this decision?”

Example:

“The model identified multiple small hemorrhagic and microaneurysm-like regions around the upper temporal retina. Their distribution is consistent with moderate diabetic retinopathy.”

==================================================
10. EXPLAINABILITY CONCORDANCE SCORE

This is the MOST IMPORTANT UNIQUE FEATURE.

Create a large card titled:

“Reasoning Confidence”

Subtitle:
“Does the AI focus on clinically meaningful lesion regions?”

Show a circular gauge:

87%

Label:
“Strong Alignment”

Display:

AI Classification Confidence
93%

Lesion-Attention Concordance
87%

Show explanation:

“The areas highlighted by Grad-CAM significantly overlap with detected retinal lesion regions.”

Add a small visualization:

AI Attention Mask
+
Detected Lesions
→
Overlap Score

Show metrics:
IoU: 0.74
Dice: 0.85

Add info tooltip:

“Reasoning confidence measures how strongly the AI’s attention overlaps with detected retinal lesion regions.”

IMPORTANT DEMO FEATURE:

Add:
“Simulate Low Concordance”

When enabled:

AI Confidence:
96%

Reasoning Confidence:
28%

Show warning:

“High diagnosis confidence but low reasoning alignment.”

Status:
“Human Review Required”

Explanation:

“The model is highly confident in its prediction, but its attention does not sufficiently overlap with clinically relevant lesion regions. This case has been deferred for ophthalmologist review.”

Make this visually striking.

This demonstrates the “right answer, wrong reason” / Clever Hans problem.

==================================================
11. CLINICAL REFERRAL LOGIC

Create automated referral output.

Possible statuses:

LOW RISK
Routine screening

REFER
Specialist consultation recommended

URGENT
Priority ophthalmology referral

DEFERRED
Human review required

Referral decision should visually reference:

DR grade

model confidence

image quality

reasoning confidence

disagreement / uncertainty

Example card:

“Refer to Ophthalmologist”

Reason:
Moderate DR detected
High lesion burden
AI confidence: 93%
Reasoning confidence: 87%

Recommended action:
“Schedule ophthalmology review within 3 months.”

For low-confidence cases:

“AI result withheld.”

“Human review required because confidence is below the safe reporting threshold.”

The system should NEVER appear to blindly trust the AI.

==================================================
12. DUAL-AUDIENCE REPORT

Create a report page/modal with two tabs:

“Clinical View”
“Patient / Health Worker View”

CLINICAL VIEW

Show:

Patient ID
Image quality
ICDR grade
Referable DR
AI confidence
Reasoning confidence
Detected lesions
Grad-CAM image
Lesion map
Referral recommendation

Button:
“Export Report”

The export can simply trigger a mock download/toast if actual PDF generation is unnecessary.

PATIENT / HEALTH WORKER VIEW

Very simple language.

Example:

“Eye screening result”

“Some changes related to diabetes were found in the retina.”

“An eye doctor should review this result.”

“Recommended: Eye specialist check-up within 3 months.”

Show visual icons instead of technical terminology.

Include language selector:

English
हिन्दी
मराठी
தமிழ்
తెలుగు
বাংলা

At minimum, dynamically demonstrate English + Hindi text.

Add:

“Listen to Result”

Button with speaker icon.

Speech playback can use browser speech synthesis if easy to implement.

==================================================
13. SCREENING RECORDS PAGE

Create searchable/filterable table.

Columns:

Patient ID
Age
Village
Date
DR Grade
AI Confidence
Reasoning Score
Referral Status
Sync Status
Reviewer

Filters:

Date
DR Grade
Referral Priority
Confidence
Sync Status

Search:
“Search patient ID or village”

Clicking a row opens a detailed screening record.

==================================================
14. OPHTHALMOLOGIST REVIEW QUEUE

Create a specialized review page.

Show cards/table of cases requiring human review.

Reasons:

Low AI confidence

Low reasoning concordance

Borderline image quality

Severe DR

Model disagreement

Each case should display:

Patient
Retinal thumbnail
AI Grade
Confidence
Reasoning Score
Reason for Flag
Priority

Click:
“Review Case”

Case Review screen:

Large retinal viewer

Tabs:
Original
Grad-CAM
Lesions
Combined

Side panel:
AI Grade
Confidence
Concordance
Detected lesions

Doctor controls:

Confirm AI Result

Change Grade:
No DR
Mild
Moderate
Severe
Proliferative

Referral:
Routine
Refer
Urgent

Notes field

Button:
“Submit Review”

After submission show:
“Correction saved for future model improvement.”

This represents the feedback/retraining loop.

==================================================
15. OFFLINE-FIRST EXPERIENCE

This must be clearly visible.

Create a top connectivity switch:
Online / Offline

When Offline:

show a persistent but non-intrusive badge:
“Offline Mode”

Text:
“Screenings are being stored securely on this device.”

Allow the complete screening workflow to still work using mock/local data.

When a screening is completed offline:

“Saved locally”
“Will sync automatically when connectivity returns.”

Create Offline Sync page.

Sections:

Connectivity
Offline

Queued Screenings
8

Last Successful Sync
2 hours ago

Storage
Healthy

List queued records:

Patient ID
Timestamp
Size
Status

Status:
Waiting to Sync

When user toggles Online:

show:
“Connection restored”

Button:
“Sync Now”

Animate/mock syncing:

Uploading 1/8
Uploading 2/8
...
Sync complete.

Then show:
“All records synced successfully.”

This will be an important live demo moment.

Use localStorage to maintain mock offline queue if convenient.

==================================================
16. ANALYTICS PAGE

Create a visually strong analytics dashboard.

Include:

Total Screenings
Referable DR Rate
Retake Rate
Human Deferral Rate
Average Confidence
Average Reasoning Confidence

Charts:

DR Grade Distribution

Referral Trends

Image Quality Failure Reasons

blur

glare

exposure

field of view

AI Confidence Distribution

Reasoning Confidence Distribution

Concordance vs Diagnosis Confidence scatter-style visualization if practical.

Add section:

“Safety Monitoring”

Flagged high-confidence / low-concordance cases:
7

Low-confidence deferred:
12

Poor-quality captures rejected:
31

==================================================
17. MODEL INSIGHTS PAGE

This page is designed partly for SIH judges.

Show a simple visual architecture:

Fundus Image
↓
Quality Gate
↓
Preprocessing
↓
Classification Model
↓
Grad-CAM
+
Lesion Detection
↓
Concordance Verification
↓
Confidence & Referral Logic
↓
Report

Add model information cards:

Classification Backbone
EfficientNet-B3/B4

Outputs
5-class ICDR + Referable DR

Explainability
Grad-CAM++

Lesion Detection
Lightweight U-Net

Primary Grading Metric
Quadratic Weighted Kappa

Edge Optimization
INT8 Quantization

Deployment
ONNX / MATLAB Coder compatible

Add a “Datasets” section:

APTOS 2019
EyePACS
IDRiD
Messidor-2

Show IDRiD as:
“Indian-population dataset used for lesion supervision and domain-matched fine-tuning.”

Add a section:

“Why this system is different”

Cards:

Quality Before Classification
“Poor captures are rejected before inference.”

Explainability as Verification
“Grad-CAM attention is checked against detected lesion regions.”

Uncertainty-aware Safety
“Unsafe or uncertain cases are deferred rather than auto-reported.”

Offline-first Deployment
“Designed for low-connectivity rural screening environments.”

Dual-audience Explanation
“Clinical detail for doctors. Simple language for frontline workers and patients.”

==================================================
18. DEMO MODE

Create a “Demo Mode” control somewhere prominent.

This is critical for a hackathon.

Provide four predefined demo scenarios:

Healthy Retina
Quality: Good
Grade: No DR
AI confidence: 97%
Reasoning score: 92%
Decision: Routine Screening

Moderate DR
Quality: Good
Grade: Moderate
Confidence: 93%
Reasoning score: 87%
Decision: Refer

Poor Image
Blur score: Failed
Decision:
Retake Image

The model must NOT classify this case.

Clever Hans / Low Concordance
Grade: Severe
AI confidence: 96%
Reasoning score: 28%
Decision:
Human Review Required

These scenarios should allow us to demonstrate the entire product without relying on a live AI backend.

==================================================
19. TECH STACK

Use Lovable’s normal modern stack.

Preferred:

React
TypeScript
Tailwind CSS
shadcn/ui
Lucide icons
Recharts if available

Use reusable components.

No unnecessary backend is required for the first version.

Use mock JSON data + localStorage where appropriate.

DO NOT require Supabase unless absolutely necessary.

Since this is a hackathon prototype, client-side state is enough for:

screening records

demo scenarios

offline queue

ophthalmologist review

language selection

connectivity simulation

The app should not show broken buttons.

Every primary CTA must perform some visible action.

==================================================
20. MICROINTERACTIONS & POLISH

Add subtle animations for:

page transitions

card hover

AI processing

progress stepper

quality checks

referral decision

offline sync

toast notifications

Do not use excessive animation.

Use skeleton/loading states where helpful.

Buttons should have:
hover
pressed
disabled
loading states.

Use professional empty states.

Use tooltips for medical/AI terminology.

==================================================
21. ACCESSIBILITY

Use:

high contrast text

readable font sizes

visible focus states

descriptive labels

large primary actions

accessible status colors with text/icon backup

The rural health-worker workflow should be particularly simple.

==================================================
22. IMPORTANT CLINICAL DISCLAIMER

Add a small disclaimer in appropriate areas:

“DrishtiAI is a screening and clinical decision-support prototype. It does not replace diagnosis by a qualified ophthalmologist.”

Avoid language suggesting the AI makes a final medical diagnosis independently.

==================================================
23. RESPONSIVENESS

Desktop:
full sidebar and analytical dashboards.

Tablet:
collapsible sidebar.

Mobile:
bottom navigation or drawer.

On mobile, prioritize:

New Screening
Records
Referral Result
Offline Queue

Retinal images and explainability viewers should remain usable.

==================================================
24. SAMPLE DATA

Populate the application with realistic synthetic Indian rural screening data.

Example villages:
Rampur
Shivpura
Devgaon
Nandgaon
Bhadra

Use anonymized IDs such as:

DR-2026-00142
DR-2026-00143

Do NOT use real patient personal data.

==================================================
25. MOST IMPORTANT UI HIERARCHY

The product should emphasize these features in this order:

Retinal image quality gate

DR classification

Grad-CAM explainability

Lesion detection

Reasoning / concordance score

Confidence-aware human deferral

Dual-audience explanation

Offline queue + sync

Ophthalmologist feedback loop

Do not bury the concordance feature.

It should feel like one of the main innovations.

==================================================
26. IMPLEMENTATION PRIORITY

If development complexity becomes too high, prioritize these pages first:

PRIORITY 1
New Screening workflow

PRIORITY 2
AI Result + Grad-CAM + lesion concordance view

PRIORITY 3
Referral / deferral logic

PRIORITY 4
Offline mode simulation

PRIORITY 5
Ophthalmologist Review Queue

PRIORITY 6
Dashboard + analytics

Do not sacrifice functionality of the main screening demo to build decorative secondary pages.

==================================================
27. ACCEPTANCE TEST — THE APP IS COMPLETE ONLY IF THIS FLOW WORKS

I should be able to:

Open the website.

Enter as Health Worker.

Start New Screening.

Enter patient details.

Upload/select a retinal image.

Run quality gate.

See blur/exposure/glare/FOV scores.

Simulate a failed-quality scan and get a retake instruction.

Run a successful scan.

See DR classification.

See AI confidence.

Open Grad-CAM.

Open lesion overlay.

See reasoning/concordance confidence.

Simulate high-confidence + low-concordance scenario.

See the system automatically defer it to human review.

See referral recommendation.

Switch between Clinical and Patient/Health Worker report.

Switch the simple report to Hindi.

Switch the app offline.

Complete a screening offline.

See it added to offline queue.

Re-enable connectivity.

Sync the queued screening.

Enter Ophthalmologist mode.

Open a flagged case.

Confirm or correct the AI result.

Save the review.

See a polished dashboard with realistic metrics.

==================================================
28. FINAL DESIGN DIRECTION

The final product should communicate:

“Clinical AI you can inspect, not just trust.”

It should feel:

credible

innovative

medically responsible

technically mature

suitable for rural India

polished enough for an SIH final presentation

Avoid:

generic gradient-heavy startup designs

giant meaningless hero sections

too many decorative elements

excessive glassmorphism

unnecessary pages

lorem ipsum

fake non-functional buttons

complex backend configuration

cluttered medical dashboards

Use realistic copy everywhere.

The interface must tell the story of the complete screening journey visually even to a judge seeing the product for the first time.

FINAL INSTRUCTION:
Generate the complete application now using the simplest maintainable implementation possible. Make intelligent assumptions rather than asking follow-up questions. Use realistic mock data and ensure all key demo interactions work immediately.

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/52235348-e33e-4496-8bde-ec992f2f2d13).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
