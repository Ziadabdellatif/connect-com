# Client Management System for Marketers

## Overview

This is a full-stack web application designed to help real estate marketers manage their client relationships in Arabic. The system provides a comprehensive platform for marketers to register, log in, add new clients, and track their interaction history. The application is built with modern web technologies and follows a clean, user-friendly design optimized for Arabic language and right-to-left (RTL) layout.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized production builds
- **UI Framework**: Tailwind CSS with shadcn/ui components
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React Query (TanStack Query) for server state management
- **Form Handling**: React Hook Form with Zod validation
- **Styling**: Custom CSS variables with RTL support and Arabic font integration

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Authentication**: bcrypt for password hashing with local storage session management
- **API Design**: RESTful endpoints with JSON responses

### Database Schema
The application uses a relational database with two main entities:
- **Marketers**: User accounts with authentication credentials
- **Clients**: Customer records linked to specific marketers

## Key Components

### Authentication System
- Custom authentication context using React Context API
- Password hashing with bcrypt
- Session persistence via localStorage
- Route protection with authenticated/unauthenticated guards

### Client Management
- Comprehensive client form with validation
- Client search and filtering capabilities
- Status tracking and WhatsApp integration
- Client history with pagination and sorting

### UI/UX Features
- Full Arabic language support with RTL layout
- Responsive design optimized for mobile devices
- Dark mode ready CSS variables
- Toast notifications for user feedback
- Loading states and error handling

## Data Flow

1. **User Registration/Login**: Users create accounts or authenticate through the login system
2. **Client Creation**: Authenticated marketers can add new clients with detailed information
3. **Client Management**: Marketers can view, search, and filter their client database
4. **Communication**: Direct WhatsApp integration for client communication
5. **Data Persistence**: All data is stored in PostgreSQL with proper relationships

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL connection
- **drizzle-orm**: TypeScript ORM for database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **wouter**: Lightweight routing library
- **zod**: Schema validation library

### Development Tools
- **Vite**: Build tool and development server
- **TypeScript**: Type safety and development experience
- **Tailwind CSS**: Utility-first CSS framework
- **ESLint**: Code linting and formatting

## Deployment Strategy

The application is configured for deployment on Replit with the following setup:
- **Build Command**: `npm run build` - Builds both client and server
- **Start Command**: `npm run start` - Runs the production server
- **Development**: `npm run dev` - Runs development server with hot reload
- **Port Configuration**: Server runs on port 5000, mapped to external port 80
- **Environment**: Requires `DATABASE_URL` environment variable for PostgreSQL connection

### Build Process
1. Vite builds the client application to `dist/public`
2. esbuild bundles the server code to `dist/index.js`
3. Static files are served from the built client directory
4. Server handles API routes and serves the SPA for all other routes

## Recent Changes
- **June 26, 2025 - Major UI/UX Enhancement**: Complete redesign of client registration form with improved mobile-friendly interface, gradient backgrounds, larger input fields, and better visual hierarchy
- **June 26, 2025 - Admin Dashboard Implementation**: Added comprehensive admin dashboard with lead status management board, client overview statistics, and marketer management capabilities
- **June 26, 2025 - Google Sheets Integration**: Integrated Google Apps Script endpoint for automatic data synchronization with external spreadsheet system
- **June 26, 2025 - Auto-Admin Assignment**: First registered marketer automatically receives admin privileges for system management
- **June 26, 2025 - Enhanced Database Schema**: Added isAdmin field to marketers table and comprehensive admin API endpoints

## Key Features Added
### Admin Dashboard
- Real-time lead status updates and management
- Comprehensive client overview with search and filtering
- Marketer management and activity monitoring
- WhatsApp integration for direct client communication
- Status change tracking and analytics

### Enhanced Client Registration UI
- Modern gradient design with improved visual appeal
- Larger, touch-friendly input fields optimized for mobile
- Better error handling with highlighted validation messages
- Animated submit button with loading states
- Dual data storage (local database + Google Sheets sync)

### System Administration
- Automatic admin role assignment for first user
- Role-based access control for admin features
- Client status management capabilities
- System-wide data analytics and reporting

## Changelog
- June 26, 2025. Initial setup
- June 26, 2025. Major enhancement with admin dashboard and improved UI

## User Preferences

Preferred communication style: Simple, everyday language.
Requests focus on: Admin dashboard functionality and improved client registration UI.