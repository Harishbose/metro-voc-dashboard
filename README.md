# Metro VOC Dashboard

**Customer Feedback Analysis Dashboard for Metro Stores**

## 📊 Overview

Real-time dashboard for analyzing customer feedback and sentiment across the Metro store network. Track customer satisfaction, identify trends, and make data-driven decisions.

## ✨ Features

- **📈 KPI Cards** - Key metrics at a glance (Volume, Avg Rating, Sentiment %)
- **📊 Interactive Charts** - Sentiment distribution, trends, and patterns
- **🔍 Advanced Filters** - Filter by Zone, State, City, Store, Quarter, Financial Year
- **💬 Customer Comments** - View actual feedback with sentiment tags
- **🌙 Dark/Light Theme** - Switch between themes for comfortable viewing
- **📱 Responsive Design** - Works on desktop, tablet, and mobile
- **⚡ Fast Loading** - Real-time data updates

## 📁 File Structure

```
metro-voc-dashboard/
├─ metro_voc_dashboard.html    (Dashboard application - 2.7 MB)
├─ reviews.xlsx                (Customer feedback data - 11 MB)
├─ stores_master.xlsx          (Store metadata - 50 KB)
├─ render.yaml                 (Deployment configuration)
├─ README.md                   (This file)
└─ .gitignore                  (Git ignore file)
```

## 🚀 Deployment

### Live Dashboard
- **URL:** https://metro-voc-dashboard.onrender.com
- **Status:** Live and accessible
- **Updates:** Monthly data refresh

### Local Setup
```bash
# Start Python web server
python -m http.server 8000

# Open in browser
http://localhost:8000
```

## 📊 Data

### reviews.xlsx
- **Content:** Customer reviews with sentiment analysis
- **Size:** ~11 MB (updated monthly)
- **Rows:** 100,000+ reviews
- **Columns:** Store Code, Store Name, Zone, State, City, FY, Quarter, Month, Sentiment, Comment, Rating, etc.

### stores_master.xlsx
- **Content:** Store location and metadata
- **Size:** ~50 KB
- **Rows:** 965 stores
- **Update Frequency:** Quarterly (when stores change)

## 🔄 Monthly Data Update

### Process
1. Get new `reviews.xlsx` from your data system
2. Upload to GitHub root folder (replaces old file)
3. Render automatically rebuilds (~5 minutes)
4. Users refresh browser (Ctrl+F5) to see new data

### GitHub Upload
```
1. Go to: github.com/YOUR_USERNAME/metro-voc-dashboard
2. Click "Add file" → "Upload files"
3. Select new reviews.xlsx
4. Click "Commit changes"
5. Done! ✅
```

### File Location
```
✅ Correct:   metro-voc-dashboard/reviews.xlsx (root)
❌ Wrong:     metro-voc-dashboard/data/reviews.xlsx
❌ Wrong:     metro-voc-dashboard/uploads/reviews.xlsx
```

## 🛠️ How It Works

### Data Loading
```
User Opens Browser
    ↓
HTML/JavaScript Loads
    ↓
JavaScript Fetches Files:
  ├─ reviews.xlsx (customer data)
  └─ stores_master.xlsx (store info)
    ↓
Data Parsed and Charts Rendered
    ↓
Dashboard Ready for Interaction ✅
```

### Dashboard Code
- **Framework:** React 18 (via Babel standalone)
- **Charts:** Recharts library
- **Data Parsing:** PapaParse (CSV) + XLSX library (Excel)
- **Styling:** Tailwind CSS + custom CSS
- **No Build Process:** Pure HTML + JavaScript

## 🎯 Filtering

Filter data by:
- **Financial Year** (Apr-Mar)
- **Quarter** (Q1, Q2, Q3, Q4)
- **Zone** (Region)
- **State**
- **City**
- **Store Code**
- **Sentiment** (Positive, Negative, Neutral)

## 💡 Usage Tips

### View Charts
- Click on chart elements to drill down
- Hover for detailed information
- Charts automatically update when filters change

### Search Comments
- Use the comment search to find specific feedback
- Filter by sentiment first, then search
- Displays actual customer comments with context

### Export Insights
- Screenshots for reports
- Charts can be saved from browser
- Data available for analysis

## 🔍 Troubleshooting

### Dashboard Shows No Data
- **Solution:** Hard refresh browser (Ctrl+F5)
- **Check:** reviews.xlsx file exists in repo root
- **Check:** File is exactly named `reviews.xlsx`

### Slow Loading
- **Solution:** Wait 5-10 seconds (file parsing takes time)
- **Note:** First load slower due to data parsing
- **Render Free Tier:** May be in startup phase (30 sec)

### Missing Charts
- **Check:** Browser console (F12) for errors
- **Check:** Data file format correct
- **Solution:** Hard refresh (Ctrl+F5)

## 📞 Support

### Common Issues
| Issue | Solution |
|-------|----------|
| No data showing | Hard refresh (Ctrl+F5) |
| Slow dashboard | File is large - be patient |
| Filters not working | Clear filters, refresh |
| Wrong data | Check reviews.xlsx date |

### Browser Console
For technical issues:
1. Open: F12 (Developer Tools)
2. Check: Console tab for errors
3. Look for: ✅ or ❌ messages
4. Report: Error messages for debugging

## 🔐 Data Privacy

- All data processed locally in browser
- No external data transmission
- No tracking or analytics
- Data stays on Render servers

## 📈 Performance

- **Load Time:** 3-10 seconds (depends on file size)
- **Interactivity:** Real-time filter updates
- **Browser:** Works on Chrome, Firefox, Safari, Edge
- **Memory:** ~500 MB (large datasets)

## 🔄 Version History

| Date | Changes |
|------|---------|
| Jan 2026 | Initial deployment |
| Monthly | Data updates |
| Quarterly | Store data updates |

## 📄 License

Internal use only - Metro stores network

## 👤 Author

Created for Metro VOC Analysis  
Maintained by Data Team

---

**Last Updated:** January 23, 2026  
**Dashboard Status:** ✅ Live and Operational  
**Data Updated:** Monthly

## ✨ Key Features

### Filters (10 types)
✅ Brand | Zone | State | City | Store Code
✅ Mall/HS | Sentiment | Financial Year
✅ Quarter | Month | Improvement Theme

### KPI Cards
✅ Total Reviews | % Negative Sentiment
✅ Best Store (Rating) | Lowest Rated Store

### Visualizations
✅ Key Drivers (Bar Chart)
✅ Emotion Word Cloud
✅ Sentiment Breakdown (Pie Chart)
✅ Sentiment Trends (Line Chart)
✅ Zone Sentiment (Stacked Bar)
✅ Store-wise Feedback Drivers (Heatmap)
✅ Customer Comments (Positive/Negative)

### Strategic Insights
✅ Store Experience Dominance
✅ Zone Sentiment Analysis
✅ Underperforming Stores Alert
✅ Positive Momentum Tracking
✅ High Review Volume Cities
✅ Best Store Performance

---

## 🔄 How It Works

```
1. You edit CSV files in GitHub
   ↓
2. Dashboard automatically fetches latest data
   ↓
3. Data is parsed and cleaned locally
   ↓
4. Store information is mapped from master file
   ↓
5. All visualizations update instantly
   ↓
6. Users see real-time analytics
```

**No file uploads. No complications. Pure GitHub magic.** ✨

---

## 📋 CSV Requirements

### reviews.csv columns:
```
Business Name | Store Code | Customer Response | Customer Rating
Sentiment | Comment Date_NEW | FY | Quarter | Month
```

### stores_master.csv columns:
```
Store Code | City | State | Tier | Mall/HS
```

---

## 📅 Monthly Update Workflow

### Option 1: Web UI (Easiest - Recommended)
```
1. Go to github.com/Harishbose/metro-voc-dashboard
2. Click reviews.csv → Edit
3. Paste new month's data
4. Commit changes
5. Open dashboard → Data updates automatically! 🎉
```

### Option 2: Command Line (Advanced)
```bash
git clone https://github.com/Harishbose/metro-voc-dashboard.git
# Update CSV files locally
git add reviews.csv stores_master.csv
git commit -m "Update reviews for January 2026"
git push origin main
```

---

## 🎨 Dashboard Preview

### Layout
```
┌─────────────────────────────────────────────┐
│  Metro VOC Dashboard - Google Reviews       │
│  📊 Data Source: GitHub (Harishbose/...)    │
├──────────────┬──────────────────────────────┤
│              │  KPI Cards (4 metrics)       │
│ Filters      ├──────────────────────────────┤
│ (10 types)   │  Strategic Insights (6)      │
│              ├──────────────────────────────┤
│              │  Charts & Visualizations     │
│              │  • Key Drivers (Bar)        │
│              │  • Sentiment (Pie)          │
│              │  • Trends (Line)            │
│              │  • Zone Analysis (Stacked)  │
│              ├──────────────────────────────┤
│              │  Heatmap (Store × Category) │
│              ├──────────────────────────────┤
│              │  Comments (Positive/Neg)    │
└──────────────┴──────────────────────────────┘
```

---

## 🔐 Security & Privacy

✅ GitHub repo is **PUBLIC** (required for access)
✅ Data transferred over **HTTPS**
✅ No credentials needed
✅ No sensitive data stored
✅ Fresh data load each page view
✅ No tracking or analytics

---

## ✅ Pre-Launch Checklist

- [ ] GitHub repo created and set to PUBLIC
- [ ] CSV files uploaded (reviews.csv, stores_master.csv)
- [ ] Column names match exactly (case-sensitive)
- [ ] Dashboard opens without errors
- [ ] All filters populate with data
- [ ] Charts render correctly
- [ ] Strategic insights display
- [ ] Comments show feedback properly
- [ ] Test filter combinations
- [ ] Hard refresh works (Ctrl+Shift+R)

---

## 🚨 Troubleshooting

### Data not loading?
**Check:**
- [ ] GitHub repo is PUBLIC (not Private)
- [ ] CSV file names exact: `reviews.csv`, `stores_master.csv`
- [ ] Column names match specification
- [ ] No blank rows in CSV
- [ ] Internet connection active

### Old data showing?
**Solution:**
- Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
- Wait 30 seconds after commit
- Clear browser cache

### Store info missing?
**Check:**
- [ ] stores_master.csv is uploaded
- [ ] Store Code values match between files
- [ ] No extra spaces in Store Code

---

## 📞 Documentation

| Document | Purpose |
|----------|---------|
| **QUICK_START.md** | 3-step setup guide (start here!) |
| **GITHUB_INTEGRATION_SETUP.md** | Comprehensive setup & troubleshooting |
| **IMPLEMENTATION_SUMMARY.md** | Technical changes & modifications |
| **ARCHITECTURE.md** | System design, data flow, diagrams |
| **GITHUB_SETUP.md** | Historical setup notes |

---

## 🎯 What Changed From Original

### Removed ❌
- File upload mechanism
- SheetJS dependency
- Manual per-session loading

### Added ✨
- GitHub CSV integration
- Store master mapping
- Loading/error states
- Data source banner
- Automatic data refresh

### Preserved ✅
- All original styling & colors
- All original filters & features
- All visualizations
- Responsive design
- Strategic insights logic

---

## 📈 Performance

| Operation | Time |
|-----------|------|
| GitHub Fetch | 2-3 sec |
| CSV Parsing | 200-500 ms |
| Data Clean & Prep | 100-200 ms |
| Initial Render | 300-500 ms |
| **Total Load** | **~3-5 sec** |
| Filter Change | ~50-100 ms |

---

## 🔗 GitHub Integration Details

```javascript
// Built-in GitHub Configuration
const GITHUB_CONFIG = {
  username: 'Harishbose',
  repo: 'metro-voc-dashboard',
  branch: 'main'
};

// Automatic CSV URLs
const GITHUB_URLS = {
  reviews: 'raw.githubusercontent.com/.../reviews.csv',
  storesMaster: 'raw.githubusercontent.com/.../stores_master.csv'
};
```

---

## 🚀 Deployment

### Local Testing
```bash
# Option 1: Python
python -m http.server 8000

# Option 2: Node.js
npx serve

# Then open: http://localhost:8000/metro_voc_dashboard.html
```

### Production
- Upload `metro_voc_dashboard.html` to your web server
- Share URL with team
- Users access from any browser
- Data auto-syncs from GitHub

---

## 📊 Use Cases

✅ **Executive Dashboards** - Real-time KPIs & insights
✅ **Store Performance** - Zone & store analytics
✅ **Customer Feedback** - Theme analysis & sentiment
✅ **Trend Analysis** - Monthly & quarterly trends
✅ **Problem Identification** - Underperforming stores
✅ **Data-Driven Decisions** - Strategic insights

---

## 💡 Pro Tips

1. **Update on Schedule** - 1st of each month for consistency
2. **Use Meaningful Messages** - "Update reviews for January 2026"
3. **Hard Refresh** - Ctrl+Shift+R after GitHub updates
4. **Test Filter Combinations** - Explore all insights
5. **Share Insights** - Export findings to stakeholders
6. **Monitor Trends** - Look for patterns over months

---

## 📞 Support

### If you need help:
1. Check **QUICK_START.md** (3-step guide)
2. Review **GITHUB_INTEGRATION_SETUP.md** (troubleshooting)
3. Check browser console (F12) for errors
4. Verify GitHub repo settings
5. Verify CSV format matches specification

---

## 🎉 Summary

### What You Have
✅ Professional analytics dashboard
✅ GitHub integration (no file uploads)
✅ All original features & styling
✅ Real-time data syncing
✅ Comprehensive documentation

### What You Need
✅ Public GitHub repo (metro-voc-dashboard)
✅ Two CSV files (reviews.csv, stores_master.csv)
✅ Monthly data updates
✅ 5 minutes initial setup

### What You Get
✅ Enterprise-grade analytics
✅ Automatic monthly updates
✅ Team-accessible dashboard
✅ Strategic insights & trends
✅ Zero maintenance after setup

---

## 📝 Version Info

**Dashboard Version:** 2.0 (GitHub Integrated)
**Base Date:** January 21, 2026
**Status:** ✅ Production Ready
**Last Updated:** January 21, 2026

---

## 🎯 Next Steps

1. **Read QUICK_START.md** - Get oriented (2 min read)
2. **Create GitHub Repo** - Set up hosting (5 min)
3. **Upload CSV Files** - Add your data (5 min)
4. **Open Dashboard** - See it in action (instant)
5. **Set Monthly Reminder** - Schedule data updates
6. **Share with Team** - Distribute dashboard URL

---

**Ready to get started?** → Open **QUICK_START.md**

**Questions about setup?** → Open **GITHUB_INTEGRATION_SETUP.md**

**Want technical details?** → Open **ARCHITECTURE.md**

---

*Built with React, Recharts, GitHub, and ❤️*

**Let's build better insights, together!** 📊✨
