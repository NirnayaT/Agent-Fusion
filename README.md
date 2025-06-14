# AgentFusion - Real Estate Decision Making Platform

**Company:** Atherya  
**Project Type:** Full-Stack Web Application  

An all-in-one real estate decision-making application that empowers agents and consumers with advanced calculators, property listings, market data integration, and collaborative tools.

## 🎯 Project Vision

Create a comprehensive web-based platform that simplifies complex real estate decisions through:
- **Advanced Calculators**: Buy vs Later, Rent vs Buy, Equity, Agent Compensation
- **Property Listings**: Complete CRUD functionality with search and filters
- **Market Data Integration**: Real-time rates and property values
- **User Management**: Role-based access for agents and clients
- **Export & Sharing**: PDF generation and email sharing capabilities

## 🏗️ Project Structure

```
agentfusion-app/
├── client/                    # React 18+ Frontend
│   ├── src/
│   │   ├── components/        # Reusable UI Components
│   │   │   ├── ui/           # Basic UI elements (buttons, inputs, cards)
│   │   │   ├── layout/       # Layout components (header, sidebar, footer)
│   │   │   ├── forms/        # Form components with validation
│   │   │   ├── charts/       # Chart and visualization components
│   │   │   ├── auth/         # Authentication components
│   │   │   ├── dashboard/    # Dashboard specific components
│   │   │   ├── listings/     # Property listing components
│   │   │   └── calculators/  # Calculator components
│   │   ├── pages/            # Page Components
│   │   │   ├── auth/         # Login, register, forgot password
│   │   │   ├── dashboard/    # Main dashboard page
│   │   │   ├── listings/     # Listing pages (list, detail, create)
│   │   │   └── calculators/  # Calculator pages
│   │   ├── services/         # API Services
│   │   │   ├── api/          # Base API configuration
│   │   │   ├── auth/         # Authentication services
│   │   │   ├── listing/      # Listing CRUD services
│   │   │   └── calculator/   # Calculator services
│   │   ├── store/            # State Management (Redux Toolkit)
│   │   │   ├── slices/       # Redux slices for different domains
│   │   │   └── middleware/   # Custom middleware
│   │   ├── hooks/            # Custom React hooks
│   │   ├── utils/            # Helper functions and constants
│   │   ├── types/            # TypeScript type definitions
│   │   └── assets/           # Static assets (images, icons, fonts)
│   ├── public/               # Public static files
│   └── tests/                # Frontend tests
├── server/                   # FastAPI Backend (SOLID Principles)
│   ├── app/
│   │   ├── api/              # API Layer
│   │   │   ├── v1/           # API version 1
│   │   │   │   ├── endpoints/ # API endpoint definitions
│   │   │   │   └── dependencies/ # Endpoint dependencies
│   │   │   └── middleware/   # Custom middleware
│   │   ├── services/         # Business Logic Layer (SRP)
│   │   │   ├── auth/         # Authentication services
│   │   │   ├── user/         # User management services
│   │   │   ├── listing/      # Listing business logic
│   │   │   ├── calculator/   # Calculator services
│   │   │   │   ├── basic/    # Basic calculators (mortgage, LTV)
│   │   │   │   └── advanced/ # Advanced calculators
│   │   │   ├── market_data/  # External API integrations
│   │   │   ├── export/       # PDF and export services
│   │   │   └── email/        # Email services
│   │   ├── repositories/     # Data Access Layer (DIP)
│   │   │   ├── interfaces/   # Repository interfaces
│   │   │   └── implementations/ # SQLAlchemy implementations
│   │   ├── models/           # Data Models (SRP)
│   │   │   ├── database/     # SQLAlchemy database models
│   │   │   └── business/     # Business logic models
│   │   ├── schemas/          # Request/Response Schemas (ISP)
│   │   │   ├── request/      # Request schemas (Pydantic)
│   │   │   ├── response/     # Response schemas
│   │   │   └── database/     # Database schemas
│   │   ├── core/             # Core Configuration
│   │   │   ├── config/       # Application configuration
│   │   │   ├── security/     # Security utilities
│   │   │   └── database/     # Database configuration
│   │   ├── dependencies/     # Dependency Injection
│   │   └── utils/            # Utility functions
│   ├── alembic/              # Database Migrations
│   └── tests/                # Backend Tests
│       ├── unit/             # Unit tests
│       ├── integration/      # Integration tests
│       └── e2e/              # End-to-end tests
├── docs/                     # Project Documentation
│   ├── api/                  # API documentation
│   ├── architecture/         # Architecture documentation
│   ├── deployment/           # Deployment guides
│   └── team/                 # Team processes and guidelines
└── scripts/                  # Utility Scripts
    ├── setup/                # Setup scripts
    ├── deployment/           # Deployment scripts
    └── testing/              # Testing scripts
```

## 🛠️ Technology Stack

### Frontend
- **Framework**: React 18+ with TypeScript
- **Build Tool**: Vite (fast development and builds)
- **State Management**: Redux Toolkit (predictable state container)
- **UI Library**: Tailwind CSS + Headless UI (utility-first CSS)
- **Routing**: React Router v6 (declarative routing)
- **HTTP Client**: Axios (promise-based HTTP client)
- **Charts**: Chart.js or Recharts (data visualization)
- **Testing**: Jest + React Testing Library

### Backend
- **Framework**: FastAPI (Python 3.11+)
- **Database**: PostgreSQL 14+ with PostGIS
- **ORM**: SQLAlchemy 2.0 with async support
- **Authentication**: JWT tokens with FastAPI Security
- **Background Tasks**: Celery with Redis broker
- **Data Validation**: Pydantic models
- **API Documentation**: OpenAPI/Swagger (built-in)
- **Testing**: Pytest with async support

### Infrastructure
- **Containerization**: Docker & Docker Compose
- **Database**: PostgreSQL with PostGIS extension
- **Cache/Sessions**: Redis 7+
- **Cloud Platform**: AWS/Azure/GCP (TBD)
- **File Storage**: AWS S3 or equivalent

## 👥 Team Structure

### Sprint Creators & Planners
- **Nirnaya**: Scrum Master, GitHub setup, Jira management, project coordination
- **Pratik**: UI/UX Design for calculators, dashboard, and all pages
- **Giri**: Landing page development + Sprint planning support

### Implementation Team
- **Bishant**: Full-stack lead (React frontend + FastAPI integration)
- **Siddhartha**: Backend lead (FastAPI APIs, database, authentication)
- **Sanjay**: Backend support + Intern (basic calculators, data validation, testing)

## 🚀 Quick Start

### Prerequisites
- **Node.js**: 18+ with npm
- **Python**: 3.11+ with pip
- **PostgreSQL**: 14+
- **Redis**: 7+
- **Git**: Latest version

### Development Setup

1. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd agentfusion-app
   ```

2. **Frontend Setup**
   ```bash
   cd client
   npm install
   cp .env.example .env
   npm run dev  # Starts on http://localhost:3000
   ```

3. **Backend Setup**
   ```bash
   cd server
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   cp .env.example .env
   # Configure database settings in .env
   alembic upgrade head  # Run migrations
   uvicorn app.main:app --reload  # Starts on http://localhost:8000
   ```

4. **Database Setup**
   ```bash
   # Create PostgreSQL database
   createdb agentfusion
   
   # Install PostGIS extension
   psql agentfusion -c "CREATE EXTENSION postgis;"
   ```

5. **Docker Setup (Alternative)**
   ```bash
   docker-compose up -d
   ```

## 📋 Development Workflow

### Sprint Timeline (8 Weeks)
- **Week 1**: Foundation & Authentication
- **Week 2**: Listings Feature + Basic Calculators
- **Week 3**: Advanced Calculators
- **Week 4**: **MVP Complete** - Dashboard & User Experience
- **Week 5**: Export & Sharing Features
- **Week 6**: Market Data Integration
- **Week 7**: Testing & Quality Assurance
- **Week 8**: Deployment & Launch

### Daily Routine
- **9:00 AM**: Daily Standup (15 minutes)
- **Development**: Feature implementation and testing
- **Code Review**: Pull request reviews
- **Integration**: Continuous integration and testing

### Weekly Schedule
- **Monday 3:00 PM**: Sprint Planning (1 hour)
- **Tuesday-Thursday**: Development and daily standups
- **Friday 4:00 PM**: Sprint Review & Retrospective (30 minutes)

## 🏗️ SOLID Principles Implementation

### 1. Single Responsibility Principle (SRP)
- **Services**: Each service handles one specific domain
  - `AuthService`: Only authentication logic
  - `ListingService`: Only listing business logic
  - `CalculatorService`: Only calculation logic
- **Models**: Separate database and business models
- **Schemas**: Dedicated request/response schemas

### 2. Open/Closed Principle (OCP)
- **Calculator Services**: New calculator types can be added without modifying existing code
- **Repository Pattern**: New data sources can be added without changing business logic
- **API Endpoints**: New endpoints extend functionality without breaking existing ones

### 3. Liskov Substitution Principle (LSP)
- **Repository Implementations**: Different database implementations can be substituted
- **Service Interfaces**: Services can be replaced with different implementations
- **Calculator Types**: All calculators follow the same interface

### 4. Interface Segregation Principle (ISP)
- **Repository Interfaces**: Small, focused interfaces for specific data access
- **API Schemas**: Separate schemas for different use cases
- **Service Contracts**: Minimal interfaces for each service

### 5. Dependency Inversion Principle (DIP)
- **Service Dependencies**: Services depend on repository interfaces, not implementations
- **Database Abstraction**: Business logic doesn't depend on specific database
- **External APIs**: Services use abstractions for external API calls

## 🔌 API Documentation

### Base Configuration
- **Base URL**: `http://localhost:8000/api/v1/`
- **Authentication**: Bearer token (JWT)
- **Response Format**: JSON
- **Documentation**: Available at `/docs` (Swagger UI)

### Main Endpoints

#### Authentication
- `POST /auth/register` - User registration
- `POST /auth/login` - User login
- `GET /auth/me` - Get current user
- `POST /auth/refresh` - Refresh JWT token

#### Listings
- `GET /listings` - Get listings with filters
- `POST /listings` - Create new listing
- `GET /listings/{id}` - Get listing details
- `PUT /listings/{id}` - Update listing
- `DELETE /listings/{id}` - Delete listing

#### Calculators
- `POST /calculators/buy-now-vs-later` - Buy timing analysis
- `POST /calculators/rent-vs-buy` - Break-even calculation
- `POST /calculators/equity` - Home equity calculation
- `POST /calculators/agent-compensation` - Commission scenarios

#### Market Data
- `GET /market-data/rates` - Current mortgage rates
- `GET /market-data/property-value/{address}` - Property values
- `GET /market-data/tax-rates/{zip_code}` - Local tax rates

## 🧪 Testing Strategy

### Frontend Testing
- **Unit Tests**: Component testing with Jest + React Testing Library
- **Integration Tests**: API integration and user flow testing
- **E2E Tests**: Complete user journey testing with Cypress

### Backend Testing
- **Unit Tests**: Service and utility function testing with Pytest
- **Integration Tests**: API endpoint and database integration testing
- **Load Tests**: Performance testing with multiple concurrent users

### Quality Standards
- **Code Coverage**: Minimum 80% for critical paths
- **Code Review**: All pull requests require review
- **Automated Testing**: CI/CD pipeline runs all tests

## 📦 Deployment

### Development
```bash
# Frontend
npm run dev

# Backend
uvicorn app.main:app --reload
```

### Production
```bash
# Build frontend
npm run build

# Deploy backend
docker-compose up -d
```

### Environment Variables

#### Frontend (.env)
```env
VITE_API_BASE_URL=http://localhost:8000/api/v1
VITE_APP_NAME=AgentFusion
```

#### Backend (.env)
```env
DATABASE_URL=postgresql://user:password@localhost:5432/agentfusion
REDIS_URL=redis://localhost:6379
SECRET_KEY=your-secret-key
ZILLOW_API_KEY=your-zillow-api-key
FREDDIE_MAC_API_KEY=your-freddie-mac-api-key
```

## 🤝 Contributing

### Git Workflow
1. Create feature branch from `develop`
2. Make changes following coding standards
3. Write tests for new functionality
4. Create pull request to `develop`
5. Code review and merge

### Coding Standards
- **Frontend**: ESLint + Prettier configuration
- **Backend**: Black code formatter + isort
- **Commits**: Conventional commit messages
- **Documentation**: Update docs for new features

### Branch Naming
- **main**: Production-ready code
- **develop**: Integration branch for development
- **feature/feature-name**: Feature branches
- **hotfix/issue-name**: Urgent fixes\
  \**for example**:
    - `feature/user-authentication`
    - `bugfix/calculator-accuracy`
    - `hotfix/security-vulnerability`

## 📚 Additional Resources

- **API Documentation**: `/docs` endpoint (Swagger UI)
- **Architecture Docs**: `docs/architecture/`
- **Deployment Guide**: `docs/deployment/`
- **Team Guidelines**: `docs/team/`

## 📞 Support

For questions and support:
- **Project Manager**: Nirnaya
- **Technical Lead**: Siddhartha (Backend), Bishant (Frontend)
- **Design Lead**: Pratik

## 📄 License

**Proprietary Software**

© 2025 Atherya. All Rights Reserved.

This software is proprietary and confidential. Unauthorized copying, distribution, or use is strictly prohibited.
---

**Last Updated**: June 13, 2025  
**Version**: 1.0  
**Status**: Active Development
