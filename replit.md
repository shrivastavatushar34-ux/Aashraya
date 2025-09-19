# Overview

This is a full-stack web application for AASHRAYA (Prashraya Welfare Foundation), a youth-led NGO operating across India. The application serves as the organization's digital platform to showcase their six welfare programs (Shiksha, Shakti, Paryavaran, Vastra, Chikitsa, and Gillu), manage donations, display events and blog content, and facilitate volunteer engagement. The platform emphasizes transparency, community engagement, and social impact.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite for development and build tooling
- **Routing**: Client-side routing with Wouter for a lightweight single-page application experience
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Components**: Radix UI primitives with shadcn/ui component library for consistent, accessible design
- **Styling**: Tailwind CSS with CSS custom properties for theming and responsive design
- **Form Handling**: React Hook Form with Zod validation for type-safe form management

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Database**: PostgreSQL (configured for Neon Database)
- **API Design**: RESTful API endpoints with proper error handling and logging middleware
- **Session Management**: PostgreSQL session store with connect-pg-simple
- **Development**: Hot module replacement and development tooling via Vite integration

## Data Storage Solutions
- **Primary Database**: PostgreSQL with connection pooling via Neon Database serverless driver
- **Schema Management**: Drizzle Kit for migrations and schema evolution
- **Data Models**: Comprehensive schema covering users, donations, students, events, blog posts, contact messages, and volunteers
- **Storage Strategy**: Relational data model with proper foreign key relationships and indexing

## Authentication and Authorization
- **User Management**: Role-based access control (user, admin, volunteer)
- **Session Storage**: Server-side sessions stored in PostgreSQL
- **Security**: Input validation using Zod schemas and secure session handling

## External Service Integrations
- **Payment Processing**: Stripe integration for donation handling with payment intents and customer management
- **Development Tools**: Replit-specific development plugins for enhanced development experience
- **Image Assets**: External image hosting via Unsplash for demonstration content
- **Social Media**: Integration points for Instagram, Facebook, Twitter, LinkedIn, and YouTube

The architecture prioritizes type safety, developer experience, and scalability while maintaining a clean separation of concerns between frontend presentation, backend logic, and data persistence layers.