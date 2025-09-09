# CompliCheck - AI-Powered Compliance Management

Enterprise compliance analysis with OpenAI integration

## Quick Start

### Prerequisites
- Java 17
- Node.js 18
- Docker
- OpenAI API Key

### Setup
```bash
# 1. Clone and setup
git clone <your-repo>
cd complicheck

# 2. Start database
docker run -d --name complicheck-postgres \
  -e POSTGRES_DB=complicheck \
  -e POSTGRES_USER=complicheck \
  -e POSTGRES_PASSWORD=dev_password \
  -p 5432:5432 postgres:15.4-alpine

# 3. Backend setup
cd backend
./mvnw spring-boot:run

# 4. Frontend setup (new terminal)
cd frontend
npm install
npm run dev