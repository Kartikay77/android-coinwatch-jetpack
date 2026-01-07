# CoinWatch - Android Crypto Tracker 📱

![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-purple?style=flat-square&logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack_Compose-green?style=flat-square&logo=android)
![Platform](https://img.shields.io/badge/Platform-Android_14.0+-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

A modern, native Android cryptocurrency tracking application built with **Kotlin** and **Jetpack Compose**. This project demonstrates industry-standard mobile architecture, integrating real-time REST APIs with a clean, reactive UI.

![App Screenshot](https://github.com/Kartikay77/android-coinwatch-jetpack/blob/main/Media/android_paypal.png?raw=true)

---

## 🚀 Key Features

* **Modern UI**: Built 100% with **Jetpack Compose**, Android's modern toolkit for building native UI using Material Design 3.
* **Real-Time Data**: Fetches live cryptocurrency data from the **CoinCap API**.
* **Clean Architecture**: Follows **MVVM** principles (Separation of Concerns) for scalable and testable code.
* **Robust Networking**: Uses **Retrofit 2** and **Gson** for efficient, type-safe API calls.
* **Asynchronous Processing**: Leverages **Kotlin Coroutines** for non-blocking network operations, ensuring a smooth user experience.
* **Error Handling**: Includes robust fallback mechanisms (Mock Data) to handle network failures gracefully.

---

## 🛠️ Tech Stack

* **Language**: Kotlin
* **UI Framework**: Jetpack Compose (Material Design 3)
* **Networking**: Retrofit 2, OkHttp, Gson
* **Concurrency**: Kotlin Coroutines & Flow
* **Architecture**: MVVM (Model-View-ViewModel) pattern
* **IDE**: Android Studio

---

## 📂 Code Structure

The app is structured to separate UI, Data, and Business Logic:

1.  **Data Layer (`Coin`, `CoinCapResponse`)**:
    * Immutable data classes that model the JSON response from the API.
2.  **Network Layer (`RetrofitInstance`, `CryptoApi`)**:
    * Singleton pattern for the Retrofit client to ensure efficient resource usage.
    * Suspended functions for asynchronous API calls.
3.  **UI Layer (`MainActivity`, `CoinScreen`)**:
    * Composable functions that reactively update based on state changes (`remember` and `LaunchedEffect`).

---

## 💻 Installation & Run

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/Kartikay77/android-coinwatch-jetpack.git](https://github.com/Kartikay77/android-coinwatch-jetpack.git)
    ```
2.  **Open in Android Studio**:
    * Select "Open" and navigate to the cloned folder.
    * Wait for Gradle Sync to complete.
3.  **Run the App**:
    * Select an Emulator (e.g., Pixel 8 Pro).
    * Click the green **Play** button.

---

## 🔍 Code Highlights

### Jetpack Compose UI
Declarative UI code that is easy to read and maintain:

```kotlin
@Composable
fun CoinItem(coin: Coin) {
    Card(
        elevation = CardDefaults.cardElevation(defaultElevation = 4.dp),
        colors = CardDefaults.cardColors(containerColor = Color.White)
    ) {
        // UI Layout logic...
    }
}
```
## Retrofit Networking

### Simple, type-safe API definition:

```
interface CryptoApi {
    @GET("v2/assets")
    suspend fun getAssets(): CoinCapResponse
}
```
👤 Author
Kartikay Gupta Software Engineer | Android & iOS Specialist
