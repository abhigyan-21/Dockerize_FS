# Dockerize Full Stack Applications

This repository demonstrates Docker containerization techniques for full-stack applications, focusing on multi-stage builds and optimization strategies.

## Projects

### 1. React Docker Multi-Stage Build (`react-docker-app/`)

A complete React application demonstrating multi-stage Docker builds for optimal production deployment.

**Features:**
- Multi-stage Dockerfile (Node.js build → Nginx production)
- Custom Nginx configuration with routing and caching
- Comprehensive .dockerignore for build optimization
- ~90% size reduction compared to single-stage builds
- Production-ready security headers and compression

**Quick Start:**
```bash
cd react-docker-app
docker build -t react-docker-app .
docker run -p 3000:80 react-docker-app
```

**Image Size Comparison:**
- Multi-stage: ~25-30MB
- Single-stage: ~400-500MB
- Reduction: ~90%

## Key Concepts Demonstrated

1. **Multi-Stage Builds**: Separate build and runtime environments
2. **Image Optimization**: Minimal production images
3. **Security**: Non-root users, security headers
4. **Performance**: Static asset caching, compression
5. **Best Practices**: .dockerignore, layer optimization

## Prerequisites

- Docker Desktop
- Node.js (for local development)
- Git

## Repository Structure

```
Dockerize_FS/
├── README.md
├── react-docker-app/          # React multi-stage build example
│   ├── Dockerfile             # Multi-stage configuration
│   ├── Dockerfile.single-stage # Comparison build
│   ├── .dockerignore          # Build optimization
│   ├── nginx.conf             # Production web server config
│   ├── docker-build.md        # Detailed documentation
│   └── src/                   # React application source
└── [future projects]          # Additional containerization examples
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/abhigyan-21/Dockerize_FS.git
   cd Dockerize_FS
   ```

2. Choose a project and follow its specific README instructions

## Contributing

Feel free to contribute additional containerization examples, optimizations, or improvements to existing projects.

## License

MIT License - see individual project directories for specific details.