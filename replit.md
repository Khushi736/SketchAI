# Overview

SketchAI is an AI-powered image conversion application that transforms regular photographs into pencil sketch drawings. The application provides a modern web interface where users can upload images, select from different artistic styles (light, medium, dark, artistic), and download the resulting pencil sketches. Built as a full-stack web application, it combines React frontend with Express backend and utilizes AI services for image processing.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript for type safety and modern development
- **Build Tool**: Vite for fast development and optimized production builds
- **UI Framework**: Shadcn/ui components built on Radix UI primitives for accessible, customizable interface components
- **Styling**: Tailwind CSS with CSS variables for consistent theming and responsive design
- **State Management**: TanStack React Query for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **File Upload**: React Dropzone for drag-and-drop file upload functionality

## Backend Architecture
- **Framework**: Express.js with TypeScript for the REST API server
- **File Processing**: Multer for handling multipart file uploads with memory storage
- **Image Processing**: Sharp library for basic image transformations and preprocessing
- **Development**: Hot module replacement via Vite integration in development mode
- **Session Management**: Connect-pg-simple for PostgreSQL-backed session storage

## Data Storage Solutions
- **Database**: PostgreSQL configured via Drizzle ORM with type-safe schema definitions
- **Connection**: Neon Database serverless PostgreSQL for cloud hosting
- **Schema Management**: Drizzle Kit for migrations and schema synchronization
- **Runtime Storage**: In-memory storage implementation with interface for easy database migration
- **File Storage**: Base64 encoding for storing images directly in database records

## Authentication and Authorization
- **Session-based**: Express sessions with PostgreSQL session store
- **CORS**: Configured for cross-origin requests with credentials support
- **File Validation**: MIME type checking and file size limits for security

## Image Processing Pipeline
- **AI Integration**: OpenAI API integration for advanced image analysis and conversion
- **Style Variants**: Four distinct pencil sketch styles (light, medium, dark, artistic)
- **Processing States**: Async processing with status tracking (processing, completed, failed)
- **Image Formats**: Support for JPEG, PNG, and WebP input formats
- **Size Limits**: 10MB maximum file size for uploads

# External Dependencies

## Core Infrastructure
- **Database**: Neon Database (PostgreSQL) for data persistence
- **AI Services**: OpenAI API for image analysis and sketch conversion
- **Development Platform**: Replit-specific plugins for development environment integration

## UI and Styling
- **Component Library**: Radix UI primitives for accessible base components
- **Styling Framework**: Tailwind CSS for utility-first styling approach
- **Icons**: Lucide React for consistent iconography
- **Fonts**: Google Fonts integration (Inter, Architects Daughter, DM Sans, Fira Code, Geist Mono)

## Development and Build Tools
- **TypeScript**: Full-stack type safety and developer experience
- **ESBuild**: Fast bundling for production server builds
- **PostCSS**: CSS processing with Tailwind and Autoprefixer
- **Sharp**: High-performance image processing library

## Runtime Dependencies
- **Image Processing**: Sharp for server-side image manipulation
- **Date Handling**: date-fns for date formatting and manipulation
- **Validation**: Zod for runtime type validation and schema enforcement
- **HTTP Client**: Fetch API for client-server communication