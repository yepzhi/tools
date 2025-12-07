# OSINT Social Analyzer

A web-based tool to search for profiles across 1000+ social media platforms.

## Features
- Search by Username, Email, or Phone
- Real-time analysis
- Dark mode UI with glassmorphism design

## Setup
1. Clone the repository
2. Open `index.html` in your browser

## Backend Requirement
This is a **Frontend Interface**. To perform real searches, it must connect to a running instance of [Social Analyzer](https://github.com/qeeqbox/social-analyzer).

1. Deploy Social Analyzer (Docker/VPS/Local).
2. Update the `API_URL` in `index.html` to point to your instance (e.g., `http://localhost:9005` or your server IP).
3. The current default is set to a demo/placeholder IP.

## Usage
Enter a username and click Search to find social media profiles.
