# JoyCraft Studio (Provisional Working Title)

An interactive concept prototype for a personalized digital birthday gifting platform built for young adults.

## Overview

JoyCraft Studio allows creators to build custom, interactive celebration websites filled with photo memories, spoken voice notes, personal letters, and celebratory animations (such as virtual candle blowing and confetti).

This repository currently hosts the **Stage 1.2 Prototype**:
- Complete responsive landing page.
- Interactive gift concept demo with a 5-module selector supporting full WAI-ARIA arrow-key navigation, responsive desktop presentation, and smooth mobile touch interaction.
- Feature showcases accurately distinguishing interactive samples, simulated concepts, and planned future studio capabilities.
- Transparent proposed pricing model (free creation & drafting; proposed ₹299 flat one-time publishing fee, subject to validation).
- Comprehensive FAQs and accessible modal dialogues.

## Current Project Status

- **Interactive Prototype Only:** The current codebase is a client-side concept demonstration.
- **Planned for Future Stages:**
  - Real gift builder and customizer studio.
  - Persistent media upload & cloud storage.
  - Actual audio recording and playback.
  - Database persistence & user accounts.
  - Payment gateway integration (for the proposed ₹299 publishing fee).
  - Production URL generation & delivery workflows.

## Technology Stack

- **Framework:** React 19 + TypeScript
- **Bundler & Dev Server:** Vite 8
- **Styling:** Tailwind CSS v4
- **Animation Utilities:** Motion (`motion/react`) & custom CSS keyframes
- **Icons:** Lucide React

## Project Architecture & Structure

```
├── src/
│   ├── components/
│   │   └── landing/
│   │       ├── Navbar.tsx             # Responsive header (mobile menu < lg, desktop links >= lg)
│   │       ├── Hero.tsx               # Value proposition & phone preview mockup
│   │       ├── InteractiveGiftDemo.tsx# Interactive sample gift with accessible WAI-ARIA tab navigation
│   │       ├── HowItWorks.tsx         # Architectural pillars & format comparison
│   │       ├── FeatureShowcase.tsx    # Modules categorized by interactive, simulated, & planned status
│   │       ├── WhoItsFor.tsx          # Relationship personas & tailor-fit recommendations
│   │       ├── ThreeStepProcess.tsx   # Planned create, preview, publish workflow
│   │       ├── PricingSection.tsx     # Transparent proposed pricing breakdown
│   │       ├── FaqSection.tsx         # Accessible accordion for visitor questions
│   │       ├── FinalCta.tsx           # Call-to-action wrap-up
│   │       ├── Footer.tsx             # Branding, site links, prototype disclaimer
│   │       └── StageNoticeModal.tsx   # Accessible focus-trapped dialog for builder CTAs
│   ├── config/
│   │   └── branding.ts                # Centralized brand tokens, pricing, and prototype notice
│   ├── types/
│   │   └── landing.ts                 # TypeScript interfaces for landing page data
│   ├── App.tsx                        # Main application container
│   ├── index.css                      # Tailwind v4 configuration, no-scrollbar, & celebratory animations
│   └── main.tsx                       # React DOM entry point
├── index.html                         # Document template with Google Fonts (Plus Jakarta Sans & Outfit)
├── metadata.json                      # AI Studio application metadata
├── package.json                       # Dependencies and build scripts
├── tsconfig.json                      # TypeScript configuration
└── vite.config.ts                     # Vite build configuration
```

## Local Development

To run the application locally:

```bash
# Install dependencies
npm install

# Start development server on port 3000
npm run dev

# Run TypeScript type check
npm run lint

# Build for production
npm run build
```

## Dependency Note

- **Google AI Studio Runtime Dependencies:** The manifest includes `@google/genai`, `express`, `dotenv`, and `tsx`. These packages are part of the Google AI Studio environment boilerplate for server-side capabilities and should be preserved. The current landing-page stage operates strictly on the client side without executing AI requests or requiring secret keys.
