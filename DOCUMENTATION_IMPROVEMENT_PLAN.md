# Pluvel Documentation Improvement Plan

## Current State
- **132 pages created** across guides, features, integrations, and accountants sections
- **Audit Score:** 73/100 (C+)
- **Key Issues:** Missing ~20 features, AI-sounding prose, some navigation inaccuracies

---

## Phase 1: Missing Feature Documentation (Priority)

### Tier 1 - High Impact (Create First)

| Feature | Path | Why Priority |
|---------|------|--------------|
| **AI CFO** | `features/accounting/ai-cfo.mdx` | Major differentiator, mentioned nowhere |
| **Anomaly Detection** | `features/accounting/anomaly-detection.mdx` | Unique selling point |
| **Budgets** | `features/accounting/budgets.mdx` | Core accounting feature |
| **Year-End Close** | `features/accounting/year-end-close.mdx` | Critical workflow |
| **Estimates/Quotes** | `features/invoicing/estimates.mdx` | Sales workflow gap |

### Tier 2 - Medium Impact

| Feature | Path | Notes |
|---------|------|-------|
| **Projects** | `features/accounting/projects.mdx` | Job costing, project profitability |
| **Fixed Assets** | `features/accounting/fixed-assets.mdx` | Depreciation tracking |
| **Credit Notes** | `features/invoicing/credit-notes.mdx` | Invoice adjustments |
| **Purchase Orders** | `features/bills/purchase-orders.mdx` | Procurement workflow |
| **Vendor Credits** | `features/bills/vendor-credits.mdx` | AP adjustments |

### Tier 3 - Complete Coverage

| Feature | Path | Notes |
|---------|------|-------|
| **Expense Reports** | `features/bills/expense-reports.mdx` | Employee reimbursements |
| **Inventory** | `features/accounting/inventory.mdx` | If supported |
| **Payroll Analytics** | `features/payroll/analytics.mdx` | Workforce insights |
| **New Hire Reports** | `features/payroll/new-hire-reports.mdx` | Compliance reporting |
| **Notifications** | `features/company/notifications.mdx` | Alert preferences |
| **Company Profile** | `features/company/profile.mdx` | Business info management |
| **Direct Deposit Setup** | `features/payroll/direct-deposit-setup.mdx` | Bank verification flow |

### Tier 4 - Firm Mode Additions

| Feature | Path | Notes |
|---------|------|-------|
| **Firm Messages** | `accountants/dashboard/messages.mdx` | Client communication |
| **Firm Staff** | `accountants/firm-staff.mdx` | Team management |
| **Firm Calendar** | `accountants/dashboard/firm-calendar.mdx` | Scheduling across clients |
| **Bookkeeper Tools** | `accountants/workflows/bookkeeper-tools.mdx` | Batch operations |

---

## Phase 2: Humanization Guidelines

### Writing Style Rules

**DO:**
- Start some pages mid-thought: "So you've got a stack of bills..."
- Use contractions naturally: "won't", "you'll", "it's"
- Vary sentence length dramatically (5 words to 25 words)
- Include one "honestly" or "actually" per 500 words
- Reference real scenarios: "Your landlord sends a rent invoice on the 1st..."
- Admit limitations: "This works great for most cases, but if you..."
- Use parenthetical asides: (yes, even that weird state tax form)

**DON'T:**
- Start every section with "The X feature allows you to..."
- Use "comprehensive", "robust", "seamless" (AI tells)
- Make every section the same length
- Always include troubleshooting (only where actually needed)
- Use perfect parallel structure in every list

### Sentence Starters to Rotate

Instead of "You can..." try:
- "Here's how to..."
- "To do this..."
- "When you need to..."
- "If you're looking to..."
- Just start with the action: "Click Settings..."
- Ask a question: "Need to add a contractor mid-month?"

### Depth Variation

| Page Type | Treatment |
|-----------|-----------|
| Core features (invoicing, payroll) | Deep, 400-600 words |
| Simple features (notifications) | Brief, 150-200 words |
| Complex workflows (year-end) | Very detailed, 600-800 words |
| Reference pages (tax forms) | Tables + minimal prose |

---

## Phase 3: Content Fixes

### Navigation Path Corrections

Review and fix paths that reference:
- "Go to Payroll → Run Payroll" (verify actual nav structure)
- "Settings → Tax" (confirm this exists)
- Dashboard locations for each feature

### Screenshot Placeholders

Either:
1. Remove `<Frame>` blocks with placeholder images, OR
2. Create actual screenshots (preferred for key workflows)

Key pages needing real screenshots:
- `run-payroll.mdx` - Payroll review screen
- `creating-invoices.mdx` - Invoice builder
- `reconciliation.mdx` - Reconciliation interface
- `ai-cfo.mdx` - AI insights dashboard (NEW)

### Cross-Reference Audit

Verify all internal links (`href="/guides/..."`) point to pages that exist.

---

## Phase 4: Voice Humanization Pass

### Pages to Rewrite (Most AI-Sounding)

Based on audit, these need voice revision:

1. `features/accounting/chart-of-accounts.mdx` - Too textbook
2. `features/compliance/calendar.mdx` - Robotic structure
3. `features/reports/profit-loss.mdx` - Reads like a manual
4. `accountants/overview.mdx` - Generic pitch language
5. `integrations/overview.mdx` - List-heavy, no personality

### Humanization Techniques

**Add "gotchas":**
```mdx
<Warning>
California has daily overtime rules. If someone works 9 hours in a day, that extra hour is OT — even if their weekly total is under 40. We handle this automatically, but you should know it's happening.
</Warning>
```

**Add real examples:**
```mdx
Say you run a design agency. A client pays their $5,000 invoice, but then asks for a $500 credit because you delivered 2 days late. Instead of voiding the whole invoice...
```

**Add casual asides:**
```mdx
The Balance Sheet shows what your business owns and owes at a specific moment. (Think of it as a financial selfie — here's exactly where things stand right now.)
```

**Vary the depth:**
```mdx
## Viewing your P&L

Go to Reports → Profit & Loss. Done.

Want more detail? You can filter by date range, compare to previous periods, or drill into any line item to see the transactions behind it.
```

---

## Phase 5: mint.json Updates

Add new pages to navigation:

```json
{
  "group": "Accounting",
  "pages": [
    "features/accounting/chart-of-accounts",
    "features/accounting/journal-entries",
    "features/accounting/categorization",
    "features/accounting/bank-rules",
    "features/accounting/ai-cfo",
    "features/accounting/anomaly-detection",
    "features/accounting/budgets",
    "features/accounting/projects",
    "features/accounting/fixed-assets",
    "features/accounting/year-end-close"
  ]
}
```

Similar additions for Invoicing, Bills, Payroll, Company sections.

---

## Implementation Order

### Week 1: High-Impact New Pages
1. Create AI CFO page (flagship feature)
2. Create Anomaly Detection page
3. Create Budgets page
4. Create Year-End Close page
5. Create Estimates page

### Week 2: Medium-Impact + Voice Pass
1. Create remaining Tier 2 pages
2. Rewrite 5 most AI-sounding pages
3. Add real examples to 10 key pages

### Week 3: Complete Coverage
1. Create all Tier 3 & 4 pages
2. Fix navigation paths across all pages
3. Update mint.json with new pages
4. Cross-reference link audit

### Week 4: Polish
1. Final voice consistency pass
2. Screenshot placeholders resolved
3. Test local dev server (need Node LTS)
4. Final review

---

## Success Metrics

| Metric | Current | Target |
|--------|---------|--------|
| Coverage Score | 72/100 | 95/100 |
| Flow/Accuracy | 81/100 | 90/100 |
| Writing Quality | 75/100 | 85/100 |
| Human Voice | 65/100 | 85/100 |
| **Overall** | **73/100** | **90/100** |

---

## Sample Rewrite: Before/After

### Before (AI-sounding):
```
## Overview

The Chart of Accounts feature allows you to manage your general ledger accounts. You can create, edit, and organize accounts into categories. The system supports hierarchical account structures for comprehensive financial tracking.
```

### After (Human):
```
## Your Chart of Accounts

This is where all your accounts live — the buckets that every transaction flows into. Assets, liabilities, revenue, expenses. If you've used QuickBooks or Xero, you know the drill.

Pluvel sets you up with a standard chart when you complete setup, but you can customize it however you want. Add accounts, rename them, reorganize the hierarchy. Just don't delete accounts that have transactions — we'll archive them instead.
```

---

## Files to Create (22 total)

```
features/accounting/ai-cfo.mdx
features/accounting/anomaly-detection.mdx
features/accounting/budgets.mdx
features/accounting/projects.mdx
features/accounting/fixed-assets.mdx
features/accounting/year-end-close.mdx
features/accounting/inventory.mdx
features/invoicing/estimates.mdx
features/invoicing/credit-notes.mdx
features/bills/purchase-orders.mdx
features/bills/vendor-credits.mdx
features/bills/expense-reports.mdx
features/payroll/analytics.mdx
features/payroll/new-hire-reports.mdx
features/payroll/direct-deposit-setup.mdx
features/company/notifications.mdx
features/company/profile.mdx
accountants/dashboard/messages.mdx
accountants/dashboard/firm-calendar.mdx
accountants/firm-staff.mdx
accountants/workflows/bookkeeper-tools.mdx
```

---

## Notes

- AI CFO should be treated as a flagship page — this is Pluvel's differentiator
- Consider adding a "What makes Pluvel different" comparison page
- Firm Mode pages should emphasize efficiency gains with real numbers
- All new pages should follow humanization guidelines from day one
