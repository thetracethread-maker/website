# ThreadTrace - EU Digital Product Passports for Fashion & Textiles

Professional Jekyll website for ThreadTrace, a 100% EU-based Digital Product Passport solution specializing in fashion and textile industries.

## Project Overview

ThreadTrace provides GDPR-compliant, ESPR-ready Digital Product Passports exclusively on European infrastructure, eliminating the legal risks associated with US-based DPP providers.

## Technology Stack

- **Static Site Generator**: Jekyll 4.3.3
- **Styling**: Custom CSS with CSS variables
- **Fonts**: 
  - Instrument Serif (display)
  - DM Sans (body)
  - IBM Plex Mono (technical/data)
- **Hosting**: EU-only (recommended: Hetzner, OVH, or Netlify EU region)

## Directory Structure

```
threadtrace-jekyll/
├── _config.yml           # Site configuration
├── _layouts/
│   └── default.html      # Main layout template
├── _includes/
│   ├── header.html       # Navigation header
│   └── footer.html       # Site footer
├── assets/
│   └── css/
│       └── main.css      # All styling
├── index.md              # Homepage content
├── Gemfile               # Ruby dependencies
└── README.md             # This file
```

## Setup Instructions

### Prerequisites

- Ruby 3.0 or higher
- Bundler gem

### Local Development

1. **Install dependencies**:
   ```bash
   cd threadtrace-jekyll
   bundle install
   ```

2. **Run local server**:
   ```bash
   bundle exec jekyll serve
   ```

3. **View site**:
   Open browser to `http://localhost:4000`

### Build for Production

```bash
bundle exec jekyll build
```

Built site will be in `_site/` directory.

## Deployment Options (EU-Only)

### Recommended EU Hosting Providers

1. **Hetzner** (Germany)
   - Data centers in Nuremberg and Falkenstein
   - 100% EU-owned
   - Excellent performance and pricing

2. **OVH** (France)
   - Multiple EU data center locations
   - European company
   - Strong GDPR compliance

3. **Netlify** (EU Region)
   - Set deployment region to EU
   - Automatic HTTPS
   - Easy continuous deployment

### GitLab Pages (EU Hosted)

Create `.gitlab-ci.yml`:

```yaml
image: ruby:3.0

pages:
  stage: deploy
  script:
    - bundle install
    - bundle exec jekyll build -d public
  artifacts:
    paths:
      - public
  only:
    - main
```

## Customization

### Updating Company Information

Edit `_config.yml`:

```yaml
company:
  name: ThreadTrace B.V.
  location: Your City, Netherlands
  email: contact@threadtrace.eu
  data_centers:
    - Frankfurt, Germany
    - Dublin, Ireland
    - Amsterdam, Netherlands
```

### Color Scheme

Modify CSS variables in `assets/css/main.css`:

```css
:root {
    --color-primary: #0A4A8A;
    --color-eu-blue: #003399;
    --color-eu-gold: #FFCC00;
    /* ... */
}
```

### Adding Content

- Create new pages as `.md` files in root directory
- Add front matter:
  ```yaml
  ---
  layout: default
  title: Page Title
  ---
  ```

## Key Features

### EU Compliance Focus

- All content emphasizes 100% EU data residency
- Clear differentiation from US-based competitors
- Specific GDPR and ESPR compliance messaging

### Fashion Industry Specialization

- Textile-specific DPP features
- Supply chain traceability from fiber to garment
- Integration with fashion PLM/ERP systems

### Regulatory Timeline

- 2027 textile DPP mandate highlighted
- Implementation deadlines clearly communicated
- Urgency messaging for early adoption

## Performance Optimization

- Minimal dependencies (pure CSS, no JavaScript frameworks)
- Google Fonts preconnect for faster loading
- Optimized animations with CSS only
- Responsive design for all devices

## SEO Configuration

Jekyll SEO tag plugin included. Add to pages:

```yaml
---
title: Your Page Title
description: Your page description for search engines
---
```

## Legal Compliance

Website content emphasizes:
- GDPR (EU 2016/679) compliance
- ESPR (EU 2024/1781) readiness
- EU Strategy for Sustainable and Circular Textiles
- Data sovereignty under EU jurisdiction only

## Support

For questions about the website implementation, contact your development team.

For ThreadTrace product inquiries: {{ site.company.email }}

## License

© 2026 ThreadTrace B.V. All rights reserved.
