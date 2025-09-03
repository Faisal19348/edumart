# Overview

EduMart BD is an educational platform designed for Bangladesh students, providing a comprehensive learning ecosystem with courses, digital library access, and book purchasing capabilities. The application serves as a one-stop educational marketplace featuring multi-level courses, digital resources, and physical book sales, all integrated into a modern web platform.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The client-side is built with React and TypeScript, utilizing a modern component-based architecture:
- **React Router**: Uses Wouter for lightweight client-side routing
- **UI Framework**: Shadcn/ui components with Radix UI primitives for accessible, customizable components
- **Styling**: Tailwind CSS with custom CSS variables for theming and responsive design
- **State Management**: TanStack Query (React Query) for server state management and data fetching
- **Build Tool**: Vite for fast development and optimized production builds

## Backend Architecture
The server follows a REST API pattern built on Express.js:
- **Framework**: Express.js with TypeScript for type safety
- **API Structure**: RESTful endpoints organized by resource (courses, books, users)
- **Data Layer**: In-memory storage implementation with interface abstraction for future database integration
- **Middleware**: Custom logging, JSON parsing, and error handling middleware
- **Development**: Hot module replacement and development server integration with Vite

## Data Storage Solutions
Currently implements an in-memory storage pattern with plans for PostgreSQL integration:
- **Schema Definition**: Drizzle ORM schema definitions in shared directory for type safety
- **Database Setup**: Configured for PostgreSQL with Neon Database serverless connection
- **Data Models**: User management, course catalog, and book inventory with proper relationships
- **Migration Support**: Drizzle Kit for database migrations and schema management

## Component Organization
The frontend follows a structured component hierarchy:
- **UI Components**: Reusable design system components in `/components/ui`
- **Feature Components**: Business logic components for courses, books, community features
- **Layout Components**: Navigation, footer, and page structure components
- **Page Components**: Route-level components combining multiple features

## API Design
RESTful API endpoints following resource-based naming:
- **Courses API**: CRUD operations with featured course filtering
- **Books API**: Inventory management with popularity filtering
- **User API**: Authentication and profile management (prepared but not fully implemented)
- **Error Handling**: Consistent error responses with proper HTTP status codes

# External Dependencies

## Database and Storage
- **Neon Database**: Serverless PostgreSQL database for production data storage
- **Drizzle ORM**: Type-safe database client and query builder
- **connect-pg-simple**: PostgreSQL session store for Express sessions

## UI and Styling
- **Shadcn/ui**: Pre-built component library built on Radix UI primitives
- **Radix UI**: Unstyled, accessible UI primitives for complex components
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Lucide React**: Icon library for consistent iconography
- **React Icons**: Additional icon sets including social media icons

## Development and Build Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Static type checking for both client and server code
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Tailwind and autoprefixer plugins

## Data Fetching and State Management
- **TanStack Query**: Server state management, caching, and data synchronization
- **React Hook Form**: Form state management and validation
- **Zod**: Runtime type validation and schema parsing

## Development Environment
- **Replit Integration**: Custom plugins for Replit development environment
- **tsx**: TypeScript execution for Node.js development server
- **Wouter**: Minimalist router for React applications