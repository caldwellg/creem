---
"@creem_io/convex": minor
---

Convex integration v2 — major feature release with breaking changes.

Features:

- i18n support for all billing UI text
- Usage limits / feature gates (`usageLimits`) with scoped trial expiry and `eligibilityScopeId` in the catalog
- Credits widgets for React and Svelte (`Credits*` components)
- Billing history widget (`BillingHistory`)
- Payment recovery primitives (`PaymentRecoveryBanner`, `PaymentRecoveryButton`)
- Provider factories: `createCreemReact` / `createCreemSvelte` with `CreemConvexProvider`
- Subscription widget slots (`SubscriptionGrid`, `SubscriptionGroup`, `SubscriptionGroupSelector`, `SubscriptionIntervalSelector`, `SubscriptionItem*` slot components, `SubscriptionUnitPicker`)
- `cancelPendingScheduledSubscriptionUpdates` mutation; scheduled-update cancellation integrated into the subscription update flow
- Product descriptions render markdown tables
- New `INTEGRATION.md` guide including brownfield migration checklist

Breaking changes:

- `creem` is now a peer dependency (`^1.5.3`) instead of a regular dependency — install it alongside this package
- Svelte peer dependency is now upstream `convex-svelte` (`>=0.14.0`) instead of `@mmailaender/convex-svelte`
- `standardwebhooks` dropped; webhook verification uses the creem 1.5 SDK and its new webhook event structure
- Deprecated `Product.Group` compatibility alias removed
- `serverIdx` replaced with `server` parameter in the Creem server configuration
- User-facing errors are thrown as `ConvexError` instead of `Error`
