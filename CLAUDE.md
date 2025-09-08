# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

EdgeFirst AI is building a company website and application ecosystem focused on edge-first, privacy-preserving AI applications. The core principle is that all AI processing happens on-device without sending user data to cloud servers.

## Key Technical Principles

### Edge-First Architecture
- All AI inference must run on-device using:
  - Apple Intelligence (iOS/macOS)
  - Gemini Nano (Android/Chrome)
  - Llama.cpp (Cross-platform)
  - ONNX Runtime (Web)
- User data never leaves the device for processing
- Optional stateless cloud relay only for temporary encrypted sync
- Complete offline functionality is mandatory

### Privacy Requirements
- Zero cloud storage of user data
- End-to-end encryption for any peer-to-peer communication
- No analytics or tracking without explicit consent
- Complete data export capability
- Local storage using SQLite/CoreData

## Development Commands

### Website Development
```bash
# If using Next.js or similar framework
npm install        # Install dependencies
npm run dev       # Start development server
npm run build     # Build for production
npm run lint      # Run linting
npm run test      # Run tests
```

### Mobile App Development
```bash
# iOS (if using React Native or Flutter)
npx pod-install   # Install iOS dependencies
npm run ios       # Run on iOS simulator

# Android
npm run android   # Run on Android emulator
```

## Architecture Patterns

### Data Flow
- Traditional Cloud: User → Cloud AI → Database → Cloud AI → User
- EdgeFirst: User Device AI ← → Encrypted Relay (temporary) ← → User Device AI

### Performance Targets
- <100ms AI inference response time
- Full offline capability
- 0 bytes to cloud storage for user data
- Model size optimization through 4-bit quantization

## Key Products

1. **Where Is** - Family location intelligence app
2. **GutFlow** - Digestive health AI assistant
3. **BudgetAI** - Financial intelligence (Q2 2025)
4. **StudyBuddy** - Educational assistant (Q3 2025)
5. **HealthVault** - Medical records AI (Q4 2025)

## Testing Approach

When implementing features:
1. Ensure complete offline functionality
2. Verify no data leaves device during normal operation
3. Test AI inference performance (<100ms target)
4. Validate data export functionality
5. Check encryption for any relay communications

## Important Files

- `localfirst-movement-prd.md` - Complete product requirements and company vision