# Testing Guide for Kehan Dong Chronicle

## Quick Start

### Local Testing
```bash
# Start a local web server
python -m http.server 8000

# Or use Python 3 explicitly
python3 -m http.server 8000

# Then visit in your browser:
# http://localhost:8000
```

## What to Test

### 1. Hero Section
- [ ] Title shows "Kehan Dong"
- [ ] Lede text mentions "Angel investor, educator, and founder"
- [ ] Chips show: Angel Investor, Inner Journey Founder, Code of Love NGO, Duke Kunshan University, Startup Go Camp
- [ ] Stats show: "1000+ lives transformed", "90.4/100 student rating", "Investor → Educator → Founder"

### 2. Chapter Navigation
- [ ] Phase rail shows 6 chapters
- [ ] Chapters load correctly:
  - Formation (Early Education)
  - Inner Journey
  - Code of Love
  - Investing (Angel Investing)
  - Duke Kunshan (SGC)
  - Present (Current Focus)

### 3. Map Functionality
- [ ] Map loads correctly
- [ ] Shows 3 locations:
  - China (early formation)
  - Kunshan, Jiangsu (Duke Kunshan University)
  - Global (distributed)
- [ ] Clicking chapters updates map location
- [ ] Map markers appear correctly

### 4. Timeline
- [ ] Timeline events load
- [ ] Events show correct dates and descriptions
- [ ] Filtering by chapter works
- [ ] Source links are functional

### 5. Sources Section
- [ ] 3 sources appear:
  - kehandong.com
  - Duke Kunshan University Article
  - Inner Journey Website
- [ ] Source links open correctly
- [ ] Source metadata displays properly

### 6. Deep Mode
- [ ] Toggle between Skim and Deep mode works
- [ ] Deep mode shows additional content:
  - Deep briefs
  - Exhibits
  - Archive timeline
  - Source explorer

### 7. Exhibits
- [ ] 3 exhibits load:
  - SGC Educational Impact
  - Founder Philosophy
  - Inner Journey Transformational Work
- [ ] Exhibit cards display correctly
- [ ] Source links work

### 8. Validation Section
- [ ] Shows 3 validation groups:
  - Educational excellence (90.4/100)
  - Inner Journey impact (1000+ lives)
  - Institutional partnerships (DKU)

### 9. Present Direction
- [ ] Shows current focus
- [ ] Lists 4 signals
- [ ] Shows next moves
- [ ] Source links work

### 10. Mobile Responsiveness
- [ ] Test on mobile viewport
- [ ] Navigation works on small screens
- [ ] Map is usable on mobile
- [ ] Text is readable

## Common Issues to Check

### Map Not Loading
- Check browser console for errors
- Verify MapLibre GL JS is loading
- Check that location coordinates are valid

### Timeline Not Showing
- Verify timeline.json is valid JSON
- Check that TimelineJS library is loading
- Look for JavaScript errors in console

### Chapters Not Appearing
- Verify chapters.json is valid JSON
- Check that chapter IDs match between files
- Ensure locationIds reference valid locations

### Sources Not Linking
- Verify URLs in sources.json are correct
- Check that sourceIds match between files
- Test external links manually

## Browser Console Checks

Open browser developer tools (F12) and check:
- [ ] No JavaScript errors
- [ ] All JSON files load successfully
- [ ] Map tiles load correctly
- [ ] No 404 errors for resources

## Data Validation

All JSON files have been validated. If you make changes, validate with:
```bash
python3 -m json.tool data/[filename].json
```

## Expected Behavior

### On Page Load
1. Hero section appears with Kehan Dong information
2. Map initializes showing global view
3. Chapter navigation rail appears
4. Timeline begins loading
5. Skim mode is active by default

### On Chapter Click
1. Page scrolls to chapter
2. Map updates to show chapter location
3. Chapter card highlights in compass
4. Timeline filters to chapter events (if in deep mode)

### On Mode Toggle
1. Skim mode: Shows narrative chapters, map, validation
2. Deep mode: Adds deep briefs, exhibits, archive timeline, source explorer

## Performance Notes
- Initial load may take a few seconds for map tiles
- Timeline rendering may be slower with many events
- Deep mode loads additional content on demand

## Known Limitations
- Limited historical data (shorter career span than original)
- Some chapters have minimal evidence (Code of Love NGO)
- No video or audio content currently
- Map has fewer locations than original chronicle

## Success Criteria
✓ All sections load without errors
✓ Navigation works smoothly
✓ Map displays correctly
✓ Sources are accessible
✓ Content is accurate and well-formatted
✓ Mobile experience is functional

---

*Testing guide created: March 18, 2026*
