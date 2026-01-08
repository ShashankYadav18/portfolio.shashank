# EmailJS Setup Instructions

Follow these steps to set up EmailJS so your contact form sends messages directly to your email:

## Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

## Step 2: Add Email Service
1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail, Outlook, Yahoo, etc.)
4. Follow the instructions to connect your email account
5. **Copy the Service ID** (you'll need this later)

## Step 3: Create Email Template
1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template content:

```
Subject: New Message from Portfolio - {{subject}}

From: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your portfolio contact form.
```

4. **Copy the Template ID** (you'll need this later)

## Step 4: Get Your Public Key
1. Go to "Account" in your EmailJS dashboard
2. Find your **Public Key** (starts with "user_" or similar)
3. **Copy this key** (you'll need this later)

## Step 5: Update Your Portfolio
Open your `script.js` file and replace these placeholders:

1. Replace `'YOUR_PUBLIC_KEY'` with your actual public key
2. Replace `'YOUR_SERVICE_ID'` with your service ID from Step 2
3. Replace `'YOUR_TEMPLATE_ID'` with your template ID from Step 3

### Example:
```javascript
// Replace this:
emailjs.init('YOUR_PUBLIC_KEY');

// With your actual key:
emailjs.init('user_abc123xyz789');

// Replace this:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', formData)

// With your actual IDs:
emailjs.send('service_abc123', 'template_xyz789', formData)
```

## Step 6: Test Your Form
1. Save your changes
2. Open your portfolio in a browser
3. Fill out the contact form
4. Submit the form
5. Check your email for the message

## Free Plan Limits
- 200 emails per month
- No credit card required
- Perfect for portfolio contact forms

## Troubleshooting
- Make sure all IDs are correctly copied (no extra spaces)
- Check your browser console for error messages
- Verify your email service is properly connected in EmailJS dashboard
- Test with different email addresses

## Alternative: Formspree (Even Simpler)
If you prefer an even simpler solution, you can use Formspree:

1. Go to [https://formspree.io/](https://formspree.io/)
2. Create account and get your form endpoint
3. Replace the form action attribute with your Formspree endpoint

Let me know if you need help with the setup!