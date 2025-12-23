# OOTD-Today
A Wechat mini program for user to decide what to ware for today's OOTD.

## Concept

OOTD: Outfit Of The Day

## Product Function

### Summary

Today’s OOTD is a decision‑first app that helps users choose what to wear in under a minute. It uses a lightweight five‑step flow — Mood/Feelings → Event → Style → Color → Weather — to set clear constraints and generate a top outfit pick plus two quick alternates. Users can accept the best suggestion, or make one‑tap swaps (top/bottom/shoes/outerwear/accessories) with short explainers like “warmer due to wind” or “complements palette”.

Major functions include:
- Decision Mode: One‑tap OOTD with a ranked top pick and two alternates; step chips to capture Mood, Event (e.g., interview, date, holiday), Style, Color, and Weather.
- Wardrobe Management: Add items with photos, category/brand/size/color/material/season; tags for style/event/palette; bulk import and de‑dupe; wear count and cost‑per‑wear.
- Outfit Builder: Drag‑and‑drop composition with AI assist for missing items, palette tweaks, and wardrobe alternates; save drafts/templates/capsules.
- OOTD Posting: Post photos (up to 10) with notes, mood, event, hashtags; link outfits and items; configurable privacy (Public/Friends/Private).
- Calendar & History: Timeline of OOTDs; filters by event/palette/tags; re‑wear insights and search.
- Recommendations: Decision‑oriented ranking using Mood/Event/Style/Color/Weather plus seasonality and wardrobe availability; avoids over‑recommending repeats.
- Privacy & Moderation: Visibility controls for posts/wardrobe/profile; automated filtering for prohibited content; block/suspend/ban with audit trail.
- Notifications & Search: Batched notifications; search by tags/color/brand/item/event/palette/capsule/user.

Non‑functional goals: fast Decision Mode init (<500ms p90 with cached inputs), clear privacy (city‑level location only), accessibility (WCAG AA), and internationalization (EN/zh‑CN).

For details, see `Product Requirement Documentation.md` and the Chinese version `产品需求文档.zh-CN.md`.