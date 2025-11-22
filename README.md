# study-buddy-platform
A collaborative study platform for students
📚 Study Buddy Platform
A collaborative study platform designed to help students connect, organize study sessions, share resources, and achieve their academic goals together.

🔗 Quick Links
Live Demo: [Loom Video]
Video Walkthrough: [Loom video]
🎯 Problem Statement
Students often struggle with:

Isolation - Studying alone can be demotivating and inefficient
Lack of Accountability - Without peers, it's easy to procrastinate
Resource Fragmentation - Study materials scattered across different platforms
Poor Time Management - Difficulty tracking study hours and maintaining consistency
Finding Study Partners - Hard to connect with peers studying the same subjects
The Solution
Study Buddy Platform brings students together in a centralized hub where they can form study groups, share knowledge, track progress, and stay motivated through peer collaboration.

👥 Target Users
Primary Audience
College & University Students - Looking for collaborative study environments
High School Students - Preparing for exams and seeking study partners
Online Learners - Remote students wanting to connect with peers
User Personas
Sarah, the Organized Planner - Wants to schedule study sessions and track her progress
Mike, the Group Leader - Enjoys creating study groups and helping others
Emma, the Resource Sharer - Loves sharing notes and learning materials with classmates
Alex, the Goal-Oriented - Needs accountability and wants to track study hours
✨ Key Features
🔐 Authentication System
User registration and login
Secure password reset functionality
Profile customization with bio and preferences
👨‍👩‍👧‍👦 Study Groups (Full CRUD)
Create study groups by subject or course
Browse and discover available study groups
Join/Leave groups based on interests
Update group details (admin privileges)
Delete groups when no longer needed
View group members and activity
⏱️ Study Session Tracking
Built-in study timer to track active sessions
Log study sessions with duration and notes
View study history and statistics
Calendar view of past and upcoming sessions
Calculate total study hours
📝 Notes & Resource Sharing
Upload and share study materials within groups
Organize notes by subject and topic
Search and filter shared resources
Bookmark useful materials
🎯 Goals & Progress
Set personal study goals (daily/weekly targets)
Track study streaks for consistency
Visual progress indicators and analytics
Achievement system to stay motivated
📊 Dashboard
Personalized overview of your study activity
Upcoming study sessions
Group notifications and updates
Quick access to all features
🛠️ Tech Stack
Frontend
React - UI component library
Tailwind CSS - Styling and responsive design
Lucide React - Icon system
Vibe Coding Tool - [Bolt.new / v0.dev / Replit]
Backend & Database
Supabase - Backend as a Service
PostgreSQL Database
Authentication
Row Level Security (RLS)
Real-time subscriptions
File Storage
Version Control
GitHub - Code repository and version control
Deployment
[Platform Name] - Production hosting
📁 Database Schema
Tables
profiles
├── id (UUID, Primary Key)
├── email (Text, Unique)
├── full_name (Text)
├── bio (Text)
├── major (Text)
├── profile_pic (Text)
└── created_at (Timestamp)

study_groups
├── id (UUID, Primary Key)
├── name (Text)
├── subject (Text)
├── description (Text)
├── max_members (Integer)
├── admin_id (UUID, Foreign Key → profiles)
└── created_at (Timestamp)

group_members
├── id (UUID, Primary Key)
├── group_id (UUID, Foreign Key → study_groups)
├── user_id (UUID, Foreign Key → profiles)
└── joined_at (Timestamp)

study_sessions
├── id (UUID, Primary Key)
├── group_id (UUID, Foreign Key → study_groups)
├── user_id (UUID, Foreign Key → profiles)
├── title (Text)
├── duration_minutes (Integer)
├── session_date (Date)
├── notes (Text)
└── created_at (Timestamp)

goals
├── id (UUID, Primary Key)
├── user_id (UUID, Foreign Key → profiles)
├── target_hours_weekly (Integer)
├── current_streak (Integer)
├── total_hours (Integer)
├── created_at (Timestamp)
└── updated_at (Timestamp)
🚀 Getting Started
Prerequisites
Node.js (v16 or higher)
Supabase account
GitHub account
Installation
Clone the repository
bash
git clone https://github.com/YOUR_USERNAME/study-buddy-platform.git
cd study-buddy-platform
Install dependencies
bash
npm install
Set up environment variables Create a .env file in the root directory:
env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
Run the development server
bash
npm run dev
Open http://localhost:5173 in your browser

🗓️ Development Timeline
Phase 1: Planning & Setup ✅
Phase 2: UI Design & Frontend 
Phase 3: Database Setup 
Phase 4: Backend Integration 
Phase 5: Testing & Polish 
Phase 6: Deployment & Documentation 
🎓 Project Context
This project was developed as part of the No Code Builders Lab course assignment, focusing on:

Fullstack application development
Database design and management
User authentication and authorization
CRUD operations implementation
Modern UI/UX principles
👨‍💻 Developer

Name: Chirag Verma
Email: tbm26chirag.verma@mastersunion.org
GitHub: 
📝 License
This project is licensed under the MIT License

🙏 Acknowledgments
No Code Builders Lab course instructors
Supabase for backend infrastructure
The open-source community
📞 Support
For questions or feedback, please open an issue in this repository or contact me at tbm26chirag.verma@mastersunion.org

⭐ If you find this project helpful, please give it a star!

