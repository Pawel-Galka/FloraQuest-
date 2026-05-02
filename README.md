<div align="center">
  <h1>🌿 FloraQuest</h1>
  <p><em>Turning plant care into a rewarding, gamified experience.</em></p>

  ![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
  ![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
  ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
  ![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
</div>

<br />

> **Note:** The source code for FloraQuest is currently private. Because I am actively preparing the application for a commercial release on the App Stores, the repository remains closed-source. This case study serves as an in-depth overview of the project, its features, architecture, and my design philosophy.

---

## 📖 Overview

Taking care of houseplants shouldn't feel like maintaining a spreadsheet. I created **FloraQuest** to transform plant care from a mundane chore into an engaging, rewarding, and gamified experience. 

FloraQuest is a mobile application that helps users track their plant collection, learn how to care for them properly, and earn rewards for keeping their "Virtual Windowsill" thriving. By combining detailed botanical data with smooth, gesture-driven UI and game-like mechanics (XP, streaks, and levels), the app keeps users motivated to nurture their green friends.

## ✨ Current Features & UI Showcase

### 1. The Virtual Windowsill (Dashboard)
The core of the app is the user's personal plant collection. 
* **Room Management:** Users can organize plants by rooms (e.g., Living Room, Bedroom). I implemented a custom drag-and-drop interaction using `PanResponder` and `Animated` APIs, allowing users to intuitively long-press and reorder their rooms horizontally.
* **Smart Sorting:** Plants can be sorted alphabetically or by "thirst level," ensuring that the plants needing the most urgent care are always at the top of the feed.
* **Daily Quests:** A dynamic header tracks the percentage of thriving plants versus those that need water, offering a quick visual summary of the day's tasks.

<!-- Tip: Place a screenshot or GIF of the Windowsill here -->
<!-- <img src="link_to_image_or_gif" width="300" /> -->

### 2. Gamified Plant Care
Watering a plant triggers a highly rewarding, custom-built animation system. 
* **Particle Engine:** I engineered a lightweight, randomized particle system (leaves and sparkles) that erupts on the screen when a plant is watered.
* **Progression System:** Users earn "Glows" (XP) and maintain a watering streak, displayed in a frosted-glass top navigation bar.

<!-- Tip: Place a GIF of the watering animation here -->
<!-- <img src="link_to_watering_gif" width="300" /> -->

### 3. Gesture-Driven Plant Deep Dive
When a user taps on a plant, they are greeted with a beautifully animated, highly detailed bottom sheet.
* **Frictionless UX:** The modal uses a custom swipe-to-close gesture that feels natural and responsive.
* **Interactive User Gallery:** I built a custom image gallery featuring pinch-to-zoom mechanics. To ensure a premium feel, the math behind the zoom eliminates the jarring "bungee" effect upon release, snapping the image back perfectly. Additionally, photo metadata (author, description) seamlessly fades out when the user zooms in to inspect plant details.
* **Comprehensive Care Guides:** Information is categorized into actionable chunks (Climate, Sunlight, Soil, Toxicity) with expandable Deep Dive cards for advanced tips (e.g., how to build a moss pole or mix aroid soil).

### 4. Smart Plant Discovery (Add Flow)
Adding a new plant is split into a streamlined, multi-step flow.
* **Search Engine:** A responsive 2-column grid layout for browsing the database. It filters results in real-time by both common and Latin names.
* **Contextual Search History:** The search bar remembers recent queries. To keep the UI clean, the "Recent Searches" history (complete with individual delete buttons) only appears when the user explicitly focuses on the input field, keeping the main discovery feed uncluttered.

## 🚀 Future Roadmap

While the frontend architecture and user experience are currently highly polished, FloraQuest is an evolving product. Here is what I am implementing next:

- [ ] **Live Backend & API Integration:** Transitioning from the current localized mock database to a robust cloud backend (e.g., Node.js/PostgreSQL or Firebase) to handle user authentication, cloud syncing, and real-time database updates.
- [ ] **AI-Powered Plant Identification:** Activating the currently mocked "Open Camera" feature. I plan to integrate a machine-learning vision API so users can simply snap a photo of a plant to identify it, instantly pulling its care profile into their Windowsill.
- [ ] **Push Notifications & Background Tasks:** Implementing local and push notifications to alert users when a plant's thirst level reaches a critical point, ensuring no plant is ever forgotten.
- [ ] **Social & Community Features:** Allowing users to publish their plant progress photos directly to the global "User Gallery" to share their botanical milestones with other app users.

## 💡 Conclusion

FloraQuest is a testament to the idea that utility apps can be both highly functional and joyful to use. By handling complex state management, custom physics-based animations, and strict UX principles completely solo, I am building an app that looks, feels, and performs like a top-tier commercial product.
