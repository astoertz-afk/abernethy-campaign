# PRD: Abernethy 2125 -- $100K Fundraiser Website

## Introduction

Abernethy Elementary in SE Portland turned 100 in 2025. The PTA is running a $100K fundraiser ("Abernethy 2125") to fund the school's next chapter -- playground improvements, classroom tech, arts programs, teacher support. The website needs to serve two audiences simultaneously: **local businesses** considering sponsorship and **families/alumni** considering personal donations. It links out to an external donations platform for payment processing.

The Canva design exports establish content and structure but the visual direction is open -- treat them as loose inspiration, not a style guide.

**Donations platform:** [BetterWorld](https://abernethyelementaryschool.betterworld.org/campaigns/general-pta-support)
**Campaign deadline:** July 1, 2026
**Brand tone:** Fun but serious. Focus on kids and the social fabric of the community. Not corporate, not guilt-driven -- proud, warm, neighborhood-level real.

## Goals

- Convert visitors into donors or sponsors via clear CTAs that link to the external donations platform
- Communicate Abernethy's story, values, and community impact compellingly enough that a stranger would want to give
- Present sponsorship tiers in a way that feels like an opportunity, not a menu
- Showcase the school's community through photography -- the site should feel alive, not corporate
- Launch as a strong single page that's architected to grow into multi-page as the campaign evolves
- Load fast, look great on mobile (parents will share links via text/social)

## User Stories

### US-001: Hero / First Impression
**Description:** As a visitor, I want to immediately understand what Abernethy 2125 is and feel compelled to keep scrolling, so I don't bounce.

**Acceptance Criteria:**
- [ ] Hero communicates: school name, Portland OR, fundraiser, $100K goal
- [ ] Primary CTA ("Donate" or "Support") visible without scrolling
- [ ] Emotional hook -- photo, tagline, or visual that creates connection in <3 seconds
- [ ] Works on mobile without horizontal scroll or text overflow
- [ ] Verify in browser using dev-browser skill

### US-002: School Story / About
**Description:** As a potential donor, I want to understand why Abernethy is special so I feel connected to the cause.

**Acceptance Criteria:**
- [ ] Covers: neighborhood school identity, 100-year history, values (Safe/Respectful/Fun), community stats
- [ ] Includes school photography -- not stock photos, real Abernethy life
- [ ] 501(c)(3) / tax-deductible status mentioned
- [ ] Scannable -- a skimmer gets the gist, a reader gets the depth
- [ ] Verify in browser using dev-browser skill

### US-003: Impact & Stats
**Description:** As a business sponsor, I want to see reach/engagement numbers so I can justify the sponsorship internally.

**Acceptance Criteria:**
- [ ] Key stats displayed prominently: 286 students, 2300 alumni, 21K community reach, 150+ volunteers, 100 years
- [ ] Stats feel dynamic/visual, not buried in a paragraph
- [ ] Context for what "community reach" means (newsletter, social, events, etc.)
- [ ] Verify in browser using dev-browser skill

### US-004: What the Money Funds
**Description:** As a donor, I want to know where my money goes so I trust this is worthwhile.

**Acceptance Criteria:**
- [ ] Clear list or visual of what the $100K funds (playground, tech, arts, teachers, etc.)
- [ ] Feels specific and tangible, not vague
- [ ] Optional: progress indicator or breakdown showing allocation
- [ ] Verify in browser using dev-browser skill

### US-005: Sponsorship / Giving Tiers
**Description:** As a business owner or major donor, I want to see sponsorship packages so I can pick the right level.

**Acceptance Criteria:**
- [ ] All tiers displayed: $50-249 (Advocate), $250-999 (Ally), $1K+ (Patron), and major giving ($2.5K-$10K, $10K-$50K, $100K)
- [ ] Each tier lists specific benefits (website listing, newsletter, social media, event naming, etc.)
- [ ] Visual hierarchy makes mid/upper tiers feel aspirational, not just more expensive
- [ ] Each tier has a CTA linking to the external donations platform
- [ ] Verify in browser using dev-browser skill

### US-006: Supporter Benefits Detail
**Description:** As a business considering sponsorship, I want to understand exactly what recognition I get so I can compare tiers.

**Acceptance Criteria:**
- [ ] Benefits are specific and concrete (not "recognition" but "logo on website + 4 newsletter mentions")
- [ ] Engagement stats where relevant (200K impressions, 15% engagement, 35% local staff)
- [ ] Clear escalation from tier to tier -- each level adds meaningfully
- [ ] Verify in browser using dev-browser skill

### US-007: Donate CTA / Conversion
**Description:** As a ready-to-give visitor, I want to donate quickly without friction.

**Acceptance Criteria:**
- [ ] Primary "Donate" / "Support" CTA appears in nav (persistent), hero, after tiers, and footer
- [ ] CTA links to external donations platform (URL configurable, easy to swap)
- [ ] Secondary CTA for "Contact us" (email or form) for sponsors who want to talk first
- [ ] Verify in browser using dev-browser skill

### US-008: Photo Gallery / Community Feel
**Description:** As a visitor, I want to see real photos of the school, kids, and events so the community feels tangible.

**Acceptance Criteria:**
- [ ] Minimum 10-15 photos throughout the page (not clustered in one spot)
- [ ] Photos integrated into section layouts, not a separate "gallery" section
- [ ] Mix of: school building, kids at events, classroom moments, community gatherings, centennial celebration
- [ ] Photos have proper aspect ratios and don't distort on any screen size
- [ ] Verify in browser using dev-browser skill

### US-009: Mobile Experience
**Description:** As a parent sharing the link in a group text, I want the site to look great on my phone.

**Acceptance Criteria:**
- [ ] Fully responsive -- no horizontal scroll on any section
- [ ] Donate CTA reachable with thumb (sticky nav or floating button)
- [ ] Photos scale gracefully, don't dominate small screens
- [ ] Text readable without pinch-zoom
- [ ] Page weight under 5MB on mobile (compressed images)
- [ ] Verify in browser using dev-browser skill

### US-010: Current Supporters / Social Proof
**Description:** As a potential donor, I want to see who has already given so I feel like I'm joining something, not starting it.

**Acceptance Criteria:**
- [ ] Section showing logos (businesses) and names (individuals) of current supporters
- [ ] Organized by tier so the hierarchy is visible
- [ ] Easy to update -- adding a new supporter should be a simple HTML edit
- [ ] Starts with placeholder/empty state that still looks intentional ("Be the first..." or similar)
- [ ] Verify in browser using dev-browser skill

### US-011: Campaign Urgency
**Description:** As a visitor, I want to know there's a deadline so I act now instead of bookmarking and forgetting.

**Acceptance Criteria:**
- [ ] July 1, 2026 deadline mentioned naturally (not a blinking countdown)
- [ ] Framing is positive ("Join us before July 2026") not anxiety-driven
- [ ] Verify in browser using dev-browser skill

### US-012: Architecture for Growth
**Description:** As the PTA web team, I want the site built so we can add pages later without a rewrite.

**Acceptance Criteria:**
- [ ] Clean component/section structure that can be split into routes
- [ ] Shared nav/footer ready for multi-page
- [ ] CSS organized so adding a page doesn't require refactoring styles
- [ ] Semantic HTML with logical section IDs for defined anchor links

## Functional Requirements

- FR-1: Single-page site with defined sections linked from nav
- FR-2: Fixed/sticky navigation with logo, section links, and primary donate CTA
- FR-3: All "Donate" / "Support" CTAs link to BetterWorld: `https://abernethyelementaryschool.betterworld.org/campaigns/general-pta-support` (stored in one JS variable for easy swap)
- FR-4: "Contact" CTA opens email (mailto:) or links to a contact form
- FR-11: Campaign deadline (July 1, 2026) displayed somewhere visible -- subtle urgency, not a countdown clock
- FR-12: "Current Supporters" section showing logos/names of businesses and donors who have already given (editable list, starts empty, grows over time)
- FR-5: Centennial logo (images/logo.png) used in nav and at least one content section
- FR-6: Photo placeholders clearly labeled by content needed, swappable via img src
- FR-7: Smooth scroll between sections via nav links
- FR-8: Responsive breakpoints: mobile (<768px), tablet (768-1024px), desktop (>1024px)
- FR-9: Semantic HTML throughout -- proper heading hierarchy, alt text, landmark elements
- FR-10: No JavaScript frameworks required for v1 -- vanilla HTML/CSS/JS, or lightweight tooling only

## Non-Goals

- No online payment processing -- all donations handled by external platform
- No user accounts, login, or donor dashboard
- No blog, news feed, or CMS
- No event calendar or RSVP system
- No donation progress tracker (may add later)
- No animations or scroll effects beyond CSS transitions
- No multilingual support for v1

## Design Considerations

- **Canva exports as content reference, not visual template.** The structure, copy, tiers, and stats come from the Canva files. Visual direction is open.
- **Photo-forward.** The site should feel like a yearbook or community newsletter, not a corporate donation page. Photos are the primary emotional driver.
- **Two audiences, one flow.** Businesses and families scroll the same page but hit different hooks -- stats/reach for sponsors, community/story for families. Don't silo them into separate tracks.
- **The logo is strong.** "Growing Strong Since 1925" tree logo is a great asset -- use it as a visual anchor, not just a nav element.
- **Avoid typical nonprofit site tropes.** No guilt-driven messaging, no thermometer progress bars, no "every dollar counts" cliches. Tone should be: proud, inviting, optimistic.
- **Fun but serious.** This is a real school with real kids. The design should feel like the best version of a neighborhood -- hand-painted signs on a well-built house. Warm, approachable, a little playful, but not childish or flimsy.
- **Kids and community are the stars.** Every design choice should center real people. Photos of kids, families, teachers, neighbors. The social fabric IS the pitch.
- **Urgency without anxiety.** July 1, 2026 deadline woven in naturally. "Join us by July 2026" not "ONLY X DAYS LEFT."

## Technical Considerations

- Static site -- no backend needed for v1
- Host anywhere (GitHub Pages, Netlify, Vercel, or school server)
- Images should be optimized (WebP with fallbacks, lazy loading)
- External donations URL stored in one place (variable or data attribute) for easy updates
- CSS custom properties for theming so design exploration is fast
- File structure ready for future static site generator migration if needed

## Success Metrics

- Visitor-to-donate-click rate > 10%
- Page load < 2s on 4G mobile connection
- Site shared organically by Abernethy families (trackable via UTM params on donate link)
- At least 3 business sponsors cite the website as part of their decision

## Resolved Questions

- **Donations platform:** BetterWorld -- https://abernethyelementaryschool.betterworld.org/campaigns/general-pta-support
- **Deadline:** July 1, 2026
- **Current supporters section:** Yes, include it
- **Brand direction:** Fun but serious. Kids and community social fabric are the focus. Not corporate.

## Open Questions

- Are there specific photos available, or do we need to request/shoot them?
- What's the contact email for sponsor inquiries?
- Who maintains the site after launch? (affects how easy edits need to be)
