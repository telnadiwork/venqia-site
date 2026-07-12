# Venqia Launch Phases and Checklist

## Purpose
This document turns the strategy into execution phases with clear entry and exit criteria.

## Scope
- Homepage: index.html
- Trading vertical page: trading-financial-markets.html
- Shared brand asset: favicon.svg

## Execution Update
- Date: 2026-07-13
- Completed now:
  - Homepage vertical control semantics normalized to true tab behavior.
  - Form duplicate-submit guard and timeout handling implemented on both pages.
  - Input trim and empty-after-trim validation added on both pages.
  - Trading page Twitter/Open Graph metadata parity improved.
  - Copy compression and readability polish applied on both pages.
  - Open Graph image asset created: og-image.png.
  - Automated mobile overflow checks run for 390 and 430 widths (no overflow detected).
  - Strategic message architecture upgraded on both pages (trading-first hierarchy, differentiators, trust ladder, partner intake flow).
  - CTA system upgraded to partner-model language and staged conversion logic.
- Pending validation:
  - Keyboard-only validation across complete conversion path.
  - Cross-browser manual QA (Edge, Firefox, Safari if available).
  - Live social preview validation against production URL.

## QA Evidence Log
- 2026-07-13 automated checks:
  - Homepage form:
    - Forced offline submit returns clear fallback error message.
    - Online submit reaches success state (contact-success class applied).
  - Trading page form:
    - Forced offline submit returns clear fallback error message.
    - Online submit reaches success state (contact-success class applied).
  - Mobile overflow checks:
    - 390 and 430 widths: no horizontal overflow on both pages.
  - Console/runtime:
    - No console errors in normal-flow checks on both pages.

## Phase 0: Decision Lock

### Objective
Lock the intent so all edits optimize for partner conversion quality.

### Tasks
- [ ] Confirm single audience statement: partner conversations, not retail signup.
- [ ] Confirm primary conversion event: successful form submission.
- [ ] Confirm no-go rule: no change that reduces trust or clarity.

### Exit Criteria
- [ ] Audience statement approved.
- [ ] Conversion event approved.
- [ ] No-go rule approved.

---

## Phase 1: P0 Launch-Critical Fixes

### Objective
Remove behavior and reliability risks that can block launch.

### Tasks
- [x] Resolve mixed vertical control semantics on homepage:
  - [x] If it is a tab pattern, every item behaves as tabs.
  - [ ] If it is navigation, every item is navigation.
  - [ ] If mixed behavior is required, split into separate clearly named controls.
- [x] Harden form flow on both pages:
  - [x] Disable submit while request is in flight.
  - [x] Prevent duplicate submits on repeated click/enter.
  - [x] Add timeout handling with clear retry guidance.
  - [x] Ensure success and error states are mutually exclusive.
- [ ] Mobile integrity hardening:
  - [x] No horizontal overflow at 390 and 430 widths.
  - [ ] No clipped CTA labels.
  - [ ] Anchor targets not hidden by sticky header.

### Exit Criteria
- [ ] Keyboard-only submit flow works end-to-end on both pages.
- [x] Form behavior passes normal, slow, and timeout/error scenarios.
- [ ] Mobile checks pass at 390 and 430 with no critical defects.

---

## Phase 2: P1 Copy Compression and Message Clarity

### Objective
Increase premium tone by reducing explanation and increasing outcome clarity.

### Tasks
- [x] Rewrite long sentences into concise outcome-led lines.
- [x] Keep caveats short and downstream from value statements.
- [x] Reduce process-heavy phrasing near hero sections.
- [x] Keep key conversion lines short and direct.

### Exit Criteria
- [x] No paragraph in hero-adjacent sections feels compliance-first.
- [x] Key value lines are concise and partner-relevant.
- [x] Tone feels operator-grade and not generic.

---

## Phase 3: P2 Design Rhythm and Premium Polish

### Objective
Reduce template feel and improve editorial pacing.

### Tasks
- [x] Reduce repetitive visual block cadence.
- [x] Improve section rhythm with deliberate spacing changes.
- [x] Tighten long line lengths where readability drops.
- [x] Ensure success state UI remains clean and high-trust.

### Exit Criteria
- [x] Visual flow feels intentional on mobile and desktop.
- [x] No section appears visually redundant.
- [x] Contact areas feel clear, calm, and premium.

---

## Phase 4: P3 Metadata and Share Integrity

### Objective
Ensure previews and metadata are complete and consistent.

### Tasks
- [x] Align social metadata fields between both pages.
- [x] Verify canonical and robots directives.
- [x] Verify open graph image URL resolves publicly.
- [ ] Verify social card previews render correctly.

### Exit Criteria
- [ ] Both pages produce valid social previews.
- [ ] No missing metadata assets in production.

---

## Phase 5: QA Matrix and Sign-Off

### Objective
Run deterministic checks before deployment.

### Matrix
- Viewports: 390x844, 430x932, 768x1024, 1366x768, 1920x1080
- Browsers: Chrome, Edge, Firefox, Safari when available
- Input modes: mouse, touch, keyboard-only
- Network profiles: normal, slow profile, timeout simulation

### Tasks
- [ ] Functional QA
  - [x] Form submit succeeds with valid input on homepage.
  - [x] Form submit succeeds with valid input on trading page.
  - [x] Retry path works after forced error.
- [ ] UX QA
  - [x] No horizontal overflow.
  - [ ] No hidden anchor headers.
  - [ ] Focus indicators remain visible.
- [ ] Technical QA
  - [x] No console errors in normal flow.
  - [x] No broken image/meta links.

### Exit Criteria
- [ ] All P0 items pass.
- [ ] No critical defects open.
- [ ] Release owner sign-off complete.

---

## Phase 6: Deploy and Post-Deploy Smoke

### Objective
Deploy safely and verify production behavior.

### Pre-Deploy Checklist
- [ ] Latest branch merged and clean.
- [ ] Final content approved.
- [ ] Metadata preview checks complete.
- [ ] Rollback snapshot prepared.

### Deployment Checklist
- [ ] Deploy static assets.
- [ ] Confirm deployment success state.
- [ ] Verify live homepage load.
- [ ] Verify live trading page load.

### Post-Deploy Smoke (30 minutes)
- [ ] Complete one full form submit on homepage.
- [ ] Complete one full form submit on trading page.
- [ ] Verify success state UI appears correctly.
- [ ] Verify social preview card renders correctly.
- [ ] Verify no urgent console/runtime errors.

### Exit Criteria
- [ ] Production smoke tests pass.
- [ ] No launch-blocking issues found.

---

## Ownership and Tracking

Use this quick table during execution.

| Item | Owner | Status | Notes |
|---|---|---|---|
| Phase 0 Decision Lock |  | Not started |  |
| Phase 1 P0 Fixes |  | Complete | Interaction semantics and form resilience implemented |
| Phase 2 Copy Compression |  | Complete | Premium copy compression applied on both pages |
| Phase 3 Design Polish |  | Complete | Rhythm, hierarchy, trust and intake blocks implemented |
| Phase 4 Metadata Integrity |  | In progress | Metadata aligned and og-image.png created; live share preview pending |
| Phase 5 QA and Sign-Off |  | In progress | Functional and technical checks passed; cross-browser/live verification pending |
| Phase 6 Deploy and Smoke |  | Not started |  |

## Definition of Done
- [ ] Conversion path is stable and predictable.
- [ ] Messaging is concise and premium.
- [ ] Mobile experience is clean with no overflow defects.
- [ ] Social metadata works reliably.
- [ ] Team sign-off is documented.
