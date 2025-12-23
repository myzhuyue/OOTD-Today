# Product Requirements Document — Today’s OOTD

## Version

| Version | Date       | Author    | Changes                                                    | Status |
|--------:|:-----------|:----------|:-----------------------------------------------------------|:-------|
| 0.1.0   | 2025-12-23 | myzhuyue  | Initial PRD draft with TOC and core feature requirements. | Draft  |
| 0.2.0   | 2025-12-23 | myzhuyue  | Pivot to decision-first: added Decision Mode, updated goals/KPIs, deprioritized social. | Draft  |
| 0.2.1   | 2025-12-23 | myzhuyue  | Added Event step and presets; integrated Event into Decision Mode and Recommendations.   | Draft  |
| 0.3.0   | 2025-12-23 | myzhuyue  | Established 5-step flow: Mood → Event → Style → Color → Weather; updated menu and sections. | Draft  |

## Menu
- [Purpose](#purpose)
- [Glossary](#glossary)
- [Personas](#personas)
- [User Journey](#user-journey)
- [Decision Mode](#decision-mode)
- [Decision Flow](#decision-flow)
  - [Mood & Feelings](#mood--feelings)
  - [Event](#event)
  - [Style](#style)
  - [Color](#color)
  - [Weather](#weather)
- [Event](#event)
- [User Management](#user-management)
  - [Onboarding](#onboarding)
  - [Register & Login](#register--login)
  - [Profile](#profile)
  - [Ban](#ban)
  - [Block](#block)
  - [Suspension](#suspension)
  - [Deactivation](#deactivation)
- [Wardrobe Management](#wardrobe-management)
- [Outfit Builder](#outfit-builder)
- [OOTD Posting](#ootd-posting)
- [Calendar & History](#calendar--history)
- [Recommendations](#recommendations)
- [Weather](#weather)
- [Social](#social)
  - [Feed](#feed)
  - [Likes](#likes)
  - [Comments](#comments)
  - [Collections](#collections)
  - [Share](#share)
- [Privacy](#privacy)
- [Notifications](#notifications)
- [Search & Explore](#search--explore)
- [Moderation](#moderation)
- [Analytics & KPIs](#analytics--kpis)
- [Non-Functional](#non-functional)
- [Out of Scope](#out-of-scope)

---

## Purpose

Today’s OOTD helps users capture, curate, and share their daily outfit choices, while providing smart recommendations based on weather, occasion, personal style, and wardrobe history.

Goals:
- Primary: Enable a confident outfit decision in under 60 seconds.
- Secondary: Make planning enjoyable and repeatable.
- Tertiary: Help users get more value from their existing wardrobe.
- Social features are optional and secondary, focused on learning rather than engagement.
- Provide actionable insights (what works, what repeats, what fits preferences).

## Glossary

- Outfit: A combination of wardrobe items worn together.
- Wardrobe Item: A single clothing piece or accessory (e.g., shirt, pants, shoes).
- Capsule: A small, cohesive set of items that mix-and-match well.
- Occasion: Context of wearing (work, casual, date, travel, formal, gym, etc.).
- Style: User-defined preference tags (minimal, streetwear, vintage, classic, etc.).
- Fit Notes: Short notes about how items fit or feel (tight, relaxed, cropped, etc.).
- Palette: Color scheme used in an outfit (neutrals, monochrome, complementary).
- Hashtags: #ootd, #capsule, #color, #occasion, #brand.

## Personas

- Everyday Stylist: Wants quick outfit ideas aligned with preferences and weather.
- Collector: Documents wardrobe thoroughly; focuses on tags, brands, and maintenance.
- Social Sharer: Posts OOTD consistently; values engagement and discoverability.
- Minimalist: Seeks repeatable capsules and metrics on re-wear efficiency.

## User Journey

- Decide: Follow the 5-step flow — Mood → Event → Style → Color → Weather — to get 1–3 ready-to-wear suggestions.
- Plan: Adjust suggestions with quick swaps; apply constraints (comfort notes, dress codes).
- Review: Check calendar/history, re-wear stats; refine style preferences.
- Maintain: Add/organize wardrobe items; manage privacy and notifications. Social optional.

## Decision Mode

- One-Tap OOTD: Present a single best outfit first, with Accept/Next options.
- Alternatives: Offer 2 quick alternates (e.g., warmer/cooler, more formal/casual).
- Inputs: Mood, event, style preferences, color selection, weather (city-level), wardrobe availability, recent repeats.
- Constraints: Respect comfort notes, color dislikes, dress codes, and seasonality.
- Quick Swaps: One-tap swap for any slot (top, bottom, shoes, outerwear, accessory).
- Explainers: Short reasons ("warmer due to wind", "complements palette", "high re-wear score").
- Offline Ready: Cache wardrobe and last weather; fall back to season-based picks.
- Flow: Present step chips in order — Mood → Event → Style → Color → Weather — with sensible defaults and the ability to skip.
- KPI Target: Median time-to-decision < 60s; first-suggestion acceptance rate > 40%; step completion taps ≤ 5.
- Save & Apply: Save decision to Calendar; optional photo later; reminders disabled by default.

## User Management

### Onboarding
- Consent: Accept ToS and Privacy Policy; optional tutorial.
- Preferences: Select styles, occasions, color likes/dislikes; set default privacy for posts.
- Permissions: Camera, photo library, location (for weather), notifications.

### Register & Login
- Methods: Email + password, phone + OTP; optional Apple/Google sign-in.
- Sessions: Token-based with refresh; auto-login until logout.
- Security: Rate-limit attempts; optional 2FA; device/session checks.

### Profile
- Fields: Avatar, display name, bio, city, style preferences, capsules.
- Stats: Posts, likes, collections, followers/following; re-wear and engagement metrics.
- Privacy: Default post privacy, social visibility, wardrobe visibility controls.
- Badges: Consistency streaks, capsule builder, community contributor.

### Ban
- Permanent removal for repeated policy violations (harassment, illegal content, fraud).
- Account disabled; content hidden from feeds/search; audit logs retained.
- Single appeal within 30 days; review within 7 days.

### Block
- Mutual content invisibility; cannot follow, comment, like, collect, or share.
- Public announcements unaffected; no private data exposed.

### Suspension
- Temporary restrictions (24h, 7d, 30d) for minor first-time violations.
- Read-only access; posting/engagement disabled; may escalate to ban.

### Deactivation
- User-initiated; profile hidden; posts not recommended; notifications paused.
- Reactivation restores settings and content.
- Separate irreversible deletion flow (subject to retention requirements).

## Wardrobe Management

- Item Attributes: Photos, category, subcategory, brand, size, color, material, seasonality, care notes, price, purchase date.
- Tags: Style, occasion, palette, capsule membership, fit notes.
- Photos: Multi-angle uploads; background removal option; AI-assisted category/color.
- Import: Bulk add via camera roll, receipt scan, or CSV; dedupe checks.
- Maintenance: Status (active, archived, to-sell, to-repair); wear count; cost-per-wear.
- Privacy: Wardrobe visibility (Private, Friends, Public); item-level overrides.

## Outfit Builder

- Composition: Drag-and-drop items into slots (top, bottom, footwear, outerwear, accessories).
- Constraints: Size/season compatibility, color harmony suggestions, occasion fit.
- AI Assist: Recommend missing items, palette tweaks, or alternates from wardrobe.
- Save: Save as draft, template, or capsule; mark preferred outfits.

## OOTD Posting

- Content: Photos (up to 10), notes, mood, occasion, location (city-level only), hashtags.
- Links: Optional brand/product links; affiliate disclosures.
- Attachments: Link to the outfit and wardrobe items used.
- Privacy: Public, Friends, Private; default configurable.
- Integrity: No illegal or harmful content; auto-filter and moderation routing.

## Calendar & History

- Timeline: Monthly/weekly views of OOTDs; filters by occasion, palette, tags.
- Re-wear Insights: Track repeats, cost-per-wear, seasonal trends.
- Search: Find past outfits by tags, color, item, occasion.
- Reminders: Optional prompts to revisit popular outfits.

## Recommendations

- Inputs: Mood, event, style, color, weather, location seasonality, wardrobe availability.
- Outputs: Decision-first ranking with a top pick and 2 alternates; explainable factors.
- Diversity: Avoid over-recommending the same items; respect user dislikes.
- Learning: Adapt to user likes, collections, and re-wear behavior.

## Weather

- Weather: Integrate city-level forecast (temp, precipitation, wind); no precise GPS stored.
- Seasonality: Tag items and prefer season-appropriate choices.

## Event

- Purpose: Provide context-specific guidance to accelerate decisions beyond general occasion.
- Presets: Interview, Meet someone (date/social), Holiday (travel/leisure), Presentation, Formal dinner, Casual day, Gym.
- Rules:
  - Interview: Higher formality; muted palette; avoid logos; polished footwear.
  - Meet someone: Smart casual; approachable colors; comfort prioritized; weather-adjusted outerwear.
  - Holiday: Travel-friendly fabrics; layer-ready; comfortable footwear; compact accessories.
  - Presentation: Elevated smart; minimal distractions; confident palette; tidy outerwear.
  - Formal dinner: Dress code-aligned; refined materials; subdued palette; statement accessory optional.
  - Casual day: Comfort-first; everyday palette; weather-adaptive.
  - Gym: Athletic category only; breathable materials; secure footwear.
- Mapping: Each event maps to formality band, palette constraints, category inclusion/exclusion, and accessory hints.
- UI: Event chips shown first in Decision Mode; single tap sets constraints; optional custom event with saved rules.

## Decision Flow

- Overview: A lightweight, five-step path to a confident decision.
- Order: Mood → Event → Style → Color → Weather. Each step sets constraints used by the recommender.

### Mood & Feelings

- Presets: Calm, Confident, Energetic, Cozy, Minimal, Bold.
- Effects: Adjust palette (e.g., Calm → neutrals; Bold → high-contrast), silhouette comfort, and style tilt.
- Defaults: If skipped, use recent mood or neutral.

### Style

- Presets: Minimal, Streetwear, Vintage, Classic, Smart Casual, Sporty.
- Effects: Prioritize matching categories/brands, typical silhouettes, and accessory hints.
- Constraints: Exclude conflicting items (e.g., Sporty excludes formal leather shoes unless Event requires).

### Color

- Presets: Neutrals, Monochrome, Complementary, Earth tones, Pastels, High-contrast.
- Effects: Limit palette; suggest swaps to fit selection; respect user color dislikes.
- Assist: Auto-scan wardrobe colors to propose feasible palettes.

### Weather

- Inputs: City-level forecast (temperature bands, precipitation, wind).
- Effects: Layering suggestions, fabric suitability, footwear traction, outerwear necessity.
- Offline: Use last known weather or season fallback.

## Social

Note: Social features are secondary and may be disabled in early releases. Focus remains on fast decision-making.

### Feed
- Home: Friends + followed creators; optional algorithmic recommendations.
- Explore: Trending tags, palettes, capsules, occasions; search bar.

### Likes
- Single-tap like; toggle; counts and friend list.
- Rate-limit bursts; detect bot-like behavior.

### Comments
- Threaded with one-level replies; timestamps; @mentions and #hashtags.
- Picture attachments allowed; no videos.
- Edit window: 10 minutes; deletion with “edited” indicator.

### Collections
- Save posts to folders (e.g., Capsules, Palettes, Occasions); reorder and tag.
- Private by default; optional sharing to Friends.

### Share
- Audience: Public, Friends, Private; owner can disable resharing.
- External share: Platform-native share previews; exclude sensitive metadata.

## Privacy

- Controls: Post visibility, wardrobe visibility, profile visibility, comments on private posts.
- Defaults: Private wardrobe; configurable post default.
- Data: City-level only for location; no precise GPS. Compliance with relevant regulations.

## Notifications

- Events: Likes, comments, follows, collections, recommendations, reminders.
- Batched to reduce spam; configurable per event type.

## Search & Explore

- Search by tags, color, brand, item, occasion, palette, capsule, user.
- Filters and sort (recent, popular, re-wear, season).

## Moderation

- Auto-filter prohibited content; keyword/image checks; user reports.
- Enforcement: Block, suspend, ban; audit trail; appeal flow.
- Safety: No harm, hate, sexual or violent content; remove and restrict.

## Analytics & KPIs

- Decision: Median time-to-decision, first-suggestion acceptance rate, quick-swap usage.
- User: DAU/MAU, retention, wardrobe completeness.
- Content: Avg likes/comments, collections, share rate.
- Recommendation: Top-pick acceptance, re-wear adoption, alternate pick usage.
- Commerce (optional): Click-through on brand links, affiliate performance.

## Non-Functional

- Performance: <200ms feed load p90; <1s outfit builder init p90.
- Decision Mode init: <500ms p90 with cached inputs.
- Security: OWASP best practices; rate-limits; encrypted at rest/in transit.
- Privacy: Minimal data; city-level location; clear consent & deletion.
- Accessibility: WCAG AA; alt text; keyboard navigation.
- Internationalization: EN/zh-CN first; extensible locales.

## Out of Scope

- Precise GPS storage or map of user locations.
- AR try-on or 3D fit; advanced virtual closets (future consideration).
- Full e-commerce cart/checkout.
