# Application JSON Schema Generator

## Project Structure
```
/Samples
├── application/              # Core application settings
│   ├── app.config.json      # Main application configuration
│   ├── theme.config.json    # Theme and styling
│   └── env.config.json      # Environment variables
│
├── frontend/                # Frontend specific
│   ├── components/          # UI Component configurations
│   │   ├── forms/          # Form configurations
│   │   ├── tables/         # Table configurations
│   │   └── dashboard/      # Dashboard configurations
│   ├── routing.json        # Route configurations
│   └── state.json          # State management
│
├── backend/                 # Backend specific
│   ├── api/                # API configurations
│   │   ├── endpoints.json  # API endpoint definitions
│   │   └── swagger.json    # API documentation
│   ├── database/           # Database configurations
│   │   ├── models/         # Data models
│   │   └── migrations/     # Migration settings
│   └── services/           # Service configurations
│
├── features/               # Feature modules
│   ├── auth/              # Authentication feature
│   │   ├── config.json    # Auth configuration
│   │   ├── roles.json     # Role definitions
│   │   └── permissions.json# Permission settings
│   ├── dashboard/         # Dashboard feature
│   └── user-management/   # User management feature
│
└── deployment/            # Deployment configurations
    ├── docker/            # Docker settings
    ├── environments/      # Environment-specific configs
    └── ci-cd/            # CI/CD pipeline configs
```

## Quick Start

1. **Choose Your Features**
   - Select which features you want in your application
   - Configure each feature through its respective JSON

2. **Database Setup**
   - Choose your database (PostgreSQL, MySQL, or Supabase)
   - Configure connection details

3. **Customize UI**
   - Modify theme settings
   - Customize component styles
   - Configure layouts

## Configuration Examples

### 1. Basic Application Setup
```json
{
  "name": "My App",
  "features": ["auth", "dashboard"],
  "database": "postgresql",
  "theme": "light"
}
```

### 2. Feature Configuration
```json
{
  "auth": {
    "enabled": true,
    "providers": ["email", "google"]
  },
  "dashboard": {
    "enabled": true,
    "widgets": ["analytics", "users"]
  }
}
```

## Team Workflows

### Creation Engine Team
- Works with: `/application`, `/frontend/components`
- Handles: Component generation, templates

### Rules Engine Team
- Works with: `/backend/api`, `/features`
- Handles: Business logic, validation rules

### Thematic Engine Team
- Works with: `/application/theme.config.json`, `/frontend/components`
- Handles: Styling, theming, UI/UX

### Authentication Engine Team
- Works with: `/features/auth`
- Handles: Authentication, authorization

### Migration Engine Team
- Works with: `/backend/database`
- Handles: Database schemas, migrations

### Analytics Engine Team
- Works with: `/features/analytics`, `/backend/services`
- Handles: Monitoring, reporting

### Testing Engine Team
- Works with: All directories
- Handles: Testing configurations, E2E tests

## Configuration Guidelines

1. **Naming Conventions**
   - Use kebab-case for file names
   - Use camelCase for JSON properties

2. **File Organization**
   - Keep related configs together
   - Use meaningful directory names
   - Split large configs into smaller files

3. **Documentation**
   - Each config file should have a description
   - Document all available options
   - Include examples

## Environment Variables
- `DATABASE_URL`: Database connection string
- `JWT_SECRET`: JWT secret key
- `API_URL`: Backend API URL
- More in `/application/env.config.json` 