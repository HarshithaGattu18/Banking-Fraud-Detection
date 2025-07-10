# Banking Fraud Detection System

A comprehensive fraud detection system built with Next.js frontend, Java Spring Boot backend, and blockchain integration for secure transaction logging.

## Features

### Frontend (Next.js)
- **Role-based Authentication**: Separate dashboards for Users, Admins, and Analysts
- **Real-time Transaction Monitoring**: Live updates on transaction status
- **Fraud Alert System**: Immediate notifications for suspicious activities
- **Blockchain Integration**: View transaction logs stored on blockchain
- **Responsive Design**: Works on desktop and mobile devices

### Backend (Java Spring Boot)
- **RESTful API**: Clean API endpoints for all operations
- **JWT Authentication**: Secure token-based authentication
- **Machine Learning Integration**: AI-powered fraud detection
- **Database Integration**: H2 (development) and MySQL (production)
- **Blockchain Logging**: All transactions logged to blockchain

### Blockchain (Solidity Smart Contracts)
- **Transaction Logging**: Immutable transaction records
- **Fraud Alert System**: Automated alerts for high-risk transactions
- **Access Control**: Role-based permissions for contract interactions

## Tech Stack

### Frontend
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- shadcn/ui components
- Lucide React icons

### Backend
- Java 17
- Spring Boot 3.2
- Spring Security
- Spring Data JPA
- JWT Authentication
- Web3j (Blockchain integration)
- DeepLearning4J (ML models)

### Blockchain
- Solidity
- Ethereum/Ganache
- Web3j
- Smart Contracts

### Database
- H2 (Development)
- MySQL (Production)

## Getting Started

### Prerequisites
- Node.js 18+
- Java 17+
- Maven 3.6+
- Ganache CLI or local Ethereum node

### Frontend Setup

1. Install dependencies:
\`\`\`bash
npm install
\`\`\`

2. Run the development server:
\`\`\`bash
npm run dev
\`\`\`

3. Open [http://localhost:3000](http://localhost:3000)

### Backend Setup

1. Navigate to backend directory:
\`\`\`bash
cd backend
\`\`\`

2. Install dependencies:
\`\`\`bash
mvn clean install
\`\`\`

3. Run the application:
\`\`\`bash
mvn spring-boot:run
\`\`\`

4. API will be available at [http://localhost:8080](http://localhost:8080)

### Blockchain Setup

1. Install Ganache CLI:
\`\`\`bash
npm install -g ganache-cli
\`\`\`

2. Start local blockchain:
\`\`\`bash
ganache-cli -p 8545 -d
\`\`\`

3. Deploy smart contracts:
\`\`\`bash
cd blockchain
truffle migrate --network development
\`\`\`

## API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Transactions
- `GET /api/transactions` - Get user transactions
- `POST /api/transactions` - Process new transaction
- `GET /api/transactions/flagged` - Get flagged transactions
- `PUT /api/transactions/{id}/status` - Update transaction status

### Blockchain
- `GET /api/blockchain` - Get blockchain status
- `GET /api/blockchain?type=contracts` - Get smart contract info

## Machine Learning Models

The system uses multiple ML models for fraud detection:

1. **Random Forest Classifier** - Primary fraud detection model
2. **Neural Network** - Deep learning approach for pattern recognition
3. **SVM Classifier** - Support Vector Machine for classification
4. **Gradient Boosting** - Ensemble method for improved accuracy

### Risk Factors Analyzed
- Transaction amount patterns
- Time-based anomalies
- Geographic location changes
- Merchant verification
- User behavior patterns

## Smart Contract Functions

### FraudDetection.sol
- `logTransaction()` - Log transaction to blockchain
- `createFraudAlert()` - Create fraud alert
- `resolveFraudAlert()` - Resolve fraud alert
- `getTransactionLog()` - Retrieve transaction data

## Security Features

- **JWT Authentication**: Secure API access
- **Role-based Access Control**: Different permissions for users/admins/analysts
- **Blockchain Immutability**: Tamper-proof transaction logs
- **Encrypted Data Storage**: Sensitive data encryption
- **Rate Limiting**: API rate limiting for security

## Deployment

### Frontend (Vercel)
\`\`\`bash
npm run build
vercel deploy
\`\`\`

### Backend (Docker)
\`\`\`bash
docker build -t fraud-detection-backend .
docker run -p 8080:8080 fraud-detection-backend
\`\`\`

### Database (Production)
Update `application.yml` with production database credentials:
\`\`\`yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/frauddb
    username: ${DB_USERNAME}
    password: ${DB_PASSWORD}
\`\`\`

## Testing

### Frontend Tests
\`\`\`bash
npm run test
\`\`\`

### Backend Tests
\`\`\`bash
mvn test
\`\`\`

### Smart Contract Tests
\`\`\`bash
truffle test
\`\`\`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email support@frauddetection.com or create an issue in the repository.
