# 🚀 AI Resume Analyzer

<div align="center">
  <br />

  <div>
    <img alt="React" src="https://img.shields.io/badge/React-4c84f3?style=for-the-badge&logo=react&logoColor=white">
    <img alt="TypeScript" src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6">
    <img alt="Tailwind CSS" src="https://img.shields.io/badge/-Tailwind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white">
    <img alt="Puter.js" src="https://img.shields.io/badge/Puter.js-181758?style=for-the-badge&logoColor=white">
  </div>

  <h3 align="center">Smart feedback for your dream job!</h3>

  <p align="center">
    An AI-powered resume analyzer that provides detailed feedback, ATS scores, and improvement suggestions tailored to specific job listings.
  </p>
</div>

## 📋 Table of Contents

- [✨ Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Quick Start](#-quick-start)
- [📱 How It Works](#-how-it-works)
- [🏗️ Project Structure](#️-project-structure)
- [🔧 Configuration](#-configuration)
- [📚 Learning Resources](#-learning-resources)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## ✨ Features

### 🎯 **Core Functionality**
- **AI-Powered Analysis**: Get comprehensive resume feedback using advanced AI models
- **ATS Score Calculation**: Receive detailed ATS (Applicant Tracking System) compatibility scores
- **Job-Specific Feedback**: Tailored analysis based on specific job descriptions and requirements
- **PDF Processing**: Seamless PDF upload and conversion to images for analysis
- **Resume Storage**: Secure cloud storage for all your resumes using Puter.js

### 🎨 **User Experience**
- **Modern UI/UX**: Clean, responsive design built with Tailwind CSS
- **Real-time Processing**: Live status updates during resume analysis
- **Interactive Dashboard**: Track all your resume submissions and scores
- **Detailed Feedback**: Comprehensive breakdown across multiple categories:
  - Overall Score
  - ATS Compatibility
  - Tone and Style
  - Content Quality
  - Structure and Format
  - Skills Alignment

### 🔐 **Authentication & Security**
- **Browser-based Auth**: No backend required - authentication handled entirely in the browser
- **Privacy-First**: Your data stays secure with Puter.js's privacy-focused approach
- **User-specific Storage**: Each user's resumes and data are isolated and secure

## 🛠️ Tech Stack

### **Frontend**
- **[React 19](https://react.dev/)** - Modern React with latest features
- **[React Router v7](https://reactrouter.com/)** - Advanced routing with data loaders and error boundaries
- **[TypeScript](https://www.typescriptlang.org/)** - Type-safe development
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **[Vite](https://vite.dev/)** - Fast build tool and dev server

### **Backend & Services**
- **[Puter.js]** - Serverless backend services
  - Authentication
  - File storage
  - AI integration (Claude, GPT, DALL·E, OCR)
  - Key-value database
- **[Zustand](https://github.com/pmndrs/zustand)** - Lightweight state management

### **AI & Processing**
- **[PDF.js](https://mozilla.github.io/pdf.js/)** - PDF processing and conversion
- **Claude 3.7 Sonnet** - AI model for resume analysis
- **OCR Capabilities** - Text extraction from resume images

## 🚀 Quick Start

### Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Git](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sahasunit/ai-resume-analyzer.git
   cd ai-resume-analyzer
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to [http://localhost:5173](http://localhost:5173)

### Build for Production

```bash
npm run build
npm start
```

## 📱 How It Works

### 1. **Authentication**
- Users sign in through Puter.js authentication
- No backend setup required - everything runs in the browser

### 2. **Resume Upload**
- Upload PDF resumes through drag-and-drop interface
- Automatic PDF to image conversion for AI analysis
- Secure cloud storage using Puter.js file system

### 3. **AI Analysis**
- Resume is analyzed using Claude 3.7 Sonnet
- Job-specific feedback based on provided job description
- Comprehensive scoring across multiple categories

### 4. **Results Dashboard**
- View detailed feedback and scores
- Track all resume submissions
- Access improvement suggestions and tips

## 🏗️ Project Structure

```
ai-resume-analyzer/
├── app/
│   ├── components/          # Reusable UI components
│   │   ├── Accordion.tsx
│   │   ├── ATS.tsx
│   │   ├── Details.tsx
│   │   ├── FileUploader.tsx
│   │   ├── Navbar.tsx
│   │   ├── ResumeCard.tsx
│   │   ├── ScoreBadge.tsx
│   │   ├── ScoreCircle.tsx
│   │   ├── ScoreGauge.tsx
│   │   └── Summary.tsx
│   ├── lib/                # Utility libraries
│   │   ├── pdf2img.ts      # PDF processing
│   │   ├── puter.ts        # Puter.js integration
│   │   └── utils.ts        # Helper functions
│   ├── routes/             # Application routes
│   │   ├── auth.tsx        # Authentication page
│   │   ├── home.tsx        # Dashboard
│   │   ├── resume.tsx      # Resume analysis results
│   │   ├── upload.tsx      # Resume upload
│   │   └── wipe.tsx        # Data cleanup
│   ├── app.css             # Global styles
│   └── root.tsx            # Root component
├── constants/              # Application constants
├── types/                  # TypeScript type definitions
├── public/                 # Static assets
└── package.json
```

## 🔧 Configuration

### Environment Setup

The application uses Puter.js for all backend services. No additional environment variables or API keys are required.

### Customization

You can customize the AI analysis by modifying the instructions in `constants/index.ts`:

```typescript
export const prepareInstructions = ({jobTitle, jobDescription}) => `
  // Your custom analysis instructions here
`;
```


## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
