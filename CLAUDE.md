# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Idios (idios.cloud) is building a technology stack and application ecosystem that enables complete data sovereignty. The name comes from ancient Greek meaning "one's own, personal, private." Idios creates a personal cloud architecture where all apps run in the user's own infrastructure (devices, home storage, personal cloud) with an intelligent stateless proxy called the Herald that manages external interactions without storing data.

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

## Key Architecture Components

### The Idios (Personal Infrastructure)
- User's devices (phone, tablet, laptop)
- Home infrastructure (NAS, home server)
- Personal cloud storage (iCloud, Google Drive, Dropbox)
- All apps run HERE in the user's sovereign space

### The Herald (Intelligent Proxy)
- Stateless message relay in the cloud
- Receives messages while devices are offline
- Brokers AI requests when local models aren't sufficient
- Auto-expires all data (configurable TTL)
- Zero permanent storage
- Acts as a trusted messenger between the idios and external world

## Key Products

1. **Where Is** - Family location coordination without surveillance
2. **GutFlow** - Medical data that stays medical
3. **BudgetAI** - Financial intelligence, truly yours (Q2 2025)
4. **StudyBuddy** - Education without data harvesting (Q3 2025)
5. **HealthVault** - Medical records meet sovereignty (Q4 2025)

## Testing Approach

When implementing features:
1. Ensure complete offline functionality
2. Verify no data leaves device during normal operation
3. Test AI inference performance (<100ms target)
4. Validate data export functionality
5. Check encryption for any relay communications

## Important Files

- `localfirst-movement-prd.md` - Complete product requirements and company vision