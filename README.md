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
- KT Lint for code formatting

## Project 
```
app/
│
├── di/                            # Dependency Injection (Dagger Hilt modules)
│
├── home/                          # Core feature module
│   ├── repository/                # Repository for fetching & processing content
│   │   ├── ContentActivity.kt     # Entry Point
│   │   ├── ContentApi.kt          # Retrofit API interface
│   │   ├── ContentView.kt 
│   │   ├── ContentViewModel.kt    # ViewModel handling business logic
├── utils/                         # Utility classes & helpers
│   ├── ConnectivityCheckInterceptor.kt  # Network connectivity check
│   ├── Constants.kt               # App-wide constants
│   ├── DispatcherProvider.kt      # Coroutine dispatcher provider
│   ├── LoadingIndicator.kt        # UI loading state handling
│   ├── Status.kt                  # Sealed class for API states (Success, Error, Loading)
│   ├── UIState.kt                 # State management for UI
│   ├── UIStateHandler.kt          # Handles UI state changes
│
├── MyApplication.kt               # Application class for Hilt
├── com/test/                      # Unit Tests
```

There are total 13 unit test cases under test package covering repository and viewmodel functions.

## Screenshot
- Click on Load Content button to fetch the data from Truecaller website.
- <img src="https://github.com/user-attachments/assets/aa168a87-5bcc-4363-bb8b-d808bd197108" width="300" height="550"/>
- A loader will be visible for couple of second.
- As soon as api fetch the data it will be visible to the user
- <img src="https://github.com/user-attachments/assets/16519498-2796-41c8-bc03-7ed68405afc5" width="300" height="550"/>
- Some operation take time for those a loading text is visible.
- <img src="https://github.com/user-attachments/assets/358a01ea-1f97-4a84-83eb-789f8788435c" width="300" height="550"/>
- Every15thCharacter information is shown in a horizontal scrollable view and word count is shown in vertically scrollable grid.
- <img src="https://github.com/user-attachments/assets/39db33e3-72e1-4b50-871b-90f2b7f23aeb" width="300" height="550"/>


