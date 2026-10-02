# Alffi Website

Marketing website for the Alffi iOS app (formerly Farmers Friend).

## Structure

```
Website/
├── index.html          # Home page
├── features.html       # Features detail page
├── pricing.html        # Pricing page
├── support.html        # Support/Help page
├── css/
│   └── styles.css      # Main stylesheet
├── js/
│   └── main.js         # JavaScript (mobile nav, smooth scroll)
└── images/
    ├── app-icon.png    # App icon (1024x1024)
    └── favicon.png     # Favicon
```

## Local Preview

To preview the website locally, you can use Python's built-in server:

```bash
cd Website
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Deployment Options

### Option 1: GitHub Pages (Recommended - Free)

1. **Create a GitHub repository:**
   ```bash
   cd Website
   git init
   git add .
   git commit -m "Initial website commit"
   ```

2. **Push to GitHub:**
   - Create a new repository on GitHub (e.g., `farmersfriend-website`)
   - Push your code:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/farmersfriend-website.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: / (root)
   - Click Save

4. **Connect your domain:**
   - In GitHub Pages settings, add custom domain: `farmersfriendapp.com`
   - At your domain registrar, add DNS records:
     - **A records** pointing to GitHub's IPs:
       - 185.199.108.153
       - 185.199.109.153
       - 185.199.110.153
       - 185.199.111.153
     - **CNAME record** for `www` pointing to `YOUR_USERNAME.github.io`

### Option 2: Netlify (Free tier)

1. **Sign up at netlify.com**

2. **Deploy:**
   - Drag and drop the Website folder to Netlify dashboard
   - OR connect to GitHub repository

3. **Connect domain:**
   - Go to Domain settings in Netlify
   - Add custom domain: farmersfriendapp.com
   - Follow Netlify's DNS instructions

### Option 3: Traditional Web Hosting

If you have existing web hosting:

1. **Upload files via FTP/SFTP**
2. **Point domain to hosting** via your registrar's DNS settings
3. **Upload the entire Website folder contents** to your public_html or www folder

## Customisation

### Update Pricing
Edit `pricing.html` to adjust pricing tiers. The current pricing is placeholder - update with your actual App Store subscription prices.

### Update App Store Link
In all HTML files, search for `https://apps.apple.com/app/farmers-friend` and replace with your actual App Store URL once the app is published.

### Contact Form
The contact form in `support.html` uses Formspree. To activate:
1. Sign up at formspree.io
2. Create a new form
3. Replace `YOUR_FORM_ID` in the form action with your actual form ID

### Add Screenshots
To add app screenshots:
1. Export screenshots from Xcode or your device
2. Add to `images/` folder
3. Reference in HTML with appropriate alt text

### Brand Colors
The primary brand color is defined in `css/styles.css`:
```css
:root {
    --color-primary: #217029;  /* Your green from the app */
}
```

## SSL Certificate

Both GitHub Pages and Netlify provide free SSL certificates automatically. Your site will be accessible via HTTPS.

## Future Improvements

Consider adding:
- [ ] Privacy Policy page (`privacy.html`)
- [ ] Terms of Service page (`terms.html`)
- [ ] App screenshots gallery
- [ ] Video demo
- [ ] Blog section for farm tips
- [ ] Customer testimonials

## Support

For website issues, contact: support@farmersfriendapp.com
