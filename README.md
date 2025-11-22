# Viva Noir — Early Access Landing Page

A beautiful, mobile-friendly landing page for Viva Noir, an upcoming AI character companion. Built with vanilla HTML/CSS and integrated with Mailchimp for email collection.

## 🚀 Features

- **Responsive Design**: Mobile-friendly layout that works on all devices
- **Mailchimp Integration**: Seamless email collection with form validation
- **Modern UI**: Dark theme with gradient accents and glassmorphism effects
- **Fast Loading**: Lightweight vanilla HTML/CSS, no dependencies
- **Netlify Ready**: Pre-configured for easy deployment

## 📁 Project Structure

```
VivaNoir/
├── index.html          # Main landing page
├── thank-you.html      # Thank you page after signup
├── netlify.toml        # Netlify deployment configuration
├── README.md           # This file
└── .gitignore          # Git ignore file
```

## 🛠️ Setup Instructions

### 1. Update Mailchimp Form (If Needed)

The Mailchimp form is already configured with the provided URL:
```
https://gmail.us9.list-manage.com/subscribe/post?u=507638aa2da7f92c5090d4658&id=08d2914f85&f_id=00e151e1f0
```

**To update the Mailchimp form:**
1. Go to your Mailchimp dashboard
2. Navigate to your list → Signup forms → Embedded forms
3. Copy the form action URL
4. Update the `action` attribute in `index.html` (line ~47)

### 2. Update Social Media Links

Currently, social media links are placeholders (`#`). To update them:

**In `index.html` (around line 60):**
```html
<a href="YOUR_TIKTOK_URL" style="color:var(--muted);text-decoration:none">TikTok</a>
<a href="YOUR_YOUTUBE_URL" style="color:var(--muted);text-decoration:none">YouTube</a>
<a href="YOUR_OTHER_LINK" style="color:var(--muted);text-decoration:none">Link</a>
```

**In `thank-you.html` (around line 20):**
```html
<a href="YOUR_TIKTOK_URL" class="button">Follow on TikTok</a>
<a href="YOUR_YOUTUBE_URL" class="button">Subscribe on YouTube</a>
```

### 3. Customize Content

**Update text content:**
- Edit `index.html` to change descriptions, features, and copy
- Edit `thank-you.html` to customize the thank you message

**Update colors:**
- Modify CSS variables in the `<style>` section:
  ```css
  :root{
    --bg:#0f1724;
    --card:#0b1220;
    --accent:#ff6b6b;
    --muted:#9ca3af;
    --glass:rgba(255,255,255,0.03)
  }
  ```

## 📦 Deployment

### Deploy to Netlify

1. **Via GitHub:**
   - Push this repository to GitHub
   - Connect your GitHub account to Netlify
   - Select this repository
   - Netlify will auto-detect settings from `netlify.toml`
   - Click "Deploy site"

2. **Via Netlify CLI:**
   ```bash
   npm install -g netlify-cli
   netlify deploy --prod
   ```

3. **Via Drag & Drop:**
   - Go to [Netlify Drop](https://app.netlify.com/drop)
   - Drag the entire `VivaNoir` folder
   - Your site will be live instantly!

### Custom Domain

1. In Netlify dashboard, go to Site settings → Domain management
2. Add your custom domain
3. Follow DNS configuration instructions

## 🎨 Customization Guide

### Change Logo
Replace the logo div in `index.html`:
```html
<div class="logo">VN</div>
```
You can replace with an image:
```html
<div class="logo">
  <img src="logo.png" alt="Viva Noir" style="width:100%;height:100%;object-fit:cover;border-radius:12px">
</div>
```

### Update GIF on Thank You Page
Replace the GIF URL in `thank-you.html`:
```html
<img src="YOUR_GIF_URL" alt="Viva Noir Teaser" width="250">
```

### Modify Form Fields
Add or remove form fields in `index.html`:
- Add new input fields before the submit button
- Update Mailchimp form to include new fields
- Ensure field names match Mailchimp merge tags

## 📧 Mailchimp Configuration

### Form Fields
- `FNAME` - First name (optional)
- `EMAIL` - Email address (required)

### Adding More Fields
1. Add input field to HTML:
   ```html
   <label class="small">Field Name</label>
   <input type="text" name="MERGE_TAG" placeholder="Placeholder" />
   ```
2. Update Mailchimp form settings to include the merge tag
3. Update the form action URL if needed

## 🔧 Troubleshooting

### Form Not Submitting
- Check Mailchimp form URL is correct
- Verify form action URL matches your Mailchimp list
- Check browser console for errors

### Redirect Not Working
- Ensure `thank-you.html` is in the same directory
- Check JavaScript is enabled in browser
- Verify form submission is successful

### Styling Issues
- Clear browser cache
- Check CSS is properly loaded
- Verify media queries for mobile responsiveness

## 📱 Mobile Optimization

The site is fully responsive with:
- Flexible grid layout
- Touch-friendly buttons
- Readable font sizes
- Optimized spacing for small screens

## 🔒 Privacy & Compliance

- Form includes privacy notice
- Mailchimp handles GDPR compliance
- No cookies or tracking scripts (unless you add them)
- Email collection is opt-in only

## 📝 License

This project is open source and available for personal or commercial use.

## 🆘 Support

For questions or issues:
- Check Mailchimp documentation for form integration
- Review Netlify deployment logs
- Contact support through your email signup list

---

**Built with ❤️ for Viva Noir**

