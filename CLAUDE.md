# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**HitungCat.com** is an Indonesian web application that helps homeowners and contractors calculate paint requirements for renovation projects. The app converts room dimensions into actionable shopping lists (Galon/Pail format) rather than abstract liter amounts.

**Current Status:** Pre-MVP (Planning & Specification phase - no code implementation yet)

## Tech Stack (Planned)

- **Frontend:** Next.js 14 with Tailwind CSS
- **Hosting:** Vercel
- **Database:** Supabase (PostgreSQL) - only if user accounts needed
- **Auth:** NextAuth.js or Supabase Auth (Google OAuth, WhatsApp OTP as priorities)
- **Analytics:** Plausible or Umami (privacy-friendly)

## Architecture Notes

### Core Calculator Logic
The MVP calculator takes:
- Room dimensions (Panjang × Lebar × Tinggi)
- Wall condition (baru/lama/lembab)
- Mode (Hemat: 5% buffer, Mandor: 15-20% buffer)

Output format uses Indonesian packaging standards:
- **Galon:** 2.5L / 5kg
- **Pail:** 20L / 25kg

### Key Design Decisions
- **Mobile-first:** 80% target traffic from mobile devices
- **Offline-capable:** PWA for areas with weak signal
- **SEO-focused:** Static generation for landing pages
- **Neutral positioning:** Not affiliated with any paint brand

## Development Principles

- Output shopping lists, not abstract numbers (actionable results)
- Validate paint coefficients through field research before implementation
- Indonesian localization: understand local wall conditions (acian, lembab, jamur)
- Target load time: <3 seconds on 4G

## Project Documentation

- `PRODUCT_VISION.md` - Full product strategy, personas, and roadmap
- `INTERVIEW_GUIDE.md` - Field research protocol for validating paint coefficients
- `FEATURE_VOTING.md` - User-driven feature prioritization system
- `question.csv` - Condensed interview questions template

## Next Steps Before Development

1. Complete field research (interview 3-5 contractors)
2. Finalize paint coverage coefficients
3. Create UI/UX wireframes
4. Define API contracts if backend needed
