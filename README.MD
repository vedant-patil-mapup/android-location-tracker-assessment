# MapUp - Android Developer Assessment

## Overview

The objective of this assessment is to build a **GPS Location Tracker application** that demonstrates your proficiency in Android development, background services, local data persistence, and API integration. You'll create an app that tracks user location in the background, stores session data locally, and displays route information with optional toll calculation integration.

## Timeline

**Duration: 14 days**

## Application Requirements

### Core Features (Must Have)

Build an Android application with the following capabilities:

| Feature                       | Description                                                                                      |
| ----------------------------- | ------------------------------------------------------------------------------------------------ |
| **Location Tracking Service** | A foreground service that tracks user location continuously                                      |
| **Background Persistence**    | Tracking must continue even when app is backgrounded or removed from recents                     |
| **Persistent Notification**   | Display a notification while tracking is active with a "Stop" action                             |
| **Local Storage**             | Store GPS tracks locally with session-based organization                                         |
| **Session History**           | View list of all previous tracking sessions                                                      |
| **Session Details**           | View detailed GPS track for any saved session                                                    |
| **Map Visualization**         | Display the tracked route on a map under session details with route details (distance, duration) |

### Bonus Features (Good to Have)

These features are not required but will strengthen your submission:

| Feature                           | Description                                                                  |
| --------------------------------- | ---------------------------------------------------------------------------- |
| **TollGuru API Integration**      | Send GPS tracks to TollGuru API and display toll calculation results         |
| **Dashboard Stats**               | Show summary stats like total tracked sessions, total distance covered, etc. |
| **Survives Process Death**        | Service continues tracking even if system kills the app process              |
| **Battery Optimization Handling** | Proper handling of Doze mode and battery optimization                        |
| **GPS Accuracy Indicators**       | Display accuracy metrics and handle poor GPS signal gracefully               |
| **Export Functionality**          | Export session data as CSV/GPX                                               |
| **Dark Mode Support**             | Proper theming for light/dark modes                                          |

## Technical Notes

Use whatever technologies, libraries, and architecture patterns you're comfortable with.

**For geographic calculations:**

- You can use [Mapbox Turf](https://docs.mapbox.com/android/java/guides/install) or similar libraries
- For polyline encoding/decoding, refer to online resources or use the conversion code provided in this repository

## TollTally API Integration

**API Documentation:** [TollTally - Route encoded polyline endpoint](https://tollguru.com/toll-api-docs#route-encoded-polyline)

This endpoint accepts polyline or direct GPS coordinates in the request body. Refer to the documentation for request/response formats.

**API Key:** Create an account and subscribe to the TollTally API (not TollGuru API) trial plan at [https://platforms.mapup.ai](https://platforms.mapup.ai) - and get your API key from the "Home" tab on the left side bar.

**Important Note**: The trial is available for 7 days after subscribing, so subscribe once you've completed the must-have features. The free tier has a limit of 15 transactions per day (approx. 10-15 requests based on the length of the route) — reuse API responses during testing to avoid exhausting your daily quota.

## Video Submission Requirements

**Duration: 30-45 minutes**

Your video submission is a critical part of this assessment. Structure your video roughly as follows:

| Section                          | Duration  | What to Cover                                                                                                                                                                                                                                      |
| -------------------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **App Demo**                     | 10-12 min | Full working demo — permissions flow, start tracking, show location being recorded, background the app, kill from recents, prove tracking continues, stop via notification, view session history, select a session, show route on map with details |
| **Implementation Deep Dive**     | 12-18 min | Walk through the codebase — project structure, architecture choices, service implementation, location tracking logic, data storage approach, map rendering. Show actual code, not slides.                                                          |
| **Gaps, Improvements & Roadmap** | 10-15 min | What's incomplete and your plan to finish it with time estimates. If complete: edge cases not handled, what you'd refactor with more time, how you'd make it production-ready, how this could scale.                                               |

**Recording:** Use any screen recording tool (Loom, OBS, etc.). Upload to YouTube/Vimeo (unlisted), Loom, or Google Drive (shared with the collaborator emails listed below) and include the link in your README.

## Evaluation Criteria

Your submission will be evaluated based on:

- **Core Functionality**: All must-have features working correctly
- **Code Quality**: Clean architecture, readable code, proper abstractions
- **Android Best Practices**: Lifecycle handling, permission management, background execution
- **Video Presentation**: Clear communication, technical depth, self-awareness about limitations
- **User Experience**: Intuitive interface, proper error handling

## Submission Guidelines

**Repository Setup:**

1. Create a **private** GitHub repository for your implementation
2. Include a README with:
   - Setup instructions
   - Architecture overview
   - Any known limitations
   - Link to your video submission
3. Add the following email addresses as collaborators:
   - vedantp@mapup.ai
   - ajayap@mapup.ai
   - dewanshp@mapup.ai
   - asijitp@mapup.ai

Finally, fill out the Google Form you received via email to submit the assessment for review.

### AI and LLM Usage

We encourage the use of AI and LLM tools for this assessment! However, you must understand what you're building and be able to explain your implementation decisions.
