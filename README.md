# Rise Marketing Website

A static marketing website for Rise Financial Wellness platform, built with Tailwind CSS.

## Pages

1. **index.html** - Main landing page with Members/Institutions toggle
2. **about.html** - About page with mission, values, team, and impact

## Design System

### Colors (from Rise app)
- **rise-blue** `#364463` - Primary dark blue (buttons, text)
- **rise-brown** `#a37d64` - Secondary warm brown
- **rise-orange** `#e4905c` - Accent orange (gradients)
- **rise-gold** `#eac351` - Accent gold (gradients, highlights)
- **rise-cream** `#ece6e1` - Background neutral
- **rise-slate** `#3c454b` - Body text

### Typography
- Font Family: Nunito (Google Fonts)
- Rounded buttons: `rounded-2xl`

### Key Features
- **Members/Institutions Toggle** - Top navigation toggle switches all content between member-focused and institution-focused messaging
- **Mobile-first responsive design**
- **Warm gradient backgrounds** matching Rise app identity

## Placeholder Graphics Needed

### index.html

1. **Hero Illustration (Members)**
   - Description: Person using Rise app on phone, surrounded by floating icons (home, car, graduation cap, piggy bank)
   - Dimensions: 600x500px
   - Style: Warm, friendly, matches orange/gold palette

2. **Hero Illustration (Institutions)** 
   - Description: Dashboard mockup showing analytics, member engagement graphs
   - Dimensions: 600x500px
   - Style: Professional, data-driven

3. **User Avatars**
   - Description: 4 circular photos of diverse members
   - Dimensions: 40x40px each

4. **Testimonial Photos**
   - Description: 3 professional headshots (diverse)
   - Dimensions: 60x60px circular

5. **Credit Union Logos**
   - Description: 5-6 partner credit union logos
   - Dimensions: ~120px wide, grayscale

### about.html

1. **Team/Community Photo**
   - Description: Diverse group of coaches, members, credit union staff together
   - Dimensions: 600x450px
   - Style: Warm, inclusive, welcoming

2. **Team Member Headshots**
   - Description: 3 professional photos for team section
   - Dimensions: 200x200px circular

3. **Partnership Illustration**
   - Description: Credit union building with connected dots leading to happy members on devices
   - Dimensions: 500x400px
   - Style: Professional illustration, warm colors

## Running Locally

Simply open the HTML files in a browser - no build process required.

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Or just open directly
open index.html
```

## Technologies

- Tailwind CSS (via CDN)
- Google Fonts (Nunito)
- Vanilla JavaScript (for toggle functionality)
- No build process required
