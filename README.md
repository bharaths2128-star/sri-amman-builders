# Sir Amman Builders Website

A modern real estate website with admin dashboard for managing properties, projects, materials, and client reviews.

## 🚀 Features

- **Admin Dashboard**: Full CRUD operations for all content
- **Multiple Image Upload**: Up to 5 images per listing
- **Detail Pages**: Image galleries with carousel navigation
- **Inquiry System**: Cart-like system for collecting property inquiries
- **Responsive Design**: Works on all devices
- **Secure Authentication**: Supabase Auth integration

## 📋 Tech Stack

- **Frontend**: React + Vite, Tailwind CSS v4, Framer Motion
- **Backend**: Python FastAPI
- **Database**: Supabase (PostgreSQL)
- **Storage**: Supabase Storage
- **Auth**: Supabase Auth

## 🛠️ Local Development

### Prerequisites
- Node.js 18+ and npm
- Python 3.8+
- Supabase account

### Frontend Setup
```bash
cd frontend
npm install
cp .env.example .env
# Add your Supabase credentials to .env
npm run dev
```

### Backend Setup
```bash
cd backend
python -m venv venv
venv\Scripts\activate  # Windows
# or: source venv/bin/activate  # Mac/Linux
pip install -r requirements.txt
cp .env.example .env
# Add your Supabase credentials to .env
python -m uvicorn main:app --reload
```

## 🌐 Deployment

See [DEPLOYMENT.md](./DEPLOYMENT.md) for detailed deployment instructions.

### Quick Deploy to Vercel
1. Push code to GitHub
2. Import project on Vercel
3. Set root directory to `frontend`
4. Add environment variables
5. Deploy!

## 📁 Project Structure

```
sir-amman-builders/
├── frontend/               # React frontend
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── contexts/      # React contexts
│   │   ├── layouts/       # Layout components
│   │   └── lib/           # Utilities
│   ├── public/            # Static assets
│   └── vercel.json        # Vercel config
├── backend/               # FastAPI backend
│   ├── routers/           # API routes
│   └── main.py            # Entry point
└── DEPLOYMENT.md          # Deployment guide
```

## 🔑 Environment Variables

### Frontend (.env)
```
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key
```

### Backend (.env)
```
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_service_role_key
```

## 📝 Database Setup

1. Create tables using `supabase_schema.sql`
2. Run migration: `migration_multiple_images.sql`
3. Apply RLS policies: `fix_policies.sql`
4. Create storage bucket named `image`

## 🎨 Features Overview

### Admin Dashboard
- Manage land properties
- Manage houses (new/old)
- Manage projects
- Manage materials
- Manage reviews
- Edit contact information

### Public Website
- Browse properties with filters
- View detailed property pages
- Image gallery carousel
- Add properties to inquiry list
- Submit inquiries
- Leave reviews

## 📧 Contact

For questions or support, contact Sir Amman Builders.

## 📄 License

Proprietary - All rights reserved
#
