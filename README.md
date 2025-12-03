# 📚 Book Lover - Modern Storytelling Platform

> A mobile-first web platform for immersive storytelling that combines the best of Medium, Wattpad, and modern book reading apps.

[![Live Demo](https://img.shields.io/badge/demo-live-success)](your-demo-url-here)
[![Next.js](https://img.shields.io/badge/Next.js-15-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-blue)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

[Live Demo](your-demo-url-here) • [Features](#features) • [Tech Stack](#tech-stack) • [Screenshots](#screenshots)

---

## 🌟 Overview

**Book Lover** is a modern, full-stack storytelling platform designed for both readers and authors. It provides a distraction-free reading experience with rich social features, content moderation tools, and comprehensive analytics.

### Why Book Lover?

- **For Readers**: Discover engaging stories, track your reading progress, build your reading list, and engage with authors through comments and likes
- **For Authors**: Publish stories with a powerful rich-text editor, track engagement analytics, manage your content, and grow your audience
- **For Admins**: Comprehensive moderation tools, user management, content oversight, and platform analytics

---

## ✨ Features

### 🎯 Core Features

#### Reading Experience
- **Distraction-Free Reading**: Full-screen, book-like reading interface
- **Progress Tracking**: Automatic progress saving with percentage completion
- **Reading List**: Save stories to read later (wishlist functionality)
- **Smart Analytics**: Track reading time and engagement

#### Author Tools
- **Rich Text Editor**: Powered by TipTap with Markdown support
- **Story Management**: Create, edit, publish, and archive stories
- **Visibility Controls**: Public, private, or password-protected stories
- **Status Management**: Draft, scheduled, published, or archived
- **Analytics Dashboard**: View counts, unique readers, engagement trends

#### Social Features
- **Engagement System**: Like/unlike stories
- **Comment Threads**: Nested comments with reply functionality
- **User Profiles**: Customizable bios and profile pictures
- **Author Discovery**: Explore stories by different authors

#### Admin Dashboard
- **User Management**: Role assignment, suspension controls
- **Content Moderation**: Story and comment moderation
- **Report System**: Handle user-generated reports
- **Platform Analytics**: Engagement metrics and trend visualization

### 🔐 Authentication & Security
- Google OAuth integration via NextAuth.js
- Role-based access control (Admin, Author, Reader)
- Secure password hashing with bcryptjs
- Session management and token verification

### 🎨 User Experience
- **Dark Mode Support**: Seamless light/dark theme switching
- **Responsive Design**: Mobile-first, works on all devices
- **Accessible UI**: Built with Radix UI primitives
- **Error Handling**: Comprehensive error boundaries and user feedback
- **Loading States**: Smooth transitions and loading indicators

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 15 (App Router) with React 19
- **Styling**: Tailwind CSS 4.1
- **UI Components**: shadcn/ui (Radix UI)
- **Rich Text Editor**: TipTap
- **State Management**: React Query (@tanstack/react-query)
- **Theme**: next-themes for dark mode
- **Icons**: Lucide React
- **Charts**: Recharts

### Backend
- **API**: tRPC for type-safe APIs
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: NextAuth.js v5
- **File Storage**: Vercel Blob
- **Analytics**: Vercel Analytics
- **Validation**: Zod schemas

### Developer Tools
- **Language**: TypeScript 5.9
- **Linting**: ESLint 9
- **Formatting**: Prettier 3.5
- **Package Manager**: pnpm 10.20
- **Database Migrations**: Drizzle Kit

---

## 📸 Screenshots

### Landing Page
![Landing Page](screenshots/landing.png)
*Hero section with featured stories carousel*

### Story Discovery
![Discover Stories](screenshots/discover.png)
*Browse and search through published stories*

### Reading Experience
![Reading View](screenshots/reading.png)
*Distraction-free reading interface with progress tracking*

### Dashboard
![User Dashboard](screenshots/dashboard.png)
*Personalized dashboard with analytics and story management*

### Story Editor
![Story Editor](screenshots/editor.png)
*Rich text editor with formatting options*

### Admin Panel
![Admin Dashboard](screenshots/admin.png)
*Comprehensive admin tools for content moderation*

---

## 🏗️ Architecture

### Database Schema

```
Users → Stories (one-to-many)
Users → Story Likes (many-to-many)
Users → Comments (one-to-many)
Users → Reading Progress (one-to-many)
Users → Wishlist (many-to-many)
Stories → Comments (one-to-many)
Stories → Visits (one-to-many)
```

### Key Tables
- **users**: User accounts with roles and profile information
- **stories**: Published and draft stories with rich content
- **story_comments**: Threaded comment system
- **story_likes**: User engagement tracking
- **story_wishlists**: Reading list management
- **reader_progress**: Reading position tracking
- **story_visits**: Analytics and view tracking
- **reports**: Content moderation system

### API Structure (tRPC)
- **Story Router**: CRUD operations, likes, comments, views
- **User Router**: Profile management, dashboard stats
- **Admin Router**: User management, content moderation
- **Analytics Router**: Engagement metrics and trends

---

## 🚀 Key Features Breakdown

### For Readers
- Discover stories through browse and search
- Read stories in a clean, distraction-free interface
- Track reading progress across multiple stories
- Like stories and leave comments
- Build a personal reading list
- View author profiles

### For Authors
- Create stories with a powerful rich-text editor
- Manage story visibility (public/private/password-protected)
- Schedule story publication
- View detailed analytics:
  - Total views and unique readers
  - Engagement trends over time
  - Comment activity
- Edit and update published stories
- Archive or delete old content

### For Administrators
- Manage users (view, suspend, change roles)
- Moderate stories and comments
- Review and resolve reports
- View platform-wide engagement metrics
- Track user activity and trends
- Handle suspended accounts with expiration dates

---

## 🎯 Use Cases

1. **Independent Authors**: Publish your stories and build an audience without traditional publishing barriers
2. **Reading Communities**: Create and discover content in a social, engaging environment
3. **Educational Content**: Share educational stories with progress tracking for students
4. **Creative Writing**: Get feedback on your work through comments and engagement metrics
5. **Content Curation**: Build collections of your favorite stories with the reading list feature

---

## 🔒 Security Features

- OAuth 2.0 authentication via Google
- Role-based access control (RBAC)
- Secure password hashing
- Protected API routes with authentication middleware
- Content moderation and reporting system
- User suspension capabilities
- Input validation with Zod schemas
- SQL injection prevention via Drizzle ORM
- XSS protection through React's built-in escaping

---

## 📊 Analytics & Insights

### User Analytics
- Reading history and progress
- Liked stories overview
- Reading list management
- Personal engagement metrics

### Author Analytics
- Story view counts
- Unique reader tracking
- Engagement trends over time
- Comment activity per story
- Reading completion rates

### Admin Analytics
- Platform-wide engagement metrics
- User growth and activity trends
- Content moderation statistics
- Report resolution tracking

---

## 🎨 Design Principles

1. **Mobile-First**: Designed for mobile devices, enhanced for desktop
2. **Accessibility**: Built with semantic HTML and ARIA attributes
3. **Performance**: Optimized images, code splitting, and lazy loading
4. **User Experience**: Intuitive navigation and clear feedback
5. **Consistency**: Unified design language across all pages
6. **Dark Mode**: Full dark mode support for comfortable reading

---

## 🌐 Deployment

The application is deployed on Vercel with:
- Serverless functions for API routes
- PostgreSQL database (Vercel Postgres or similar)
- Vercel Blob for image storage
- Automatic deployments from the main branch
- Environment variable management
- Preview deployments for pull requests

---

## 📝 Future Enhancements

- [ ] Advanced search with filters (genre, tags, popularity)
- [ ] Story categories and tag system
- [ ] Following/follower relationships
- [ ] Real-time notifications
- [ ] Story recommendation engine
- [ ] Author statistics dashboard refinement
- [ ] Export stories to PDF/EPUB
- [ ] Social media sharing integrations
- [ ] Multi-language support
- [ ] Story collaboration features

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 🤝 Contact

For inquiries about this project:

- **Live Demo**: [your-demo-url-here]
- **Email**: your-email@example.com
- **LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- **Portfolio**: [your-portfolio-url.com](https://your-portfolio-url.com)

---

## 🙏 Acknowledgments

Built with modern web technologies and best practices:
- [Next.js](https://nextjs.org/) - React framework
- [tRPC](https://trpc.io/) - Type-safe APIs
- [Drizzle ORM](https://orm.drizzle.team/) - TypeScript ORM
- [shadcn/ui](https://ui.shadcn.com/) - UI component library
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [TipTap](https://tiptap.dev/) - Rich text editor

---

**Note**: This is a showcase repository for portfolio purposes. The source code is kept in a private repository.

Made with ❤️ by [Your Name]
