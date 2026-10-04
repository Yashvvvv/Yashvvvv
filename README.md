# Hi, I'm Yash 👋

**Android Developer · Kotlin, Jetpack Compose, Kotlin Multiplatform · Spring Boot on the backend**

I build Android apps and the backends behind them. At **[AppStorys](https://appstorys.com)** I ship features in a production in-app engagement SDK that runs inside other companies' Android apps, and I re-architected it around a Kotlin Multiplatform shared core that backs Android, Flutter and React Native. Outside work I build products end to end: the API, the auth, the web console and the Android client.

📍 Noida / Delhi, India · B.Tech AI/ML, GCET (2026) · Open to Android and SDE roles

[Portfolio](https://yashsharma054.dev) · [LinkedIn](https://www.linkedin.com/in/yash-sharmagg) · [Email](mailto:sharmayashh054@gmail.com) · [Twitter](https://twitter.com/_Yash_ss)

---

## 💼 Work

**Android Developer, AppStorys (AppVersal Pvt. Ltd.)** · Noida · Dec 2025 – present

- Ship features in a production **in-app engagement SDK** used by host Android apps: interactive stories, surveys, overlays and CTA flows.
- Build and optimise **Jetpack Compose** UI with unidirectional state, lifecycle-safe side effects and recomposition-aware rendering.
- Re-architected the SDK around a **Kotlin Multiplatform shared core**, splitting business logic from presentation so one codebase backs Android, Flutter and React Native.
- Maintain the **Kotlin, Flutter and React Native binding layers** over that core, keeping integration behaviour consistent across host apps.

---

## ⭐ Flagship: [VenueSync](https://github.com/Yashvvvv/VenueSync) · [live](https://venuesync.pages.dev/)

**An event ticketing platform I built end to end.** Organisers publish events, attendees buy tickets, and door staff scan QR codes at entry.

| Layer | What I built |
|---|---|
| 📱 **Android** | Kotlin + Jetpack Compose client with Hilt and Ktor. Auth0 sign-in through AppAuth, with tokens kept in the Android Keystore. Ticket purchase, My Tickets with QR codes, and a staff scanner built on ML Kit. Tickets sit in an **encrypted on-device store**, so they still open at the venue door without signal. |
| ⚙️ **Backend** | Spring Boot REST API on PostgreSQL. **Race-condition-proof seat allocation with JPA pessimistic locking**: purchases are atomic and idempotent, and ticket validation is race-safe, so a seat can't be oversold or a ticket scanned in twice. Server-side QR generation with ZXing. |
| 🔐 **Auth** | Auth0 OAuth2/OIDC with multi-role RBAC: organiser, attendee and door staff. Staff join an event through an invite code. |
| 🌐 **Web** | React + TypeScript organiser console, deployed on Cloudflare Pages. |
| ✅ **Quality** | Unit tests on the backend and Android, with Android tests running in GitHub Actions on every pull request. Docker Compose for local setup. |

`Kotlin` `Jetpack Compose` `Hilt` `Ktor` `Spring Boot` `JPA` `PostgreSQL` `Auth0` `React` `TypeScript` `Docker` `GitHub Actions`

---

## 📱 Android projects

### [GCET Connect](https://github.com/Yashvvvv/GCET_CONNECT): AI college assistant · [try it in the browser](https://appetize.io/app/b_p3kmdkjsrqrk43rjeb44fyibzi)
A chatbot for students of my college, built on the Google Gemini API. A custom **Levenshtein-distance matcher** answers from a curated college Q&A set first, and Gemini is used only when nothing matches, so local facts stay correct. Replies stream token by token, chat history is kept in Room, and a study mode generates MCQ quizzes on any CS topic.

`Kotlin` `Jetpack Compose` `MVVM` `Hilt` `Room` `Coroutines` `Gemini API`

### [ReadSphere](https://github.com/Yashvvvv/ReadSphere): book reading companion
Search the Google Books API, track what you're reading, rate books, take notes, and sync your library in real time with Cloud Firestore. MVVM with Coroutines and Firebase Authentication. It has its own visual identity and motion system rather than default Material styling.

`Kotlin` `Jetpack Compose` `MVVM` `Hilt` `Firebase Auth` `Firestore` `Retrofit`

### [MedAssist](https://github.com/Yashvvvv/Medassistandroid): AI medicine assistant (the Android client for PharmaLens, below)
Scan a medicine with the camera to identify it, check drug interactions, find nearby pharmacies on a map, and get medication reminders. Built with Clean Architecture (use cases), CameraX, Room, WorkManager reminders, Google Maps and encrypted token storage.

`Kotlin` `Jetpack Compose` `Clean Architecture` `CameraX` `Room` `WorkManager` `Google Maps`

<details>
<summary><b>More Android work</b></summary>

| Project | What it is |
|---|---|
| [Jet Weather Forecast](https://github.com/Yashvvvv/jetweatherforecast) | Forecasts, city search and offline favourites: API, repository, Room and Compose, with real error and retry states |
| [Voice Assistant](https://github.com/Yashvvvv/Voice-Assistant-App) | Speech recognition sends what you say to Gemini, with the conversation shown in a chat UI |
| [Vrid](https://github.com/Yashvvvv/Vrid) | Blog reader with pagination, offline caching and HTML rendering in Compose |

</details>

---

## ⚙️ Backend projects

### [PharmaLens](https://github.com/Yashvvvv/PharmaLens-AI-Pharmaceutical-Intelligence-Platform): AI pharmaceutical platform · [full stack](https://github.com/Yashvvvv/MedAssist-FullStack)
The Spring Boot backend behind MedAssist. **AI medicine recognition** with Google Gemini and WebFlux. Secure REST APIs with JWT, **4-tier RBAC** (including verified healthcare providers), BCrypt and IP-based rate limiting with Bucket4j. Caffeine caching cuts repeat AI calls, and a pharmacy locator does geo-search with the Google Maps API. Ships with Docker and Prometheus metrics.

`Spring Boot` `WebFlux` `Spring Security` `JWT` `PostgreSQL` `Gemini API` `Google Maps API` `Docker`

### [Hospital Management System](https://github.com/Yashvvvv/Hospital_Management)
REST API for patients, doctors, appointments, insurance and departments, modelled with Spring Data JPA/Hibernate. Secured with JWT and role-based access, with global exception handling and controller tests using JUnit, Mockito and H2.

`Java` `Spring Boot` `JPA/Hibernate` `PostgreSQL` `Spring Security` `JUnit` `Mockito`

### [NexusNotes](https://github.com/Yashvvvv/NexusNotesWebApp): one API, two stacks
A notes app with a stateless JWT API (access and refresh tokens, BCrypt-hashed passwords) in Kotlin + Spring Boot on MongoDB, with a React frontend. I then **rebuilt the same API [in FastAPI](https://github.com/Yashvvvv/FastAPI_Mongo_Backend)** with Beanie and Celery to see what each framework gives you for free.

`Kotlin` `Spring Boot` `MongoDB` `React` `Python` `FastAPI`

<details>
<summary><b>More web and AI tools</b></summary>

| Project | What it is |
|---|---|
| [SubtitlesGen](https://github.com/Yashvvvv/SubtitlesGen) | Generates subtitles from a video, an audio file or a YouTube link, using OpenAI Whisper (Python + React) |
| [ResumeAnalyzer](https://github.com/Yashvvvv/ResumeAnalyzer) | Scores a resume against a job description and lists the missing skills, using Gemini |
| [Portfolio](https://github.com/Yashvvvv/Portfolio_Website) | My personal site, [yashsharma054.dev](https://yashsharma054.dev) (React, TypeScript, Tailwind, Cloudflare) |

</details>

---

## 🛠️ Tech stack

| | |
|---|---|
| **Languages** | Kotlin, Java, C/C++, SQL, TypeScript, JavaScript |
| **Android** | Jetpack Compose, Material Design 3, Navigation, Kotlin Multiplatform, Coroutines & Flow |
| **Architecture** | MVVM, Clean Architecture, Hilt/Dagger, Retrofit, Ktor, Room, DataStore |
| **Backend & data** | Spring Boot, Spring Security, REST APIs, OAuth2/OIDC & JWT, JPA/Hibernate, PostgreSQL, MySQL, MongoDB, Firebase |
| **Tools** | Git, Gradle, Docker, GitHub Actions, Android Studio, IntelliJ IDEA, Postman, Swagger |

## 🏆 Achievements & leadership

- **Application Development Lead**, GDG on Campus GCET (Sep 2024 – Jul 2025)
- **Cybersecurity Executive**, GDSC GCET (Sep 2023 – Aug 2024)
- **Best Beginner Team**, Hack This Fall 4.0
- **Smart India Hackathon finalist**, out of 50+ teams, with KrishiApp
- **500+ DSA problems** solved across LeetCode, GeeksforGeeks and CodeStudio
