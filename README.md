# DIKWP OphthaCareRehab OS

DIKWP OphthaCareRehab OS is an offline-first, GitHub-ready ophthalmology treatment-preparation and visual rehabilitation governance system. It helps ophthalmology departments organize eye disease evidence, AI screening results, follow-up risk, rehabilitation needs, clinician review tickets, and patient education drafts.

This system is not a diagnostic device, not a treatment device, not a prescribing system, and not a substitute for an ophthalmologist, optometrist, low-vision specialist, rehabilitation therapist, emergency service, regulator, or approved medical AI device.

## Quick Start

```bash
pip install -e .
ophthacare analyze examples/sample_ophthalmology_care_case.json --out outputs/demo
ophthacare guard "generate patient education draft for low vision rehabilitation" 
ophthacare static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Open `index.html` for the standalone demo.

## Core Outputs

- `ophthacare_report.json`
- `dikwp_eye_care_ledger.json`
- `disease_pathway_matrix.csv`
- `treatment_review_tickets.csv`
- `rehabilitation_plan.md`
- `low_vision_support_plan.md`
- `ai_screening_review_queue.csv`
- `patient_education_pack.md`
- `clinician_review_board.md`
- `followup_safety_plan.md`

## Boundary

Allowed: education, evidence organization, red flag escalation, treatment preparation, rehabilitation planning drafts, patient education drafts, local quality review.

Blocked: autonomous diagnosis, autonomous treatment recommendation, prescribing, injection scheduling, laser/surgery approval, device control, emergency triage replacement, clinical decision automation, patient-specific directives without clinician review.
