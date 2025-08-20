# replit.md

## Overview

BecaFuturo is a comprehensive educational platform designed to help high school students in Hidalgo, Estado de México, and Mexico City navigate their transition to university. The platform provides a vocational test, university directory, scholarship search, and event calendar to help students discover their ideal career path and find educational opportunities.

The application is built as a full-stack web platform with a React frontend using TypeScript and shadcn/ui components, and an Express.js backend with PostgreSQL database integration through Drizzle ORM. The system focuses on providing personalized career recommendations and connecting students with relevant universities and scholarship opportunities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite as the build tool
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for client-side routing
- **Forms**: React Hook Form with Zod validation
- **Theme System**: Custom theme provider with light/dark mode support

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database Integration**: Drizzle ORM with PostgreSQL
- **Session Management**: Express sessions with PostgreSQL store (connect-pg-simple)
- **Development Setup**: Hot reload with Vite integration for development mode

### Data Storage Solutions
- **Primary Database**: PostgreSQL with Neon serverless hosting
- **ORM**: Drizzle ORM for type-safe database operations
- **Schema Management**: Drizzle Kit for migrations and schema updates
- **Static Data**: JSON files for universities, scholarships, events, and vocational test questions stored in server/data directory

### Database Schema Design
The system uses four main entities:
- **Users**: Basic authentication and user management
- **Test Results**: Stores vocational test answers and career recommendations
- **Scholarship Applications**: Tracks student applications to scholarships
- **Static Data Tables**: Universities and scholarships with JSONB fields for flexible data structures

### Authentication and Authorization
- Simple username/password authentication system
- Session-based authentication using Express sessions
- Sessions stored in PostgreSQL for persistence
- No complex role-based access control - focused on student users

### API Architecture
- RESTful API design with Express.js routes
- Endpoints for universities, scholarships, test results, and events
- Query parameter-based filtering for search functionality
- JSON responses with proper error handling
- Request logging middleware for development debugging

## External Dependencies

### Database and Hosting
- **Neon Database**: PostgreSQL serverless database hosting
- **Replit**: Development and hosting platform

### UI and Styling
- **shadcn/ui**: Pre-built React component library
- **Radix UI**: Accessible component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Font Awesome**: Icon library for UI elements
- **Google Fonts**: Montserrat and Open Sans font families

### Development and Build Tools
- **Vite**: Frontend build tool and development server
- **TypeScript**: Static type checking
- **ESBuild**: Backend bundling for production
- **Drizzle Kit**: Database schema management and migrations

### Feature Libraries
- **TanStack Query**: Server state management and caching
- **React Hook Form**: Form handling and validation
- **Zod**: Schema validation
- **date-fns**: Date manipulation and formatting
- **jsPDF**: PDF generation for test results
- **Wouter**: Lightweight client-side routing

### Development Utilities
- **tsx**: TypeScript execution for development
- **PostCSS**: CSS processing with Autoprefixer
- **Class Variance Authority**: Component variant management
- **clsx & tailwind-merge**: Conditional CSS class handling