# Ceros QA — Reuters Plus

A lightweight browser-based tool for validating Ceros campaign tracking against Reuters Plus naming conventions.

## What it checks

1. **Naming convention** — validates every event label against Brooke's naming standards (logo, video, quartile, article, CTA, link, scroll, social share/profile, carousel, navigation)
2. **Coverage** — detects interactive elements on the page and flags anything missing or undocumented
3. **Destination URLs** — extracts hotspot and inline hyperlink destinations from the Ceros experience JSON and surfaces anything that looks wrong
4. **Bugs** — flags hidden layers with URL interactions (common template remnants that can cause misfires if layers are later unhidden)

## How to use

1. Open the live campaign page
2. Right-click → **View Page Source** → Ctrl+A → Ctrl+C
3. Paste into the **Page Source** box
4. The JSON URL will auto-detect and appear as a link above the right box
5. Open that URL in a new tab → Ctrl+A → Ctrl+C → paste into the **Experience JSON** box
6. Click **Run QA Check**

The JSON step is optional but unlocks full URL validation, inline hyperlink detection, and bug checking.

## Naming conventions (Brooke's doc)

| Type | Format | Example |
|------|--------|---------|
| Logo | `[Brand]_Logo_Click` | `EY_Logo_Click` |
| Video | `[Brand]_[Title] Video` | `EY_AI Summit 2025 Video` |
| Video quartile | `[Brand]_[First3Words]_Video Start/25/50/75/100` | `EY_AISummit2025_Video 25` |
| Article | `[Brand]_[AssocVideo]_[ArticleName]Article#_Click` | `EY_AISummit_TenStepsArticle1_Click` |
| CTA | `[Brand]_CTA_[CTACopy]_Click` | `EY_CTA_LearnMore_Click` |
| Link | `[Brand]_Link_[LinkedWords]_Click` | `Google_Link_FindOutMore_Click` |
| Scroll | `[Brand]_Scroll 25/50/75/100` | `EY_Scroll 50` |
| Social share | `[Brand]_Social_[Platform]_Share_Click` | `EY_Social_LinkedIn_Share_Click` |
| Social profile | `[Brand]_Social_[Platform]_Profile_Click` | `EY_Social_LinkedIn_Profile_Click` |
| Carousel | `[Brand]_Carousel_Clicks` | `EY_Carousel_Clicks` |
| Navigation | `[Brand]_Navigation_[ButtonName]_Clicks` | `EY_Navigation_BackToHub_Clicks` |

## Deploy to GitHub Pages

1. Create a new repo (e.g. `ceros-qa`)
2. Upload `index.html`
3. Go to **Settings → Pages → Source → main branch → / (root)**
4. Your tool will be live at `https://[username].github.io/ceros-qa`

## Built by

Rose Patard, Customer Success & Analytics, Thomson Reuters EMEA
