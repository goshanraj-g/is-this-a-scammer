# 📱 is-this-a-scammer 📱
Have you ever been waiting for an important call, only to answer and realize… it’s just one of those annoying scam calls? 🤦‍♂️
"is this a Scammer?" helps you identify scam callers instantly, so you never have to second-guess who's on the other end of the line

# How does it work?
### Number Validation & Metadata Extraction
- Check if the number is valid, and determine the carrier, country and type (landline, VoIP, mobile, etc...) APIs: Twilio Lookup API, NumVerify API
### Cross-Checking with Scam Databases
- Compare the number against government scam databases (FCC, Ofcom) and crowd-sourced databases (Hiya, Truecaller) APIs: Hiya API, Truecaller API, FCC / Ofcom Scam Reports
### Community-Driven Scam Reports
- Community can report scam numbers and provide details (ex. "123-456-7890: IRS Scam", "098-765-4321: Tech Support Scam") Note: There will need to be a validation/voting system
- Reports can be stored in PostgreSQL database and help flag suspicious numbers
### Frequency-Based Scam Detection
- We track how often a number is reported and flag it as high risk if reports spike
- Frequently searched numbers are cached using Redis for fast lookups
### AI-Based Scam Detection (Future Feature)
- Use a machine learning model to analyze scam call patterns, and detect potiential scams even before they're reported

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
