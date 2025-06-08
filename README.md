# Course Subscription Application

## Overview
This is a ServiceNow-based course subscription application where learners can view available courses and subscribe to them. Built using ServiceNow platform with UI Builder for the frontend interface.

## Features Implemented

### PRD01: Course List - COMPLETED
- Displays list of 6 available courses from ServiceNow backend
- Shows course details: Title, Description, Duration  
- Responsive layout using UI Builder repeater component
- Connected to ServiceNow course table

![Course Listing](screenshots/course_listing.png)
*Course listing page displaying all available courses*

![Course Details](screenshots/card_container.png)
*Individual course cards showing title, description, and duration*

### PRD02: Course Subscription - PARTIALLY COMPLETED
- Subscribe buttons integrated into each course card
- Functional event handling for button clicks
- Modal confirmation dialog implemented
- User can interact with subscription flow

![Subscribe Buttons](screenshots/button_handlers.png)
*Subscribe buttons visible on each course card*

![Subscription Modal](screenshots/modal_dialog.png)
*Confirmation modal appears when user clicks subscribe*

## Technical Implementation

### Backend Setup
- ServiceNow development instance configured
- Course table created with sample data (6 courses)
- Subscription table structure created

![Course Table](screenshots/courses_backend.png)
*ServiceNow course table with populated sample data*

![Subscription Table](screenshots/courseList_dataResources.png)
*Data resources and subscription table configuration*

### Frontend Setup
- UI Builder used for interface design
- Repeater component for course display
- Event handlers configured for user interactions

![UI Builder Events](screenshots/button_handlers.png)
*Event handler configuration in UI Builder*

![Debug Output](screenshots/console_print.png)
*Debug information showing repeater functionality*

## Known Issues

### Subscription Recording Problem
The main technical challenge: while the UI interaction works correctly, subscription records are not being created in the ServiceNow subscription table when users confirm their subscription.

**What Works:**
- Subscribe button clicks trigger events
- Modal confirmation dialog appears
- User can click Yes/Cancel

**What Doesn't Work:**
- No records created in subscription table after confirmation
- Backend data insertion fails silently

## Incomplete Features

Due to the subscription recording issue:
- Creating subscription records (core PRD02 requirement)
- Unsubscribe functionality
- Duplicate subscription prevention
- Visual feedback for successful subscriptions
- Robot Framework test suite

## User Interaction Flow

1. User views course listing page
2. User sees available courses with details
3. User clicks "Subscribe" on desired course
4. Confirmation modal appears: "Confirm Subscription?"
5. User clicks "Yes" to confirm
6. **Issue**: No subscription record is created

## Technical Architecture

- **Platform**: ServiceNow
- **Frontend**: UI Builder with repeater components
- **Backend**: ServiceNow tables (Course, Subscription)
- **Data**: 6 sample courses with titles, descriptions, durations

## Installation and Setup

1. Clone this repository
2. Import ServiceNow application files from `x_quo_coursehub/` folder
3. Configure ServiceNow development instance
4. Access the application through ServiceNow interface

## Testing

Robot Framework test suite was planned but not implemented due to incomplete subscription functionality.

## Future Improvements

1. Fix subscription record creation in backend
2. Implement unsubscribe functionality
3. Add duplicate subscription prevention
4. Create comprehensive test suite
5. Add error handling and user feedback

## Links
- [Original Repo](https://bitbucket.org/qualdatrix/coursehub/src/main/)

## Author
Mohan Giri
