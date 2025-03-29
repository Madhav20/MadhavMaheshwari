## Read Me
This is an Android app built using Kotlin, Jetpack Compose, and MVVM architecture. The app fetches content from a given website and processes it in parallel to display three key pieces of information:

1. 15th Character: Displays the 15th character of the content.
2. Every 15th Character: Shows every 15th character in a horizontal grid.
3. Word Count: Counts occurrences of each unique word and displays them in a two-column list.

🏗️ Tech Stack
- Language: Kotlin
- UI Framework: Jetpack Compose
- Architecture: MVVM
- Dependency Injection: Dagger Hilt
- Networking: Retrofit + OkHttp
- Coroutines & Flow: For asynchronous operations
- Unit Testing: JUnit, Turbine, and MockK

## Project 
```
app/
│
├── di/                    # Dependency Injection (Dagger Hilt modules)
│
├── home/                  # Core feature module
│   ├── repository/        # Repository for fetching & processing content
│   │   ├── ContentActivity.kt # Entry Point
│   │   ├── ContentApi.kt  # Retrofit API interface
│   │   ├── ContentView.kt 
│   │   ├── ContentViewModel.kt  # ViewModel handling business logic
├── utils/                 # Utility classes & helpers
│   ├── ConnectivityCheckInterceptor.kt  # Network connectivity check
│   ├── Constants.kt       # App-wide constants
│   ├── DispatcherProvider.kt  # Coroutine dispatcher provider
│   ├── LoadingIndicator.kt  # UI loading state handling
│   ├── Status.kt          # Sealed class for API states (Success, Error, Loading)
│   ├── UIState.kt         # State management for UI
│   ├── UIStateHandler.kt  # Handles UI state changes
│
├── MyApplication.kt       # Application class for Hilt
├── com/test/              # Unit Tests
```
