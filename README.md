# 🌸 WeatherApp ⛅

A delightful Android weather app built with **Kotlin** and the **MVVM** architecture pattern. WeatherApp delivers real‑time forecasts from OpenWeatherMap and wraps them in *cute, mood‑lifting wallpapers* that change with the sky. Perfect for developers looking for a clean codebase and users who crave a little aesthetic joy alongside their weather updates.

---

## ✨ Features

|                             |                                                                    |
| --------------------------- | ------------------------------------------------------------------ |
| **📡 Real‑time Forecasts**  | Current weather for any city via OpenWeatherMap API                |
| **🎀 Adorable Wallpapers**  | Dynamic backgrounds for sunny, rainy, cloudy, and snowy conditions |
| **🔍 Search & Location**    | Auto‑detect device location or search by city name                 |
| **🚀 MVVM Under the Hood**  | Clean separation of concerns with ViewModel + LiveData             |
| **⚡ Pull‑to‑Refresh**       | Manual refresh to grab the latest data                             |
| **🌗 (Optional) Dark Mode** | Inherits system night mode for comfy late‑night checks             |

> **Note:** *Offline caching is not yet implemented. An internet connection is required.*

---

## 🖼️ Screenshots
![cloudy](https://github.com/user-attachments/assets/bc6dbbee-c7b4-4ad9-a126-ac7348fd490f)
![splash screen](https://github.com/user-attachments/assets/fdec9b7e-4678-4989-b17d-b7f324b720da)
![rain](https://github.com/user-attachments/assets/641a8f96-6a17-4b4e-acfb-9e210376fba3)
![clear](https://github.com/user-attachments/assets/afa4e9ca-7118-400a-b1a9-00ff95f3ec4f)


---

## 🛠 Tech Stack

| Layer                | Library / Tool                    |
| -------------------- | --------------------------------- |
| Language             | Kotlin                            |
| Architecture         | MVVM + Repository pattern         |
| Networking           | Retrofit • OkHttp • Moshi/Gson    |
| Async & Lifecycle    | Coroutines • LiveData • ViewModel |
| Dependency Injection | (Optional) Hilt/Dagger            |
| UI                   | XML Layouts • Material Components |
| Build                | Gradle (KTS)                      |

---

## 🚀 Getting Started

### 1. Prerequisites

* **Android Studio Flamingo | 2023.1.1** or newer
* **Android SDK 24+** (minSdk = 24)
* **A free OpenWeatherMap API key** → [https://openweathermap.org/api](https://openweathermap.org/api)
* A device or emulator with internet access

### 2. Clone the Repository

```bash
git clone https://github.com/anushruti-peanut/weather_app.git
cd weather_app
```

### 3. Add Your API Key

WeatherApp expects the key in a project‑level `gradle.properties` (preferred) **or** a compile‑time resource. Pick one of the two methods below:

<details>
<summary>✏️ <b>gradle.properties (recommended)</b></summary>

1. Open or create the file `<project‑root>/gradle.properties`.
2. Add:

   ```properties
   OPEN_WEATHER_API_KEY="your_key_here"
   ```
3. Sync Gradle. The key is accessed securely via `BuildConfig.OPEN_WEATHER_API_KEY`.

</details>

<details>
<summary>📄 <b>strings.xml (quick test)</b></summary>

1. Open `app/src/main/res/values/strings.xml`.
2. Add:

   ```xml
   <string name="open_weather_api_key">your_key_here</string>
   ```
3. Rebuild the project.

</details>

### 4. Build & Run

* Click **Run ▶** in Android Studio, or use Gradle:

```bash
./gradlew :app:installDebug
```

The app launches on the selected device. Grant location permission (optional) and enjoy the cute forecast!

---

## 🏗️ Project Architecture

```
com.anushruti.weatherapp
│
├─ data            // DTOs, Retrofit service, repository implementation
│   ├─ remote      // API layer
│   └─ model       // Data models mapped to UI state
│
├─ domain          // Repository interface (if using Clean Architecture)
│
├─ ui              // Activities / Fragments + ViewModels
│   └─ bindings    // XML layout bindings & adapters
│
└─ utils           // Constants, extensions, helpers
```

* **ViewModel** exposes immutable `LiveData<UiState>` to the UI.
* **Repository** fetches from network (future: cache to Room).
* **DI** ready – swap a fake repository in tests.

---

## 🧭 Roadmap

* [ ] 📅 7‑day & hourly forecasts
* [ ] 🎨 Theme selector (pastel, dark, AMOLED)
* [ ] 🏷️ Weather widgets / complications


---


## 🙋‍♀️ Author & Contact

Made with ☕, Kotlin ♥ and a sprinkle of 🌸 by **[Anushruti](https://github.com/anushruti-peanut)**.

* GitHub Issues – best place for bugs & feature requests
* Feel free to connect on LinkedIn or drop a star ⭐ if this project brightened your day!


