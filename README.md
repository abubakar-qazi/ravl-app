# Ravl — Real-Time Social Discovery

> **Meet someone new in 3 minutes. Or don't. Either way, it'll be interesting.**

Ravl is a high-velocity social discovery app built around quick, timed interactions. Instead of browsing profiles and sending cold messages, Ravl matches you with someone compatible and puts you both in a live conversation — with games, ice breakers, and a timer.

> ⚠️ Currently in closed beta.

---

## ✨ Features

### 🚀 Vibe Check Onboarding
- Personality-driven onboarding using **Would You Rather** questions
- Answers generate a compatibility profile used to improve match quality
- The more honest your answers, the better your matches

### 🌐 Orbit Lobby
- Animated live lobby showing active users in the matching pool
- One tap to enter the queue — matchmaking handles the rest
- Real-time queue status and estimated wait indicators

### ⚡ Smart Matchmaking
- Server-side matchmaking via **Firebase Cloud Functions**
- Pairs users based on compatibility scores computed from onboarding responses and availability
- Handles queue management, timeout logic, and rematch flows

### 💬 Ephemeral Live Chat
The core experience — a 3-minute timed conversation between two matched users:

- **Blur Reveal** — avatars start blurred and gradually sharpen as conversation depth increases
- **Ice Breakers** — context-aware conversation starters based on mutual interests and vibe compatibility
- **Extend Session** — both users can mutually agree to extend the timer if the conversation is going well
- **Real-Time Typing** — live typing indicators and online presence via Firebase Realtime Database

### 🎮 Interactive Social Games
Built-in games designed to break the ice fast:

| Game | Description |
|---|---|
| Truth or Dare | Three difficulty levels — Mild, Spicy, and Extreme. Server-side scoring. |
| Rock Paper Scissors | Quick decision-maker with live result animations |
| Would You Rather | Compare choices to find common ground between matched users |

### 🤝 Connections & Permanent Chat
- Send a friend request to users you vibe with during a live session
- Connected friends unlock a permanent chat interface with message history and unread counts
- Rich profiles with avatars, bios, and vibe stats from past sessions

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| State Management | Riverpod |
| Navigation | GoRouter |
| UI | Custom animations, Glassmorphism, Google Fonts |
| Authentication | Firebase Auth (Email/Password + Google Sign-In) |
| Database | Firebase Firestore |
| Real-Time Presence | Firebase Realtime Database |
| Media Storage | Firebase Storage |
| Backend Logic | Firebase Cloud Functions (TypeScript) |

### Cloud Functions
| Function | Purpose |
|---|---|
| `matchmaking.ts` | Queue management, compatibility scoring, user pairing |
| `gameActions.ts` | Game state management, move validation, server-side scoring |

---

## 📂 Project Structure

```
lib/
├── screens/            # Auth, Lobby, Chat, Game, Profile screens
├── services/           # Firebase services (Auth, Chat, Matchmaking, Games)
├── models/             # Data models (User, ChatRoom, GameSession, Match)
├── utils/              # Constants, helpers, and theme utilities
└── widgets/            # Reusable UI components and animations

functions/
├── src/
│   ├── index.ts        # Cloud Functions entry point
│   ├── matching.ts     # Matchmaking queue and pairing logic
│   └── gameActions.ts  # Game mechanics and scoring
```

---

## 🎨 Design Language

Ravl uses a **Glassmorphism** design language — frosted glass surfaces, soft gradients, and layered depth. The aesthetic reinforces the app's theme: interactions that feel alive, temporary, and real.

Custom animations throughout:
- Orbit lobby particle effects
- Blur reveal avatar transitions
- Timer countdown animations
- Game result celebrations

---

## 📱 Platform
- **Android** — Closed beta
- Firebase Auth supports Email/Password and Google Sign-In

---

## ⚠️ Beta Status

Ravl is currently in closed beta. The core matching, chat, and game systems are functional. Active development is ongoing.

---

## 👨‍💻 Developer

Built by **Abubakar Qazi** — Flutter developer based in Islamabad, Pakistan.

[GitHub](https://github.com/abubakar-qazi) · [LinkedIn](https://linkedin.com/in/abubakar-qazi-6b9934311)
