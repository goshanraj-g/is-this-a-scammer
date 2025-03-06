# 📱 is-this-a-scammer 📱
Have you ever been waiting for an important call, only to answer and realize… it’s just one of those annoying scam calls? 🤦‍♂️
is this a Scammer? helps you identify scam phone numbers instantly, so you never have to second-guess who's on the other end of the line

# How does it work?

# 🛠 Tech Stack
## Frontend
- React.js – Fast, modern UI
- Next.js – Server-side rendering (if needed)
- Tailwind CSS – Clean, responsive styling
## Backend
- Node.js + Express.js – Handles API requests & number lookups
- Python (FastAPI or Flask) (For AI-powered detection, optional)
## Database
- PostgreSQL – Stores scam reports and user submissions
- Redis (Optional, for caching frequently searched numbers)
## APIs & Data Sources
- Twilio Lookup API – Validates phone numbers and provides carrier details
- NumVerify API – Checks number validity and region
- Hiya API / Truecaller API – Accesses scam reports and caller IDs
- FCC / Ofcom Scam Databases – Uses government scam reports for verification
## Hosting & Deployment
Frontend: Vercel or Netlify
Backend: AWS Lambda, DigitalOcean, or Heroku
Database: Supabase (for PostgreSQL with authentication) or Firebase
