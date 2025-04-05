# Matrimony Platform Directory Structure

```text
matrimony-platform/
├── api-gateway/
│   ├── cmd/
│   │   └── main.go
│   ├── internal/
│   │   ├── config/         # Gateway configuration
│   │   ├── routes/         # Route definitions
│   │   ├── middleware/     # Auth, logging, rate limiting
│   │   ├── clients/        # Service discovery & client factories
│   │   └── utils/          # Shared utilities
│   ├── api/
│   │   └── swagger/        # OpenAPI specifications
│   ├── deployments/
│   │   ├── docker/
│   │   │   └── Dockerfile
│   │   └── kubernetes/
│   │       └── gateway.yaml
│   └── config.yaml         # Environment configurations
│
├── auth-service/
│   ├── cmd/
│   │   └── main.go
│   ├── internal/
│   │   ├── auth/           # Core authentication logic
│   │   ├── jwt/            # Token management
│   │   ├── models/         # Data models
│   │   ├── repository/     # Database interactions
│   │   ├── handlers/       # HTTP handlers
│   │   └── middleware/     # Security middleware
│   ├── migrations/         # SQL migration files
│   ├── deployments/
│   │   ├── docker/
│   │   └── kubernetes/
│   ├── test/
│   │   ├── unit/           # Unit tests
│   │   └── integration/    # Integration tests
│   └── config.yaml
│
├── user-service/
│   ├── cmd/
│   │   └── main.go
│   ├── internal/
│   │   ├── profile/        # Profile management
│   │   ├── matchmaking/    # Algorithm implementations
│   │   ├── search/         # Search functionality
│   │   ├── storage/        # File upload handling
│   │   ├── cache/          # Redis integrations
│   │   └── ...             # Other components
│   ├── migrations/         # DB migration scripts
│   ├── deployments/
│   └── test/
│
├── admin-service/
│   ├── cmd/
│   │   └── main.go
│   ├── internal/
│   │   ├── dashboard/      # Monitoring components
│   │   ├── audit/          # Audit logging
│   │   └── ...             # Admin-specific features
│   └── deployments/
│
├── common/                 # Shared across services
│   ├── pkg/
│   │   ├── logging/        # Structured logging
│   │   ├── errors/         # Custom error types
│   │   ├── database/       # DB connection factories
│   │   └── messaging/      # RabbitMQ wrappers
│   ├── proto/              # Protobuf definitions
│   └── scripts/            # Shared scripts
│
├── infrastructure/
│   ├── docker-compose/     # Local development setup
│   ├── terraform/          # Cloud provisioning
│   │   ├── modules/
│   │   ├── aws/
│   │   └── gcp/
│   ├── monitoring/
│   │   ├── prometheus/     # Alert rules
│   │   └── grafana/        # Dashboards
│   └── k8s/                # Base Kubernetes manifests
│
├── docs/
│   ├── ARCHITECTURE.md     # System design
│   ├── API_DOCS.md         # API references
│   └── OPERATIONS.md       # Deployment guide
│
├── scripts/                # Global scripts
│   ├── migration/
│   ├── deployment/
│   └── monitoring/
│
├── .github/                # CI/CD workflows
│   └── workflows/
│
├── Makefile                # Global build commands
└── README.md               # Project overview