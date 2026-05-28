---
copyright: "Copyright © 2026 Sungrow Power Supply Co., Ltd."
license: "Client Work Product - Subject to MSA"
---

# Project Status

**Last Updated**: 2026-05-28
**Updated By**: ENGINEERING_PRINCIPAL
**Overall Status**: 🟢 ON TRACK

---

## Project Overview

**Project**: Aegis Firmware Governance Platform
**Type**: Brownfield (AIRE Build)
**Start Date**: 2026-03-31 (Discovery kickoff)
**Target Completion**: 2027-03-01 (17-cycle roadmap)
**Active Cycle**: CYCLE-2
**Current Step**: Cycle 2 Build Workshops — Epics 1–3 closing, Epic 4 (SR Dashboard) code-merged pending review, Epic 5 (Audit Export) not yet started

> **Compliance milestone**: ISO 27001 / SOC 2 close-out target 2026-06-30 (BC-2 closes 2026-06-07 with a 23-day cushion if on schedule).

---

## Progress Summary

**Overall Completion**: 74% (78/106 stories complete across planned cycles BC-0 → BC-2)

| Step | Status | Owner | Updated | Evidence |
|------|--------|-------|---------|----------|
| Discovery | ✅ Done | AIRE_DISCOVERY_ANALYST | 2026-05-01 | `docs/requirements.md`, `discovery/baseline/functional-scope.md` |
| System Discovery | ✅ Done | AIRE_ANALYST_PM_BROWNFIELD | 2026-05-22 | `context-project/architecture/current/00-system-overview.md` |
| Deep-Dive | ✅ Done | AIRE_ANALYST_PM_BROWNFIELD | 2026-05-22 | `context-project/architecture/current/01-intake-pipeline-deep-dive.md` |
| Build Cycles | ✅ Done | AIRE_BUILD_CYCLE_PLANNER | 2026-05-22 | `build-cycles/cycle-1/cycle-plan.md`, `build-cycles/cycle-2/cycle-plan.md` |
| Implementation Plan | ✅ Done | AIRE_ARCHITECT | 2026-05-22 | `build-cycles/cycle-2/implementation-plan.md` |
| Cycle 0 — Walking Skeleton | ✅ Done | AIRE_DEV | 2026-05-04 | 27/27 stories complete (see Build Cycles table) |
| Cycle 1 — Flow 1A Intake + i18n | ✅ Done | AIRE_DEV | 2026-05-22 | 37/38 stories complete (Story 6.4 deferred to Tester role) |
| Epic 1: SR Quality Gate Decision Surface (CYCLE-2) | 🟡 In Progress | AIRE_DEV | 2026-05-28 | 6/10 stories done (1.10 deferred to BC-3) |
| Epic 2: Waiver Lifecycle (CYCLE-2) | 🟡 In Progress | AIRE_DEV | 2026-05-28 | 4/5 stories done (2.2 deferred to BC-3) |
| Epic 3: Component-Level Review (CYCLE-2) | 🟡 In Progress | AIRE_DEV | 2026-05-28 | 1/6 stories done (3.4, 3.7 deferred to BC-3) |
| Epic 4: SR Triage Dashboard + Notifications (CYCLE-2) | 🟡 In Progress | AIRE_DEV | 2026-05-28 | 3/10 stories done (4.1, 4.2, 4.3) |
| Epic 5: Compliance Audit Export (CYCLE-2) | ⏸️ Not Started | — | — | 0/10 stories |
| Review | 🟡 In Progress | AIRE_REVIEWER | 2026-05-28 | Per-story reviews under `build-cycles/cycle-*/wrap-up/*-review.md` |
| QA | 🟡 In Progress | AIRE_QA | 2026-05-28 | Per-story QA via PR pipeline; cycle-final E2E deferred to Tester role |

---

## Current Step Details

### Cycle 2 — Flow 1B Quality Gate (Security Reviewer)

**Owner**: AIRE_DEV
**Status**: 🟡 In Progress
**Started**: 2026-05-18
**Window**: 2026-05-18 → 2026-06-07
**Compliance milestone**: ISO 27001 / SOC 2 close-out by 2026-06-30

**Progress**:

- [x] Epic 1.1–1.4, 1.7, 1.11 — IntakeRequest schema, recordGateDecision lambda + SR panel, SR attestation download, HQ attestation read-only row, release-classification + TPSA conditional, TPSA state control ✅
- [x] Epic 2.1, 2.3, 2.4, 2.5 — createWaiver + FC-3 regression, waiver lifecycle auto-clear, HQ view of waived artifact, authorization regression ✅
- [x] Epic 3.1 — ComponentAudit entity schema ✅
- [x] BUG-058 — write `currentLifecycleState` on SR gate decision ✅
- [x] Epic 4.1, 4.2, 4.3 — SR dashboard page + 4 KPI cards, Needs-Action-Now list, product-line filter chip ✅
- [ ] Epic 1.5, 1.6, 1.8, 1.9 — per-binary upload + pass/fail gate, pipeline routing, record-lineage 2FK display 🔄
- [ ] Epic 2.6 — site-cascade waiver (D18) 🔄
- [ ] Epic 3.2, 3.3, 3.5, 3.6, 3.8 — rejectComponent, per-component re-upload, ReviewRecord container, roll-up comments, BundleUpdateEvent enum
- [ ] Epic 4.4–4.10 — Activity inbox, email notifications, attestation format finalization
- [ ] Epic 5.1–5.10 — Audit export pipeline (compliance-critical)
- [ ] Deferred to BC-3 (per PR #480, #424): Stories 1.10, 2.2, 3.4, 3.7

---

## Build Cycles

| Cycle | BUILDID | Scope | Stories | Status | Start | End |
|-------|---------|-------|---------|--------|-------|-----|
| Cycle 0 | CYCLE-0 | Walking Skeleton (Flows 0–4 vertical slice) | 27/27 | ✅ Done | 2026-04-22 | 2026-05-04 |
| Cycle 1 | CYCLE-1 | Flow 1A — HQ Engineer Firmware Intake + i18n foundation | 37/38 | ✅ Done | 2026-05-05 | 2026-05-22 |
| Cycle 2 | CYCLE-2 | Flow 1B — Security Reviewer Quality Gate + Audit Export (ISO/SOC 2 milestone) | 14/41 | 🟡 In Progress | 2026-05-18 | — |
| Cycle 3 | CYCLE-3 | TBD — carry-forward of BC-2 deferrals + rework team integration | 0/0 | ⏸️ Not Started | — | — |
| Cycles 4–17 | — | Directional only; per-cycle plans authored at each Planning activity | — | ⏸️ Not Started | — | — |

> Cycle 1 deferred Story 6.4 (Cycle-Final Playwright E2E) to a dedicated Tester role per the "no test data in production" decision (2026-05-08). Cycle 2 deferred Stories 1.10, 2.2, 3.4, 3.7 to BC-3 per PR #480 / PR #424 (PDM UX scope correction).

---

## Story Tracker

### CYCLE-0 — Walking Skeleton

| BUILDID | Story | Title | Start | End |
|---------|-------|-------|-------|-----|
| CYCLE-0 | 1.1 | Scaffold SPA Tooling | 2026-04-22 | 2026-04-22 |
| CYCLE-0 | 1.2 | Amplify Gen-2 Backend Wiring | 2026-04-22 | 2026-04-22 |
| CYCLE-0 | 1.3 | SPA App Shell + Auth | 2026-04-22 | 2026-04-22 |
| CYCLE-0 | 1.4 | Data Access Foundation | 2026-04-22 | 2026-04-26 |
| CYCLE-0 | 1.5 | CI + Authorization Matrix Harness | 2026-04-26 | 2026-04-27 |
| CYCLE-0 | 2.1 | Core Entity Data Models | 2026-04-26 | 2026-04-27 |
| CYCLE-0 | 2.2 | Audit Pipeline | 2026-04-26 | 2026-04-27 |
| CYCLE-0 | 2.3 | Admin CRUD UI | 2026-04-26 | 2026-04-27 |
| CYCLE-0 | 2.4 | Flow 0 E2E + Authz Matrix | 2026-04-26 | 2026-04-27 |
| CYCLE-0 | 3.1 | Artifact Bundle + Waiver + Quality Gate Models | 2026-04-27 | 2026-04-29 |
| CYCLE-0 | 3.2 | Upload Pipeline | 2026-04-27 | 2026-04-29 |
| CYCLE-0 | 3.3 | HQ Upload UI | 2026-04-27 | 2026-04-29 |
| CYCLE-0 | 3.4 | SR Intake Review UI | 2026-04-27 | 2026-04-29 |
| CYCLE-0 | 3.5 | Flow 1 E2E + Object Lock | 2026-04-27 | 2026-04-29 |
| CYCLE-0 | 4.1 | FirmwareRequest + DownloadNonce + DeploymentRecord + Notification Models | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 4.2 | Approve + Redeem Lambdas | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 4.3 | ST Request + Download UI | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 4.4 | SR Request Queue + ST Deployment Confirmation | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 4.5 | Flow 2 E2E + MFA Abuse | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 5.1 | Dashboard Action Item Inbox | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 5.2 | Site Inventory + Firmware Tab | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 5.3 | Devices Tab + Read-Only Detail | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 5.4 | Cross-Site Impact + Audit Export | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 5.5 | Flow 3 + Flow 4 E2E | 2026-04-29 | 2026-04-29 |
| CYCLE-0 | 6.1 | Seed Demo Data Script | 2026-05-03 | 2026-05-03 |
| CYCLE-0 | 6.2 | Demo Runbook + Dry Run | — | 2026-05-04 |
| CYCLE-0 | 6.3 | Final QA + Sign-Off Packet | — | 2026-05-04 |

### CYCLE-1 — Flow 1A Intake + i18n

| BUILDID | Story | Title | Start | End |
|---------|-------|-------|-------|-----|
| CYCLE-1 | 1.1 | Verify BC-0 Baseline State | 2026-05-04 | 2026-05-04 |
| CYCLE-1 | 1.2 | Apply Intake Pipeline Recommended Change | 2026-05-04 | 2026-05-04 |
| CYCLE-1 | 1.3 | Re-baseline CI + Authorization Matrix | 2026-05-04 | 2026-05-04 |
| CYCLE-1 | 2.1 | Catalog Data Model + AppSync Schema | 2026-05-05 | 2026-05-05 |
| CYCLE-1 | 2.2 | Catalog CRUD Lambdas | 2026-05-05 | 2026-05-05 |
| CYCLE-1 | 2.3 | Board Component Manifest Model | 2026-05-05 | 2026-05-05 |
| CYCLE-1 | 2.4 | Catalog Admin UI | 2026-05-05 | 2026-05-05 |
| CYCLE-1 | 3.1 | IntakeRequest Data Model + State Machine | 2026-05-06 | 2026-05-06 |
| CYCLE-1 | 3.2 | createIntakeRequest Lambda | 2026-05-06 | 2026-05-06 |
| CYCLE-1 | 3.3 | Draft Save + SR-Invisibility | 2026-05-06 | 2026-05-06 |
| CYCLE-1 | 3.4 | Three-Path Firmware-Type Form UI | 2026-05-06 | 2026-05-06 |
| CYCLE-1 | 3.5 | Per-Binary Mapping UI + Zip-Bundle Ingestion | 2026-05-06 | 2026-05-06 |
| CYCLE-1 | 4.1 | requestUploadUrl Lambda + Object Lock COMPLIANCE | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 4.2 | Dual Filename Audit + Normalized Display Name | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 4.3 | Artifact Slot Model | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 4.4 | Multi-Binary Upload UI With Progress | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 4.5 | UTF-8 / Chinese Filename Round-Trip | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 4.6 | Surface Consolidation | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 5.1 | Bundle Completeness Engine | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 5.2 | In-Review State Transition Gate | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 5.3 | FC-11 Two-Line Defense At AppSync | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 5.4 | Completeness UI + Submit Gate | 2026-05-07 | 2026-05-07 |
| CYCLE-1 | 6.1 | Locale Infrastructure + CJK Font Loader | 2026-05-08 | 2026-05-08 |
| CYCLE-1 | 6.2 | Locale Switch UI + Persistence | 2026-05-08 | 2026-05-08 |
| CYCLE-1 | 6.3 | Flow 1A Translations (zh-CN) | 2026-05-08 | 2026-05-08 |
| CYCLE-1 | 6.4 | Cycle-Final Playwright E2E | — | Deferred to Tester role |
| CYCLE-1 | 7.1 | Catalog Resolver EAV Fix | 2026-05-09 | 2026-05-09 |
| CYCLE-1 | 7.2 | Intake Bug-Fix Bundle | 2026-05-09 | 2026-05-09 |
| CYCLE-1 | 7.3 | Layout Regression Commit | 2026-05-09 | 2026-05-09 |
| CYCLE-1 | 8.1 | Nav + Firmware Request Consolidation | 2026-05-09 | 2026-05-09 |
| CYCLE-1 | 9.1 | Catalog Flatten (Enum Migration) | 2026-05-09 | 2026-05-09 |
| CYCLE-1 | 10.1 | Intake Scope Schema Migration | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 10.2 | Intake Wizard Shell + Steps | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 10.3 | Intake Wizard Hardening | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 10.4 | Intake Wizard Cleanup | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 11.1 | Sidebar IA Reshuffle | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 11.2 | Design System Alignment | 2026-05-10 | 2026-05-10 |
| CYCLE-1 | 12.1 | Admin Audit Log | 2026-05-12 | 2026-05-12 |

### CYCLE-2 — Flow 1B Quality Gate

| BUILDID | Story | Title | Start | End |
|---------|-------|-------|-------|-----|
| CYCLE-2 | 1.1 | IntakeRequest Schema Extensions for SR Attestation + Conditional Approval | 2026-05-26 | 2026-05-26 |
| CYCLE-2 | 1.2 | recordGateDecision Lambda + SR Decision Panel UI | 2026-05-26 | 2026-05-26 |
| CYCLE-2 | 1.3 | SR Attestation Download Document | 2026-05-26 | 2026-05-26 |
| CYCLE-2 | 1.4 | HQ Attestation Read-Only Row | 2026-05-26 | 2026-05-26 |
| CYCLE-2 | 1.5 | Per-Binary Security Review File Upload | — | — |
| CYCLE-2 | 1.6 | Per-Binary Pass/Fail Hard Gate | — | — |
| CYCLE-2 | 1.7 | Release Classification Display + TPSA Conditional | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 1.8 | Pipeline Routing (Major / Minor) | — | — |
| CYCLE-2 | 1.9 | Record Lineage 2FK Display | — | — |
| CYCLE-2 | 1.10 | Flag For Revision Per Artifact | — | Deferred to BC-3 |
| CYCLE-2 | 1.11 | TPSA State Control | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 2.1 | createWaiver Engine Extension + FC-3 Regression | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 2.2 | Waiver Dialog MVP UX | — | Deferred to BC-3 |
| CYCLE-2 | 2.3 | Waiver Lifecycle Auto-Clear | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 2.4 | HQ View Of Waived Artifact | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 2.5 | Authorization Regression (Waiver) | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 2.6 | Site Cascade Waiver (D18) | — | — |
| CYCLE-2 | 3.1 | ComponentAudit Entity Schema | 2026-05-27 | 2026-05-27 |
| CYCLE-2 | 3.2 | rejectComponent Mutation | — | — |
| CYCLE-2 | 3.3 | Per-Component Re-upload Zip Exception | — | — |
| CYCLE-2 | 3.4 | Component Version Chain | — | Deferred to BC-3 |
| CYCLE-2 | 3.5 | ReviewRecord Container | — | — |
| CYCLE-2 | 3.6 | Roll-up Comment Thread | — | — |
| CYCLE-2 | 3.7 | Resubmission Indicator MVP UX | — | Deferred to BC-3 |
| CYCLE-2 | 3.8 | BundleUpdateEvent Kind Enum | — | — |
| CYCLE-2 | 4.1 | SR Dashboard Page + Summary Cards | 2026-05-27 | 2026-05-28 |
| CYCLE-2 | 4.2 | Needs-Action-Now List | 2026-05-27 | 2026-05-28 |
| CYCLE-2 | 4.3 | Product-Line Filter Chip | 2026-05-27 | 2026-05-28 |
| CYCLE-2 | 4.4 | ActivityNotification Schema + Hook | — | — |
| CYCLE-2 | 4.5 | Email Notification Send | — | — |
| CYCLE-2 | 4.6 | Activity Inbox HQ Dashboard | — | — |
| CYCLE-2 | 4.7 | Dismiss Activity Notification | — | — |
| CYCLE-2 | 4.8 | Email Inbox Atomic + Audit | — | — |
| CYCLE-2 | 4.9 | SR Attestation Format Finalization | — | — |
| CYCLE-2 | 4.10 | Attestation Download Authz Regression | — | — |
| CYCLE-2 | 5.1 | Audit Export Format Ratification | — | — |
| CYCLE-2 | 5.2 | exportComplianceAuditTrail Lambda | — | — |
| CYCLE-2 | 5.3 | Filterable Audit Export | — | — |
| CYCLE-2 | 5.4 | Authorization Matrix Harness Extension | — | — |
| CYCLE-2 | 5.5 | Segregation Of Duties Test | — | — |
| CYCLE-2 | 5.6 | Service-Tech Doc Visibility Server-Side Gate | — | — |
| CYCLE-2 | 5.7 | Audit Completeness Property Test | — | — |
| CYCLE-2 | 5.8 | Audit Export Performance | — | — |
| CYCLE-2 | 5.9 | Cryptographic Controls Evidence | — | 🔴 Blocked (OQ-38 / D21) |
| CYCLE-2 | 5.10 | SBOM Third-Party Completeness Helper Text | — | — |

> Stories 4.1–4.3 wrap-up reviews landed 2026-05-28 (`build-cycles/cycle-2/wrap-up/story-4.{1,2,3}-review.md`). Story 4.1 carries one Engineering-Principal sign-off item (routing deviation D-1: dashboard unified under `/` via role dispatch on `DashboardPage`; legacy `/security-reviewer/dashboard` redirects).

---

## Quality Metrics

| Metric | Target | Current | Status |
|--------|--------|---------|--------|
| Unit Test Coverage | ≥85% | ~99% statements / ~88% branches (BC-1 close) | ✅ |
| Integration Tests | 100% pass | Per-PR green | 🟡 In Progress |
| Code Review | All stories | 78/106 stories closed via wrap-up review | 🟡 In Progress |
| Documentation | All stories | 78/106 stories have wrap-up review docs | 🟡 In Progress |

---

## Completed Steps

- [x] **Discovery**: 2026-05-01
  - Evidence: `docs/requirements.md`, `discovery/baseline/functional-scope.md`
- [x] **System Discovery + Deep-Dive (BC-1 close refresh)**: 2026-05-22
  - Evidence: `context-project/architecture/current/00-system-overview.md`, `01-intake-pipeline-deep-dive.md`
- [x] **Build Cycles plan (BC-1)**: 2026-05-01
  - Evidence: `build-cycles/cycle-1/cycle-plan.md`
- [x] **Build Cycles plan (BC-2)**: 2026-05-22
  - Evidence: `build-cycles/cycle-2/cycle-plan.md`
- [x] **Cycle 0 — Walking Skeleton**: 2026-05-04
  - Evidence: BC-0 wrap-up under `build-cycles/cycle-0/wrap-up/`
- [x] **Cycle 1 — Flow 1A Intake + i18n**: 2026-05-22
  - Evidence: 37 story reviews + handover in `build-cycles/cycle-1/wrap-up/` (`handoff-to-cycle-2.md`)

---

## Upcoming

1. **Cycle 2 Epic 1** — close Stories 1.5, 1.6, 1.8, 1.9 (per-binary upload, pass/fail gate, pipeline routing, record-lineage display)
2. **Cycle 2 Epic 2.6** — site-cascade waiver (D18, Engineering Principal + PDM, Day 10 close target)
3. **Cycle 2 Epic 3** — Stories 3.2, 3.3, 3.5, 3.6, 3.8 (rejectComponent, re-upload, ReviewRecord, comments, BundleUpdateEvent)
4. **Cycle 2 Epic 4** — close Stories 4.4–4.10 (Activity inbox + email notifications + attestation format finalization)
5. **Cycle 2 Epic 5** — Audit Export pipeline (compliance-critical; close before 2026-06-30 milestone)
6. **Cycle 2 wrap-up + handover to Cycle 3** — target 2026-06-06

---

## Blockers

| ID | Description | Owner | Opened | Status |
|----|-------------|-------|--------|--------|
| OQ-38 | Cryptographic controls evidence (Story 5.9) — pending closure | Engineering Principal | 2026-05-22 | 🔴 Blocked |
| D21 | Cryptographic controls scope decision (paired with OQ-38) | Engineering Principal + PDM | 2026-05-22 | 🔴 Blocked |
| P-5 | Compliance / audit advisor identification (pre-build gate for Epic 5 AC-9) | Tiny Team | 2026-05-22 | 🟡 Pending |
| D18 | Site-cascade waiver scope (Story 2.6) | Engineering Principal + PDM | 2026-05-22 | 🟡 Pending (Day 10 close target) |
| D16 | ReviewRecord container scope (Story 3.5) | Engineering Principal | 2026-05-22 | 🟡 Pending (Day 10 close target) |
| OQ-37 | Customer-data compliance boundary in writing | Sheng Tong | 2026-04-01 | 🟡 Pending |

---

## Agent Activity

| Agent | Last Action | Status | Updated |
|-------|-------------|--------|---------|
| AIRE_DISCOVERY_ANALYST | Requirements synthesis | Idle | 2026-05-01 |
| AIRE_ANALYST_PM_BROWNFIELD | System overview + intake-pipeline deep-dive refresh (BC-1 close) | Idle | 2026-05-22 |
| AIRE_ARCHITECT | Cycle 2 implementation plan | Idle | 2026-05-22 |
| AIRE_BUILD_CYCLE_PLANNER | Cycle 2 plan + handoff document | Idle | 2026-05-22 |
| AIRE_UI_UX_DESIGNER | BC-2 design pass (Epic 4 input reference + coverage worksheet) | Idle | 2026-05-20 |
| AIRE_DEV | Cycle 2 Epic 4 (Stories 4.1–4.3) merged | Active | 2026-05-27 |
| AIRE_REVIEWER | Per-story wrap-up reviews | Active | 2026-05-28 |
| AIRE_QA | Per-PR validation | Active | 2026-05-28 |

---

## Notes

- **Narrative changelog**: prior inline `**Last Updated (…)**` / `**Previously (…)**` prose entries (46 blocks, ~260 KB) were archived to [`build-cycles/cycle-1/wrap-up/status-changelog.md`](../build-cycles/cycle-1/wrap-up/status-changelog.md) during the 2026-05-28 rewrite. The canonical record for each item is its `*-review.md` file under the corresponding `build-cycles/cycle-N/wrap-up/`.
- **Test-data discipline**: per the 2026-05-08 decision, the production-targeted CI steps (`Authorization matrix (against sandbox)`, `E2E against deployed main`) are disabled — re-enable only against a non-prod environment per Engineering Principal sign-off.
- **E2E ownership**: end-to-end testing has been transferred from DEV to a dedicated Tester role (TBD). Story 6.4 (Cycle 1) and any cycle-final E2E stories halt on that handoff.
- **Compliance**: ISO 27001 / SOC 2 close-out target is 2026-06-30. Cycle 2 closes 2026-06-07 with a 23-day cushion if on schedule.
