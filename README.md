# ECS Training & Consultancy - Deployment Notes

Static marketing site for **ECS TRAINING & CONSULTANCY SDN. BHD.**

## Live Site
- **Custom Domain:** https://ecstraining.com.my
- **GitHub Pages:** https://elijahtingmk.github.io/ecs-training

## Deployment

This site is deployed via GitHub Pages from the `main` branch, root directory (`/`).

### Files
- `index.html` - Main website
- `styles.css` - Responsive stylesheet
- `CNAME` - Custom domain configuration

### DNS Configuration

Configure the following DNS records at your domain registrar (Cloudflare recommended):

#### For Apex Domain (ecstraining.com.my):
```
Type: A
Name: @
Value: 185.199.108.153
TTL: Auto

Type: A
Name: @
Value: 185.199.109.153
TTL: Auto

Type: A
Name: @
Value: 185.199.110.153
TTL: Auto

Type: A
Name: @
Value: 185.199.111.153
TTL: Auto
```

#### For WWW Subdomain:
```
Type: CNAME
Name: www
Value: elijahtingmk.github.io
TTL: Auto
```

### GitHub Pages Settings

1. Go to repository Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / `/ (root)`
4. Custom domain: `ecstraining.com.my`
5. Enforce HTTPS: ✓ (enable after DNS propagates)

### Verification

After DNS propagation (may take 24-48 hours):
- Check https://ecstraining.com.my loads correctly
- Verify HTTPS certificate is active
- Test www redirect: https://www.ecstraining.com.my

## Content

The site features:
- **Hero** with company positioning
- **Why PRisMA** benefits overview
- **Primary Program:** PRisMA Stage I LEO26 Screen (4-hour HRD Corp claimable course)
- **Earned Leadership™** secondary offering
- **Who We Serve** target audiences
- **Credentials** (DOSH PTP/ASV-053/26, HRD Corp Accredited Trainer)
- **Contact** section with email

### Brand Guidelines
- **Colors:** Cream (#FDF6E3) and Navy (#1C3144)
- **Email:** info@ecstraining.com.my
- **Legal Entity:** ECS TRAINING & CONSULTANCY SDN. BHD.
- **SSM:** 202601002650 (1664747-T)

## Development

Pure HTML/CSS static site. No build process required.

To preview locally:
```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

---

**Repository:** https://github.com/elijahtingmk/ecs-training
**Contact:** info@ecstraining.com.my
