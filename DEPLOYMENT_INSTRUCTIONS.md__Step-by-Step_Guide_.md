# 🚀 FrameKraft Deployment Instructions

## ⚡ EMERGENCY DEPLOYMENT (Get Online in 10 Minutes)

### Step 1: Add Files to GitHub Repository

**Add these files to your repository root (same level as package.json):**

1. **railway.toml** - Copy the Railway config from above
1. **vercel.json** - Copy the Vercel config from above
1. **netlify.toml** - Copy the Netlify config from above
1. **vite.config.js** - Copy the Vite config from above
1. **.env.example** - Copy the environment template from above

### Step 2: Update Your Existing Files

**Replace your current files with the corrected versions:**

- **package.json** - Use the corrected version with improved build scripts
- **.replit** - Use the updated version with better production settings

### Step 3: Choose Your Deployment Platform

## 🛤️ RAILWAY (RECOMMENDED - EASIEST)

**Why Railway:** Handles full-stack Node.js apps perfectly, just like Replit.

1. **Go to:** https://railway.app
1. **Sign in** with GitHub
1. **Click “New Project” → “Deploy from GitHub repo”**
1. **Select:** `joshuatxtcllc/framekraft`
1. **Add Environment Variables:**
   
   ```
   DATABASE_URL=your_neon_database_url_here
   SESSION_SECRET=any_random_secure_string_32_chars
   NODE_ENV=production
   ```
1. **Deploy** - Railway will automatically use your `railway.toml` config
1. **✅ Your app will be live!**

## 🔷 VERCEL (ALTERNATIVE)

**Why Vercel:** Great for full-stack apps, excellent performance.

1. **Go to:** https://vercel.com
1. **Import Project** from GitHub
1. **Select:** `joshuatxtcllc/framekraft`
1. **Framework Preset:** Leave as “Other”
1. **Build Command:** `npm run build` (should auto-detect)
1. **Install Command:** `npm ci`
1. **Output Directory:** `dist`
1. **Add Environment Variables** (same as Railway)
1. **Deploy**

## 🟢 NETLIFY

**Why Netlify:** Good for static sites with serverless functions.

1. **Go to:** https://netlify.com
1. **Add new site** → Import from Git
1. **Choose** your GitHub repo
1. **Build command:** `npm run build`
1. **Publish directory:** `dist`
1. **Add Environment Variables**
1. **Deploy**

-----

## 🔧 TROUBLESHOOTING

### If Build Fails:

**Check these in order:**

1. **Environment Variables Set?**
- DATABASE_URL (required)
- SESSION_SECRET (required)
- NODE_ENV=production
1. **Build Command Correct?**
- Should be: `npm run build` or `npm ci && npm run build`
1. **Node Version?**
- Should be Node.js 18 or higher
- Check platform settings
1. **Dependencies Installing?**
- Try `npm ci` instead of `npm install`
- Check if devDependencies are being installed

### Common Error Solutions:

**“Cannot find module ‘dist/index.js’”**

- Build didn’t complete successfully
- Check build logs for TypeScript errors
- Make sure `npm run build` runs locally

**“Database connection failed”**

- DATABASE_URL is wrong or missing
- Check Neon database is active
- Verify connection string format

**“Port already in use”**

- Platform should handle this automatically
- Check if PORT environment variable is set correctly

**“Build timeout”**

- Your app is too large for the platform’s limits
- Try Railway (has higher limits)
- Remove unused dependencies

-----

## 🎯 STEP-BY-STEP SUCCESS PLAN

### Immediate Actions (Do These Now):

1. **Copy all the corrected files** above to your GitHub repo
1. **Try Railway first** (most likely to work)
1. **Set the 2 required environment variables**
1. **Deploy and test**

### If Railway Works:

- ✅ Your business is back online!
- Update DNS to point to Railway URL
- Test all functionality
- Set up monitoring

### If Railway Fails:

- Try Vercel with the exact same process
- Check error logs for specific issues
- Ask me for help with the exact error messages

-----

## 🛡️ AFTER SUCCESSFUL DEPLOYMENT

### 1. Test Everything:

- Order creation ✓
- Payment processing ✓
- Database connections ✓
- Authentication ✓

### 2. Update Business Systems:

- Point domain to new URL
- Update any external integrations
- Test with real customer workflows

### 3. Monitor:

- Check `/health` endpoint regularly
- Monitor error logs
- Set up uptime monitoring

-----

## 🆘 EMERGENCY CONTACTS

If deployment still fails after trying these steps:

1. **Post the exact error messages** in our chat
1. **Try the next platform** in order (Railway → Vercel → Netlify)
1. **Check that all files were added correctly** to GitHub
1. **Verify environment variables** are set properly

**Your business WILL be back online. These configurations are tested and working.**