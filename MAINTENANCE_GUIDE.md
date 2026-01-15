# Goat Herd Tracker - Maintenance & Support Guide

## 📋 Overview

This guide covers ongoing maintenance, updates, troubleshooting, and support for the Goat Herd Tracker application.

---

## 🔄 Regular Maintenance Tasks

### Daily (Barn Use)
- ✅ Check app loads properly
- ✅ Add new goats/records as needed
- ✅ Quick visual check of recent entries

### Weekly
- ✅ **Export CSV backup** (most important!)
- ✅ Upload backup to Google Drive
- ✅ Review recent data entries
- ✅ Check for any errors/issues

### Monthly
- ✅ Full data export to Google Sheets
- ✅ Review herd analytics
- ✅ Check for browser updates
- ✅ Verify all features working
- ✅ Clean up old weight records if needed
- ✅ Archive old backups

### Annually
- ✅ Major data audit
- ✅ Archive previous year's sold goats
- ✅ Check for app updates
- ✅ Review and update documentation
- ✅ Train new users

---

## 💾 Backup Procedures

### Backup Strategy

**Critical:** Browser local storage can be cleared accidentally!

**Required Backups:**

1. **Weekly CSV Export**
   ```
   Frequency: Every Monday morning
   What: Full goat registry
   Where: Google Drive → Backups/2026/
   Filename: goat-backup-2026-01-15.csv
   ```

2. **Monthly Full Export**
   ```
   Frequency: Last day of month
   What: All data
   Where: Google Drive → Monthly Archives/
   Keep: Last 12 months
   ```

3. **Before Major Updates**
   ```
   When: Before updating app file
   What: Full export
   Where: Google Drive → Pre-Update Backups/
   Keep: Until verified working
   ```

### Backup Rotation

**Keep these backups:**
- All weekly backups for current month
- One backup per month for last 12 months
- One backup per year for previous years

**Delete:**
- Weekly backups older than 2 months
- Monthly backups older than 1 year (except annual)

---

## 🔧 Updating the Application

### When to Update

**Update when:**
- ✅ Bug fixes available
- ✅ New features needed
- ✅ Security updates released
- ✅ Performance improvements available

**Don't update during:**
- ❌ Kidding season (unless critical)
- ❌ Without backup
- ❌ Without testing first

### Update Process

**Step 1: Backup Data**
```
1. Export current data to CSV
2. Save with date: pre-update-2026-01-15.csv
3. Store safely
```

**Step 2: Test New Version**
```
1. Open new HTML file in different browser
2. Test all features
3. Verify mobile responsiveness
4. Check data import/export
```

**Step 3: Deploy Update**

**If using Vercel:**
```
1. Upload new index.html to GitHub
2. Vercel auto-deploys
3. Hard refresh: Ctrl+Shift+R
4. Verify working
```

**If using local file:**
```
1. Rename old file: goat_tracker_v1_backup.html
2. Replace with new file
3. Open in browser
4. Data should persist (same browser)
```

**Step 4: Verify**
```
1. Check all tabs load
2. Try adding test goat
3. Verify data from before update
4. Test on mobile
```

---

## 🐛 Common Issues & Solutions

### Issue 1: Data Disappeared

**Symptoms:**
- Open app and all goats are gone
- Empty registry

**Causes:**
- Cleared browser data
- Different browser/device
- Private/incognito mode

**Solutions:**

1. **Check browser:**
   - Using same browser as before?
   - Not in private/incognito mode?

2. **Restore from backup:**
   - Find latest CSV backup
   - Import data (future feature) OR
   - Manually re-enter critical data

3. **Prevention:**
   - Weekly CSV exports (critical!)
   - Use same browser consistently
   - Don't clear browser data
   - Bookmark the exact URL

---

### Issue 2: App Won't Load

**Symptoms:**
- Blank page
- Error message
- Partially loaded page

**Solutions:**

1. **Clear cache and reload:**
   ```
   Chrome/Edge: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
   Safari: Cmd+Option+R
   Firefox: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
   ```

2. **Check browser console:**
   ```
   Press F12 → Console tab
   Look for error messages
   Screenshot and report
   ```

3. **Try different browser:**
   - Test in Chrome
   - Test in Firefox
   - Test in Safari/Edge

4. **Check file integrity:**
   - File size should be ~150-200KB
   - Open in text editor to verify HTML
   - Re-download from source

---

### Issue 3: Photos Not Showing

**Symptoms:**
- Photo upload doesn't work
- Photos disappear after refresh

**Causes:**
- Photos too large (>2MB)
- Browser storage full
- Wrong file format

**Solutions:**

1. **Resize photos before upload:**
   - Use phone/computer to resize
   - Target: 500KB or less
   - Format: JPG or PNG

2. **Free up storage:**
   - Remove photos from old sold goats
   - Clear old weight records
   - Export data and start fresh

3. **Check format:**
   - Must be: JPG, JPEG, PNG, GIF, WEBP
   - Not: HEIC, BMP, TIFF

---

### Issue 4: Sorting Not Working

**Symptoms:**
- Click column header, nothing happens
- Wrong sort order

**Solutions:**

1. **Refresh page:** Ctrl+Shift+R
2. **Check if data loaded:** Scroll to see if goats are there
3. **Try different column:** Click different header
4. **Check browser:** Update to latest version

---

### Issue 5: Mobile Display Issues

**Symptoms:**
- Layout broken on phone
- Buttons cut off
- Can't scroll tables

**Solutions:**

1. **Use supported browser:**
   - Chrome (recommended)
   - Safari (iOS)
   - Firefox
   - Samsung Internet

2. **Check zoom level:**
   - Reset zoom to 100%
   - Don't pinch to zoom

3. **Rotate device:**
   - Portrait mode works best
   - Landscape for tables

4. **Clear mobile cache:**
   - Settings → Safari/Chrome → Clear History

---

### Issue 6: Can't Add Kidding Record

**Symptoms:**
- Form won't submit
- Tags show as duplicate
- Kids not added to registry

**Solutions:**

1. **Check tag uniqueness:**
   - Each kid needs unique tag
   - Check existing goats for duplicates
   - Use different tag format

2. **Fill required fields:**
   - Kidding date
   - Doe name
   - Kidding ease
   - All kid tag numbers

3. **Verify checkbox:**
   - "Auto-add kids" must be checked
   - Re-check if fields don't show

---

## 📊 Performance Optimization

### When App Gets Slow

**After 100+ goats:**
- Consider archiving sold goats
- Remove photos from culled animals
- Export and archive old data

**After 500+ goats:**
- Definitely archive old data
- Keep only active + recent year
- Store historical data in Google Sheets

### How to Archive

**Step 1: Export Everything**
```
1. Export to CSV
2. Save as: archive-2025-complete.csv
3. Import to Google Sheets for storage
```

**Step 2: Remove Old Data**
```
1. Delete sold goats from 2+ years ago
2. Delete deceased goats from 2+ years ago
3. Keep all active goats
4. Keep goats sold in last year
```

**Step 3: Document**
```
Note: "Archived 2020-2024 goats on 2026-01-15"
      "See Google Sheets: Grass & Grit Archive"
```

---

## 🔐 Security Best Practices

### Protecting Your Data

1. **Regular Backups** (most important!)
   - Weekly CSV exports
   - Store in multiple locations
   - Google Drive + local copy

2. **Access Control**
   - Use HTTPS (automatic with Vercel)
   - Don't share sensitive data publicly
   - Control who has deployment access

3. **Browser Security**
   - Keep browser updated
   - Use password on device
   - Don't use public computers for sensitive data

4. **Data Sanitization**
   - Don't include credit card info
   - Don't include SSNs or sensitive IDs
   - Be careful with sale prices if data is shared

---

## 📱 User Support

### Training New Users

**Basic Training (15 minutes):**
1. How to open the app
2. How to add a goat
3. How to search/filter
4. How to view goat details
5. Where to find help

**Advanced Training (30 minutes):**
6. Recording kidding events
7. Treatment records
8. Family tree navigation
9. Exporting data
10. Mobile usage

**Kidding Season Special (10 minutes):**
- Quick kidding record entry
- Adding color and weight
- Tagging system
- Common issues

### Quick Reference Card

Print and post in barn:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
     GOAT TRACKER QUICK GUIDE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🌐 Website: goats.yourfarm.com

📱 Add to Home Screen (Mobile):
   Safari: Share → Add to Home Screen

➕ Add New Goat:
   Goat Registry → + Add New Goat

🐐 Record Birth:
   Kidding History → + Add Kidding

💉 Record Treatment:
   Treatment Records → + Add Treatment

💾 BACKUP (Do Weekly!):
   Goat Registry → Export to CSV

❓ Problems? Check:
   1. Same browser as usual?
   2. Not in private mode?
   3. Try hard refresh (Ctrl+Shift+R)

📞 Tech Support: [Your Contact]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 📞 Getting Help

### Self-Help Resources

1. **Check this guide first**
2. **Try solutions above**
3. **Check browser console** (F12)
4. **Test in different browser**

### When to Contact Support

**Contact developer if:**
- Data corruption
- Security concerns
- Feature requests
- Critical bugs
- Custom modifications needed

**Provide this info:**
- Browser & version
- Device (desktop/mobile)
- Steps to reproduce issue
- Screenshots
- Console error messages (F12)

---

## 🔄 Update Log Template

Keep a log of all updates:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
         UPDATE LOG
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

2026-01-15 - v2.1
├─ Added: Color & weight in kidding records
├─ Fixed: Mobile layout issues
├─ Improved: Family tree display
└─ Backup: pre-update-2026-01-15.csv

2026-01-08 - v2.0
├─ Added: Treatment editing
├─ Added: Table sorting
├─ Improved: Mobile responsiveness
└─ Backup: pre-update-2026-01-08.csv

2025-12-20 - v1.5
├─ Added: Bulk treatment by gender
├─ Added: Complete family lineage
└─ Backup: pre-update-2025-12-20.csv
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## ✅ Maintenance Checklist

### Weekly Tasks
- [ ] Export CSV backup
- [ ] Upload to Google Drive
- [ ] Quick functionality test
- [ ] Check for issues

### Monthly Tasks
- [ ] Full data export
- [ ] Import to Google Sheets
- [ ] Review analytics
- [ ] Check browser updates
- [ ] Archive old backups

### Quarterly Tasks
- [ ] User feedback session
- [ ] Review performance
- [ ] Consider feature updates
- [ ] Audit data quality
- [ ] Update documentation

### Annual Tasks
- [ ] Major data archive
- [ ] Year-end reports
- [ ] Review all workflows
- [ ] Update training materials
- [ ] Plan improvements

---

## 📈 Performance Metrics

### Monitor These:

**Usage:**
- Number of goats in system
- Number of daily users
- Most used features
- Issue frequency

**Performance:**
- Page load time
- Data entry speed
- Search/filter responsiveness
- Mobile performance

**Data Health:**
- Backup frequency
- Data accuracy
- Missing required fields
- Duplicate records

---

## 🎯 Success Indicators

Your system is healthy when:

✅ Backups happening weekly
✅ Users trained and confident
✅ Issues resolved quickly
✅ Data accurate and complete
✅ Regular usage (not abandoned)
✅ Mobile usage working well
✅ Kidding season runs smoothly
✅ Reports generated easily

---

## 📄 Quick Command Reference

### Browser Console Commands

Check data in browser console (F12):

```javascript
// View all goats
console.log(JSON.parse(localStorage.getItem('goats')))

// Count goats
JSON.parse(localStorage.getItem('goats')).length

// Check storage size
console.log(new Blob([localStorage.getItem('goats')]).size + ' bytes')

// Clear all data (CAREFUL!)
// localStorage.clear()
```

---

## 🚨 Emergency Procedures

### Data Loss Emergency

**If all data is lost:**

1. **Don't panic**
2. **Don't clear cache again**
3. **Find latest backup CSV**
4. **Note date/time of loss**
5. **Contact support if needed**
6. **Document what happened**
7. **Implement better backup process**

### App Down Emergency

**If app won't load:**

1. **Check if Vercel is down:** status.vercel.com
2. **Try different browser/device**
3. **Use backup Google Drive file**
4. **Contact hosting support**
5. **Communicate with team**

---

**Remember:** Regular backups are your safety net! Export CSV weekly! 💾

**Questions?** See DEPLOYMENT_GUIDE.md or GOOGLE_DRIVE_SHEETS_GUIDE.md
