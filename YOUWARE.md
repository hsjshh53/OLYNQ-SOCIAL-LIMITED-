# OLYNQ SOCIAL - Project Documentation

## Project Overview
OLYNQ SOCIAL is a mobile-first social networking application built as a Single Page Application (SPA) contained within a single `index.html` file. It features a modern glassmorphism UI and real-time functionality powered by Firebase.

## Technology Stack
- **Frontend**: Vanilla JavaScript (ES Modules), HTML5
- **Styling**: Tailwind CSS (via CDN)
- **Backend**: Firebase v9.22.0 (Authentication, Realtime Database)
- **Icons**: FontAwesome 6.4.0

## Architecture
The entire application logic resides in `index.html`.
- **State Management**: A global `state` object tracks users, posts, chats, and UI state.
- **Routing**: A custom `router` object handles navigation between views (home, communities, messages, profile, etc.).
- **Data Sync**: Firebase `onValue` listeners provide real-time updates for all data.

## Key Features
- **Authentication**: Email/Password login and signup.
- **Home Feed**: Real-time posts with media support (Base64 images/videos), likes, comments, and sharing.
- **Stories**: Users can post text, images, and videos to their story, which expires after 24 hours.
- **Communities (Groups)**: 
    - **Feed**: Dedicated post feed for group members.
    - **Chat**: Real-time group chat.
    - **Admin Tools**: Creator/Admins can manage members (promote, demote, remove) and delete the group.
- **Messaging**: Real-time private chat with user status and media sharing.
- **Profile**: User profiles with cover photos, bio, and "Follow" functionality. Users can view each other's profiles.
- **Search**: User search functionality.

## Recent Updates
- **Groups Overhaul**: Added Feed, Chat, and Admin tabs to groups. Implemented full admin permissions (promote/demote/remove members).
- **Sharing**: Added ability to share posts to your own feed.
- **Stories**: Enhanced stories with media support and a dedicated viewer.
- **Performance**: Implemented lazy loading for images.
- **Chat System**: Added sender's profile picture to outgoing messages. Fixed broken profile pictures and missing names in the chat list.
