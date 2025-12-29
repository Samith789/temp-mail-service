# GitTempMail - Free Temporary Email Service

![GitTempMail Banner](https://img.shields.io/badge/GitTempMail-Free_Temporary_Email-green)
![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

A completely free temporary email service hosted on GitHub Pages. No registration, no limits, 100% open source.

## 🌐 Live Demo
Visit: `https://[your-username].github.io/temp-mail-service/`

## ✨ Features
- ✅ **Completely Free** - No costs, hosted on GitHub
- ✅ **No Registration** - Generate emails instantly
- ✅ **Multiple Domains** - Choose from various email domains
- ✅ **Real-time Inbox** - Check emails instantly
- ✅ **Mobile Responsive** - Works on all devices
- ✅ **Ad Spaces Ready** - Monetization ready
- ✅ **Open Source** - Full source code available

## 🚀 Quick Start

### Option 1: Use Directly
1. Visit the live demo link above
2. Click "Generate Free Email"
3. Copy the email address
4. Send test email from your Gmail/Outlook
5. Click "Check Inbox" to see emails

### Option 2: Deploy Your Own
1. **Fork this repository** (Click Fork button)
2. **Enable GitHub Pages**:
   - Go to Repository Settings
   - Click "Pages" in left sidebar
   - Select "main" branch as source
   - Click Save
3. **Your site is live!** Visit: `https://[your-username].github.io/temp-mail-service/`

## 🔧 Advanced Setup (Real Email Reception)

### Step 1: Get Free Email API
1. Sign up at [Mailgun](https://www.mailgun.com) (10k emails/month free)
2. Get your API Key and Sandbox Domain
3. Add to GitHub Secrets:
   - `MAILGUN_API_KEY`
   - `MAILGUN_DOMAIN`

### Step 2: Configure GitHub Actions
Create `.github/workflows/email-processor.yml`:

```yaml
name: Email Processor
on: [workflow_dispatch, schedule]
jobs:
  process-emails:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Process Emails
        run: |
          echo "Email processing would happen here"
          # Add your email processing script
