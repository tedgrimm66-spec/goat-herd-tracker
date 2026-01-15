# Goat Herd Tracker - Deployment Guide

## 📋 Overview

This guide covers how to deploy the Goat Herd Tracker application to various hosting platforms. The application is a single HTML file that runs entirely in the browser with no backend required.

---

## 🚀 Vercel Deployment (Recommended)

Vercel is the recommended hosting platform - it's free, fast, and easy to set up.

### Prerequisites
- GitHub account
- Vercel account (free at vercel.com)

### Step 1: Prepare Your Repository

1. **Create a new GitHub repository:**
   - Go to github.com
   - Click "New Repository"
   - Name it: `goat-herd-tracker`
   - Make it Public or Private (your choice)
   - Click "Create repository"

2. **Upload the file:**
   - Click "uploading an existing file"
   - Upload `goat_herd_tracker_enhanced_improved.html`
   - **IMPORTANT:** Rename it to `index.html` when uploading
   - Commit the file

### Step 2: Deploy to Vercel

1. **Connect Vercel to GitHub:**
   - Go to vercel.com
   - Sign up/login with GitHub
   - Click "Add New Project"
   - Click "Import Git Repository"
   - Select your `goat-herd-tracker` repository
   - Click "Import"

2. **Configure the Project:**
   - **Framework Preset:** Leave as "Other" or "Static"
   - **Root Directory:** Leave blank (use root)
   - **Build Command:** Leave blank (no build needed)
   - **Output Directory:** Leave blank
   - Click "Deploy"

3. **Wait for deployment:**
   - Vercel will deploy in ~30 seconds
   - You'll get a live URL like: `goat-herd-tracker.vercel.app`
   - Click "Visit" to see your live app!

### Step 3: Custom Domain (Optional)

1. Go to your project settings in Vercel
2. Click "Domains"
3. Add your custom domain (e.g., `goats.yourfarm.com`)
4. Follow Vercel's DNS configuration instructions

### Updating the App

**When you need to update:**
1. Upload new `index.html` to GitHub repository
2. Vercel automatically redeploys (in ~30 seconds)
3. Your live site updates automatically!

---

## 🔧 Alternative Hosting Options

### Option 2: Netlify

1. Sign up at netlify.com
2. Drag and drop `index.html` to Netlify
3. Rename to `index.html` if needed
4. Get instant live URL
5. Free SSL certificate included

**Updating:** Drag new file to same site to update

### Option 3: GitHub Pages

1. Create GitHub repository
2. Upload file as `index.html`
3. Go to Settings → Pages
4. Source: Deploy from main branch
5. URL: `yourusername.github.io/goat-herd-tracker`

**Updating:** Push new file to GitHub repository

### Option 4: Google Drive (Simple Sharing)

**Note:** Google Drive can share files but won't host them as a web app. See GOOGLE_DRIVE_SETUP.md for details.

1. Upload HTML file to Google Drive
2. Right-click → Get link → Anyone with link can view
3. Share link with team members
4. Users download and open locally

**Pros:** Easy, familiar interface
**Cons:** Not a live website, users need to download

### Option 5: Firebase Hosting

1. Install Firebase CLI: `npm install -g firebase-tools`
2. Create project at console.firebase.google.com
3. Initialize: `firebase init hosting`
4. Copy `index.html` to `public/` folder
5. Deploy: `firebase deploy`

**Best for:** Integration with other Firebase services

---

## 📊 Data Storage Considerations

### Important Notes:

1. **Browser Local Storage:**
   - Data is stored in each user's browser
   - Each user has their own separate data
   - Data is NOT synced between users or devices

2. **For Single User:**
   - Perfect as-is
   - Access from same device/browser
   - Regular CSV backups recommended

3. **For Multiple Users/Devices:**
   - Each browser has separate data
   - Use CSV export/import to share data
   - Or consider backend integration (see ADVANCED_SETUP.md)

---

## 🔐 Security Considerations

### Current Setup (Client-Side Only)

**✅ Safe for:**
- Personal use
- Farm internal use
- Non-sensitive data

**⚠️ Consider additional security if:**
- Data is highly sensitive
- Need user authentication
- Need audit logs
- Regulatory compliance required

### HTTPS

All recommended hosting platforms provide free HTTPS:
- ✅ Vercel: Automatic HTTPS
- ✅ Netlify: Automatic HTTPS
- ✅ GitHub Pages: Automatic HTTPS
- ✅ Firebase: Automatic HTTPS

---

## 📱 Mobile Access

Once deployed, users can access from any device:
- Desktop browsers
- Mobile phones (optimized!)
- Tablets

**Recommended:** Add to home screen on mobile devices:
- **iOS:** Safari → Share → Add to Home Screen
- **Android:** Chrome → Menu → Add to Home Screen

---

## 🔄 Backup Strategy

### Automatic Backups (Recommended)

Set up a backup routine:

1. **Weekly CSV Export:**
   - Export goat registry
   - Save with date: `goat-backup-2026-01-15.csv`
   - Store in cloud (Dropbox, Google Drive, etc.)

2. **Monthly Full Backup:**
   - Export all data
   - Keep 3 months of backups
   - Delete older backups

3. **Before Major Changes:**
   - Export data before updates
   - Test on separate browser first
   - Keep backup until verified working

---

## 🚨 Troubleshooting Deployment

### Issue: "Not Found" Error

**Solution:**
- Ensure file is named `index.html`
- Check it's in root directory
- Verify deployment succeeded

### Issue: Changes Not Showing

**Solution:**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache
- Wait a few minutes for deployment

### Issue: Data Lost After Update

**Solution:**
- Browser local storage is separate from the HTML file
- Data should persist through updates
- If lost, restore from CSV backup

### Issue: Can't Access on Mobile

**Solution:**
- Ensure using HTTPS (not HTTP)
- Try different mobile browser
- Check mobile data/WiFi connection

---

## 📞 Support Resources

### Vercel Support
- Docs: vercel.com/docs
- Community: github.com/vercel/vercel/discussions

### Netlify Support
- Docs: docs.netlify.com
- Community: answers.netlify.com

### GitHub Pages Support
- Docs: docs.github.com/pages

---

## ✅ Deployment Checklist

Before going live:

- [ ] File renamed to `index.html`
- [ ] Deployed successfully
- [ ] Can access via URL
- [ ] Works on mobile
- [ ] HTTPS is enabled
- [ ] Tested adding/editing/deleting goats
- [ ] Tested on multiple browsers
- [ ] Backup system established
- [ ] Team members can access
- [ ] Custom domain configured (if desired)

---

## 🎯 Recommended Setup for Grass and Grit Farms

**For Your Farm:**

1. **Primary:** Vercel deployment
   - Free
   - Fast
   - Auto-updates from GitHub
   - Custom domain: `goats.grassandgrit.farm`

2. **Backup:** Keep file in Google Drive
   - Easy team access
   - Download for offline use

3. **Data:** Regular CSV exports to Google Drive
   - Weekly automatic reminder
   - Backup folder in Drive

4. **Mobile:** Add to home screen on barn phone/tablet
   - Quick access during kidding season
   - Works offline once loaded

---

## 📄 File Structure for Deployment

```
your-repository/
├── index.html                           (the main app file)
├── README.md                            (optional - project description)
└── backups/                             (optional - store CSV backups)
    ├── goat-backup-2026-01-15.csv
    └── goat-backup-2026-01-08.csv
```

---

## 🔄 Version Control Best Practices

### When Updating the App:

1. **Keep version history in GitHub:**
   ```
   git add index.html
   git commit -m "Added color and weight tracking for kids"
   git push
   ```

2. **Tag major versions:**
   ```
   git tag -a v2.0 -m "Version 2.0 - Enhanced kidding records"
   git push origin v2.0
   ```

3. **Create branches for testing:**
   ```
   git checkout -b testing-new-feature
   # Test changes
   git checkout main
   git merge testing-new-feature
   ```

---

## 📈 Monitoring & Analytics (Optional)

### Add Google Analytics (Optional):

Add before `</head>` in index.html:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

**Tracks:**
- Number of users
- Most used features
- Device types
- Usage patterns

---

## 🎓 Next Steps

After deployment:

1. **Test thoroughly** - Add test goats, try all features
2. **Train users** - Show team how to access and use
3. **Set up backups** - Schedule weekly exports
4. **Monitor usage** - Check if app is working well
5. **Gather feedback** - Improve based on user needs

---

**Questions?** See TROUBLESHOOTING.md or contact your deployment specialist.

**Ready to deploy?** Start with Vercel - it's the easiest and fastest option!
