# API Documentation Plan for Narra Backend

## Overview
This document outlines the plan for documenting the Narra backend API endpoints for internal team use. The documentation will be built using Mintlify with MDX syntax, maintaining the existing starter kit structure as reference.

## Target Audience & Tone
- **Primary audience**: Internal Narra team members
- **Experience levels**: From newcomers needing comprehensive onboarding to senior developers requiring quick reference
- **Documentation tone**: 
  - Clear and conversational, avoiding unnecessary jargon
  - Include context about "why" decisions were made, not just "how" things work
  - Balance depth for learning with brevity for quick lookups
  - Use internal terminology and reference our specific tools/services
  - Include gotchas and lessons learned from real usage

## Key Narra Concepts

### Lenses
In Narra, **lenses** are the different categories of clinical data we track for patients:
- **Vitals** - Blood pressure, heart rate, temperature, etc.
- **Medications** - Current and past medications
- **Labs** - Laboratory test results
- **Allergies** - Patient allergies and reactions
- **Problems** - Medical conditions and diagnoses
- **Imaging** - Radiology and imaging results
- **Plans** - Treatment plans and care protocols
- **Family/Social History** - Family medical history and social factors

These lenses are central to how we organize and retrieve patient data throughout the backend.

### Logs
**Logs** are clinical updates posted by healthcare providers throughout the day to:
- Record patient status updates and observations
- Keep medical teams aligned on patient care
- Help individual providers track their patients' progress
- Create a chronological record of patient interactions

Logs can include various lenses data and are processed by our AI to categorize and extract relevant information.

## Active Endpoints to Document

### Priority 1 - Core Clinical Features
1. **Chat V2** (`/api/v1/chat_v2`) - AI-powered clinical assistant
2. **Patient Data** (`/api/v1/patient-data`) - Lenses data management (vitals, labs, medications, etc.)
3. **Log Routes** (`/api/v1/log`) - Clinical logs creation and processing

### Priority 2 - Data Entry Support
4. **Meta Routes** (`/api/v1/meta`) - Form field metadata for lenses data entry
5. **Upload Routes** (`/api/v1/uploads`) - Media file management for logs
6. **PDF Upload Routes** (`/api/v1/pdf-uploads`) - Document processing for clinical records

### Priority 3 - AI/ML Features
7. **Vision Log Routes** (`/api/v1/vision-logs`) - Image analysis
8. **Audio Transcription Routes** (`/api/v1/audio-transcriptions`) - Audio processing

### Priority 4 - Supporting Services
9. **Media Routes** (`/api/v1/media`) - Media deletion
10. **FCM Routes** (`/api/v1/fcm`) - Push notifications
11. **RevenueCat Routes** (`/api/v1/revenuecat`) - Subscription management

## Documentation Structure for Each Endpoint

Each endpoint documentation will include:

1. **Overview**
   - Purpose and use cases (with internal context)
   - Key features and why we built them this way
   - Authentication requirements
   - Common pitfalls to avoid

2. **Endpoints**
   - HTTP method and path
   - Description with business logic context
   - Request parameters (path, query, body)
   - Request/response models with examples
   - Error responses and what they mean for our system

3. **Code Examples**
   - cURL examples for quick testing
   - Python/JavaScript examples matching our internal tools
   - Real scenarios from our app usage
   - Debugging tips from team experience

4. **Integration Notes**
   - Related endpoints and typical workflows
   - How this fits into our larger architecture
   - Performance considerations we've learned
   - Links to relevant internal tools/dashboards

## Documentation Approach

1. **Keep existing Mintlify starter pages** as syntax reference
2. **Create new section** in navigation: "Backend API"
3. **Use OpenAPI spec** where available for consistency
4. **Include real examples** from the codebase
5. **Document authentication** patterns clearly
6. **Highlight streaming endpoints** (SSE) with special attention

## Navigation Structure

```
Backend API/
├── Overview
├── Authentication
├── Core Features/
│   ├── AI Chat (chat_v2)
│   ├── Patient Data
│   └── Patient Logs
├── Data Management/
│   ├── Form Metadata
│   ├── Media Uploads
│   └── Document Processing
├── AI Services/
│   ├── Vision Analysis
│   └── Audio Transcription
└── Platform Services/
    ├── Push Notifications
    └── Subscriptions
```

## Next Steps

1. Start with Chat V2 endpoint as it's the most complex
2. Create template structure that can be reused
3. Document one endpoint at a time, taking breaks between each
4. Update navigation in docs.json after each endpoint

## Questions to Clarify

1. Should we include internal implementation details or just API contracts?
2. Do we need to document deprecated endpoints or just active ones?
3. What level of code examples do you prefer (basic vs comprehensive)?
4. Should we include performance considerations and rate limits?

## Example Documentation Style

For newcomers:
> "The Chat V2 endpoint is the heart of our AI assistant. It's where user messages get transformed into helpful clinical insights. Think of it as our GPT-4 orchestrator that knows when to search online, query patient data, or tap into our knowledge base."

For senior developers:
> "SSE streaming with 30-second heartbeat. Tool calls are parallelized when possible. Patient context injection happens pre-prompt. Check CloudWatch for latency metrics."