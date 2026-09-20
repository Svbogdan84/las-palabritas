# las-palabritas
Word cards

- v0.62 - Added 10 topics (Shopping, Sport, Cinema, Medicine, Auto, Professions, Internet & Computers, Education, Office, Hobbies): 200 new words
- v0.61 - Confirmed target language (EN/UK/RU) is persisted like mute and reverse mode; no behavior change
- v0.60 - Added Reverse mode toggle (🔁, persisted): translation → Spanish, with the example after the revealed Spanish word; renamed "Mix mode" to "All words"
- v0.59 - "Skip for now" available immediately, before or after flipping; skipping never counts toward progress
- v0.58 - Added synthesized sound effects (new card, skip, "I know this"), no external assets
- v0.57 - Rewrote 162 templated thematic-topic examples with contextual sentences; fixed 5 stray adjective placeholders
- v0.56 - Rewrote 181 templated noun examples with contextual sentences
- v0.55 - Rewrote 183 templated adjective examples with contextual sentences and correct gender agreement
- v0.54 - Rewrote 180 templated verb examples with contextual sentences; fixed broken reflexive-verb examples
- v0.53 - Fixed "Couldn't save progress" error: storage falls back to localStorage outside Claude Artifacts
- v0.52 - Removed duplicate thematic-topic words, disambiguated near-synonym pairs, added version footer
- v0.51 - More words
- v0.5 - Add Rus
- v0.4 - Add Ukr
- v0.3 - Mix mode
- v0.2 - Examples were added
- v0.1

> A lightweight, zero-dependency single-page web application for mastering Spanish vocabulary with multi-language support (English, Ukrainian, Russian), interactive 3D flashcards, and category-based progress tracking.

![Palabritas Banner](https://img.shields.io/badge/Language-Spanish%20%28Espa%C3%B1ol%29-C99A44?style=for-the-badge)
![UI Languages](https://img.shields.io/badge/UI_Languages-EN%20%7C%20UK%20%7C%20RU-22303F?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-Single--File%20Vanilla%20JS-5E9A50?style=for-the-badge)
![Dependencies](https://img.shields.io/badge/Dependencies-Zero-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [User Interface & Design System](#-user-interface--design-system)
- [Grammatical & Thematic Categorization](#-grammatical--thematic-categorization)
- [Technical Architecture](#-technical-architecture)


---

## 🌟 Overview

**Palabritas** (*"Little Words"*) is an elegant, highly performant web-based flashcard application designed to accelerate Spanish vocabulary acquisition. Built entirely as a self-contained single-page application (SPA), Palabritas requires no server infrastructure, build tools, package managers, or third-party JavaScript libraries.

Whether you are an English, Ukrainian, or Russian speaker learning Spanish, Palabritas delivers an intuitive learning environment with real-time feedback, contextual usage examples, tactile 3D card interactions, and automatic progress persistence.

---

## ✨ Key Features

- 🃏 **Hardware-Accelerated 3D Flashcards**: Tactile flip card animations powered by native CSS3 3D perspective transforms (`rotateY`).
- 🌐 **Trilingual Translation System**: Instant switching between **English**, **Ukrainian**, and **Russian** translations for both vocabulary words and UI controls.
- 📂 **Dual Category Learning Modes**:
  - **Main Grammatical Categories**: Focus on core parts of speech (*Nouns, Adjectives, Verbs, Others*).
  - **Thematic Topics**: Target contextual vocabulary modules (*Food, Travel, Animals, Family, Weather, Colors, Body, Clothing, Home, Emotions, Shopping, Sport, Cinema, Medicine, Auto, Professions, Internet & Computers, Education, Office, Hobbies*).
- 🔀 **All Words Deck**: Combine all categories and topics into a randomized full-deck practice session.
- 🔁 **Reverse Mode**: Toggle card direction between Spanish → translation (default) and translation → Spanish.
- 📊 **Persistent Progress Tracking**: Automatically tracks learned words per category. Uses the Claude Artifacts `window.storage` API when run inside an Artifact, and falls back to `localStorage` when run as a standalone file — displaying progress bars, percentages, and completed badges either way.
- 🔄 **Smart Session Management**: Skip cards for review later, mark mastered words, and review completed decks at any time.
- 📱 **Mobile-First Responsive Layout**: Optimized for smartphones, tablets, and desktop displays with touch-friendly targets.
- ⚡ **No Build Step, No Tracking**: No server infrastructure, build tools, or third-party JavaScript libraries — no analytics or ad tracking of any kind. Progress persists via the Claude Artifacts `window.storage` API.

---

## 🎨 User Interface & Design System

Palabritas uses a dark paper-and-slate aesthetic designed to minimize eye strain during long study sessions while maintaining high legibility and clear color coding for grammatical word classes.

### Color Tokens

| Token Name | Hex Code | Role / Element |
| :--- | :--- | :--- |
| `--bg` | `#1B2430` | Main application background (Deep Slate) |
| `--panel` | `#22303F` | Tile card background & secondary container |
| `--paper` | `#F5F1E6` | Flashcard face background (Warm Paper) |
| `--gold` | `#C99A44` | Primary brand accent, active state, progress fill |
| `--noun` | `#BFE0B6` | Noun category badge & tile fill (Soft Green) |
| `--adj` | `#EFC0BA` | Adjective category badge & tile fill (Warm Coral) |
| `--verb` | `#B7D3EC` | Verb category badge & tile fill (Soft Blue) |
| `--other` | `#D9C7E8` | Other category badge & tile fill (Soft Lavender) |

---

## 📚 Grammatical & Thematic Categorization

### 1. Main Grammatical Categories

Palabritas color-codes grammatical parts of speech to help learners build structural intuition:

- 🟢 **Sustantivos (Nouns)**: Common objects, places, concepts, professions, and natural phenomena (e.g., *la casa, el libro, el médico, la playa*).
- 🔴 **Adjetivos (Adjectives)**: Descriptive attributes, physical traits, personality features, and emotional states (e.g., *grande, feliz, rápido, amable*).
- 🔵 **Verbos (Verbs)**: Core action verbs, essential helper verbs, and daily routine verbs (e.g., *hablar, comer, vivir, descansar*).
- 🟣 **Otros (Others)**: Essential adverbs, prepositions, conjunctions, pronouns, and transitional phrases.

### 2. Thematic Sub-Topics

For focused real-world situational learning, words are organized into curated sub-topics:

| Topic Icon | Spanish Name | English Name | Ukrainian Name | Russian Name |
| :---: | :--- | :--- | :--- | :--- |
| 🍲 | Comida | Food | Їжа | Еда |
| ✈️ | Viajes | Travel | Подорожі | Путешествия |
| 🐾 | Animales | Animals | Тварини | Животные |
| 👪 | Familia | Family | Сім'я | Семья |
| ⛅ | El clima | Weather | Погода | Погода |
| 🎨 | Los colores | Colors | Кольори | Цвета |
| 🫀 | El cuerpo | Body | Тіло | Тело |
| 👕 | La ropa | Clothing | Одяг | Одежда |
| 🏠 | La casa | Home | Дім | Дом |
| 💭 | Las emociones | Emotions | Емоції | Эмоции |
| 🛍️ | Las compras | Shopping | Покупки | Покупки |
| ⚽ | El deporte | Sport | Спорт | Спорт |
| 🎬 | El cine | Cinema | Кіно | Кино |
| 🩺 | La medicina | Medicine | Медицина | Медицина |
| 🚗 | El automóvil | Auto | Авто | Авто |
| 👷 | Las profesiones | Professions | Професії | Профессии |
| 💻 | Internet e informática | Internet & Computers | Інтернет і комп'ютери | Интернет и компьютеры |
| 🎓 | La educación | Education | Освіта | Образование |
| 🏢 | La oficina | Office | Офіс | Офис |
| 🧩 | Los pasatiempos | Hobbies | Хобі | Хобби |

---

## 🛠️ Technical Architecture

Palabritas is engineered as a zero-dependency, single-file HTML5 web application containing embedded CSS3 and Vanilla ES6+ JavaScript.
