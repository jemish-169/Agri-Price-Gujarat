# Agri-price

## Features

### Android App

- **Offline-first architecture**: Reduces network calls by caching market and crop data locally using Room database.
- **Home**: Shows recently sold prices for selected markets and crops.
- **Crop**: Selecting a crop shows markets with min/max prices of last sold in each market.
- **Market**: Selecting a market displays all sold crops with min/max prices of last updated date.
- **Date filtering**: Users can view data of past 100 days in both crop and market sections.
- **Settings**: Users can reselect their preferences and switch the app theme.

### Backend & Database

- **Data pipeline**: A Python script periodically collects crop pricing data from public sources, processes it, and pushes it to Supabase.
- **Centralized storage**: Supabase acts as the single source of truth for all crop names, market names, and price entries.
- **Data handling**: Only the latest 100 days of data are retained, and unused crop or market records are automatically removed.

## Technology Stack

- **Android-App**:
  - **Android (Kotlin)** – Native Android development using Jetpack Compose  
  - **Jetpack Compose** – Declarative UI toolkit for clean, efficient layouts  
  - **Coroutines** – Managing background tasks smoothly  
  - **Koin** – Lightweight Dependency injection  
  - **MVVM + Clean Architecture** – Ensures a scalable, maintainable, and test-friendly codebase  
  - **Material Design** – Follows Google’s UI/UX guidelines for intuitive design  
  - **Animations** – Enhances user experience with meaningful transitions and effects
  - **Room Database** – For offline first approach and serving cached data on failure
  - **Navigation-3** – Navavigation between modules with Back-stack ownership
  - **Jetpack-DataStore** – Flow based user preference saving

- **Backend**:
  - **Python** – Getting data from public data-sources and updating database

- **Database & Cloud**:
  - **Supabase** – Backend-as-a-service for Database, Single source of truth  

## Screenshots

| Crop According | Market According |
|-------------|-------------|
| ![1](https://github.com/user-attachments/assets/c2b5cf26-e8db-4a2f-8459-67b9a52d1d93) | ![2](https://github.com/user-attachments/assets/86b5ff8e-ad29-4390-9c29-ecd6ace5f494) |

| Crop Selection | Crop Detail |
|-------------|-------------|
| ![3](https://github.com/user-attachments/assets/6abd931b-067e-4615-b1ed-e57bb94406a3) | ![4](https://github.com/user-attachments/assets/1d12cc56-dda1-4284-9afc-bce33eacad57) |

| Market Selection | Market Detail |
|-------------|-------------|
| ![5](https://github.com/user-attachments/assets/5f1d9794-1444-45e0-a0fa-300a6fef6ed3) | ![6](https://github.com/user-attachments/assets/868c9e9d-1a55-4e0a-89f3-39ccfdd27610) |

| Date Selection | History Screen |
|-------------|-------------|
| ![7](https://github.com/user-attachments/assets/fae72c0d-d3b0-430e-b661-304e2b9e274a) | ![Screenshot_2025-07-25-02-44-38-387_com elite agriprice](https://github.com/user-attachments/assets/47ca62d0-e706-4742-8471-ec2dde9b6658) |
