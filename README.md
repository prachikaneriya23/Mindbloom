# 🌱 MindBloom – Student Wellness

> A calming desktop wellness companion designed to help students reflect, track their mood, build healthy habits, manage stress, and develop a positive mindset.

**MindBloom** is a Python-based desktop application built with **Tkinter** and **Pillow**. It brings together mood tracking, journaling, wellness activities, breathing exercises, motivational content, affirmations, and personal wellness streaks in one simple interface.

The application is designed around a simple idea:

> **Small steps every day can create meaningful changes in your mental and emotional well-being.**

---

## ✨ Features

### 🏠 Home Dashboard

The MindBloom home experience provides a welcoming space for students to begin their wellness journey.

It includes:

- 🌱 MindBloom branding
- 🔥 Personal wellness streak
- 💬 Motivational content
- 🌟 Positive reminders
- 🧭 Easy navigation between wellness activities

---

### 😊 Mood Tracker

The **Mood Tracker** allows users to record how they are feeling and maintain a history of their moods.

Available mood options include:

- 😄 Amazing
- 😊 Happy
- 😐 Okay
- 😔 Low
- 😢 Sad
- 😰 Anxious
- 😤 Frustrated
- 😴 Exhausted

Users can:

- Select their current mood
- Add an optional personal note
- Save their mood entry
- Review recent mood history
- Track emotional patterns over time

Mood entries are stored locally for future use.

---

### 📓 Personal Journal

The **My Journal** section provides a private space for reflection and self-expression.

Users can choose between:

#### ✅ What Went GOOD

Reflect on:

- Small achievements
- Positive moments
- Things that made you happy
- Gratitude
- Personal wins

#### 🌧️ What Was Hard

Write about:

- Difficult experiences
- Stressful situations
- Challenges
- Negative emotions
- Things that are difficult to process

Journal entries are timestamped and saved locally.

---

### 💪 Learn & Grow

The **Learn & Grow** section encourages students to develop a growth mindset.

It includes a **Fear vs Growth** reframing section:

```text
❌ Fear:
"I failed, so I am not good enough."

✅ Growth:
"I failed, so now I know what to fix."
```

It also contains inspirational stories about well-known individuals who experienced failure or rejection before achieving success.

The goal is to help students understand that:

- Failure is part of learning
- Setbacks do not define your potential
- Asking for help is a strength
- Progress is more important than perfection

---

### 🌿 Healthy Lifestyle

The **Healthy Lifestyle** section provides a simple daily wellness checklist.

Users can track habits such as:

- 💧 Drinking enough water
- 🥗 Eating a nourishing meal
- 🚶 Moving their body
- 🌙 Getting adequate sleep
- 📵 Taking screen breaks
- 🤝 Connecting with others
- 🧘 Taking quiet time
- 😄 Doing something enjoyable

The application calculates a simple **wellness score** based on completed checklist items.

Example:

```text
8 / 8 completed
      ↓
   100%
      ↓
🌟 You're absolutely thriving today!
```

The section also provides daily wellness tips covering areas such as hydration, breathing, movement, sleep, nutrition, social connection, journaling, sunlight, and music.

---

### 🫁 Breathe & Relax

MindBloom includes an interactive breathing exercise designed to provide a simple guided relaxation experience.

The breathing cycle follows:

```text
Inhale → Hold → Exhale → Hold
```

The interface provides:

- 🫁 Animated breathing circle
- ⏱️ Countdown timer
- 🌬️ Guided breathing phases
- ▶️ Start/Stop controls
- 💙 Calming messages

The breathing animation runs using a background thread while Tkinter updates the interface.

---

### ✨ Affirmations

The application provides positive affirmations designed to encourage self-compassion and resilience.

Examples include ideas such as:

- Believing in your progress
- Accepting that you don't need everything figured out
- Understanding the importance of rest
- Asking for help
- Taking life one step at a time
- Recognizing your own worth

Affirmations are also used throughout the interface to create a supportive atmosphere.

---

## 🔥 Wellness Streak

MindBloom includes a simple daily streak system.

The application records the user's last activity date and updates the streak based on consecutive days.

The sidebar displays the current streak:

```text
🔥 5-day streak
```

This encourages users to return regularly and build consistent wellness habits.

---

## 💾 Local Data Storage

MindBloom stores user wellness data locally in a JSON file.

The application automatically creates/uses:

```text
~/wellness_data.json
```

The stored data includes:

```text
entries
mood_log
streaks
last_date
```

This allows journal entries, mood history, and streak information to persist between application sessions.

No external database is required.

---

## 🏗️ Application Architecture

```text
                     ┌──────────────────────┐
                     │      MindBloom       │
                     │  Student Wellness    │
                     └──────────┬───────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ▼                     ▼                     ▼
     Mood Tracker           My Journal          Learn & Grow
          │                     │                     │
          ▼                     ▼                     ▼
     Mood History          Journal Entries      Growth Mindset
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ▼                     ▼                     ▼
   Healthy Lifestyle       Breathe & Relax       Affirmations
          │                     │                     │
          ▼                     ▼                     ▼
   Wellness Score          Guided Breathing       Positive Mindset
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                ▼
                       Local JSON Storage
```

---

## 🛠️ Tech Stack

| Technology       | Purpose                                 |
| ---------------- | --------------------------------------- |
| **Python**       | Core application development            |
| **Tkinter**      | Desktop graphical user interface        |
| **ttk**          | Styled widgets and scrollbars           |
| **Pillow (PIL)** | Image generation and graphical elements |
| **JSON**         | Local data storage                      |
| **datetime**     | Dates, timestamps, and streak tracking  |
| **threading**    | Background breathing animation          |
| **time**         | Breathing exercise timing               |
| **random**       | Random motivational content             |
| **math**         | Animation and graphical calculations    |
| **OS**           | File-system and platform operations     |

The repository is currently a Python project with the application implemented primarily in `student.py`.

---

## 📁 Project Structure

```text
Mindbloom/
│
├── README.md
│
└── student.py
```

### `student.py`

The main application contains:

- Tkinter user interface
- Navigation sidebar
- Home dashboard
- Mood tracker
- Journal system
- Growth mindset content
- Healthy lifestyle checklist
- Wellness score calculation
- Breathing exercise
- Affirmations
- Motivational content
- Local JSON data management
- Wellness streak tracking
- Pillow-based graphics and animations

The repository currently contains the README and the main Python application file.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have:

- **Python 3.x**
- `pip`
- A desktop environment capable of running Tkinter

Verify your Python installation:

```bash
python --version
```

---

## 📥 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/prachikaneriya23/Mindbloom.git
```

### 2. Navigate to the Project

```bash
cd Mindbloom
```

### 3. Install Pillow

The application uses Pillow for image generation and graphical elements.

```bash
pip install pillow
```

> **Note:** Tkinter is included with many standard Python installations. On some Linux distributions, it may need to be installed separately.

---

## ▶️ Run the Application

Start MindBloom with:

```bash
python student.py
```

The application opens a desktop window titled:

```text
🌱 MindBloom – Student Wellness
```

The interface provides a sidebar for navigating between the different wellness modules.

---

## 🖥️ User Interface

The application uses a dark-themed desktop interface with:

```text
┌─────────────────────────────────────────────┐
│ 🌱 MindBloom                                │
├──────────────┬──────────────────────────────┤
│ 🏠 Home      │                              │
│ 😊 Mood      │       Main Content Area      │
│ 📓 Journal   │                              │
│ 💪 Learn     │       Wellness Features      │
│ 🌿 Healthy   │                              │
│ 🫁 Breathe   │                              │
│ ✨ Affirm    │                              │
└──────────────┴──────────────────────────────┘
```

The sidebar provides access to:

- 🏠 Home
- 😊 Mood Tracker
- 📓 My Journal
- 💪 Learn & Grow
- 🌿 Healthy Life
- 🫁 Breathe
- ✨ Affirmations

---

## 🔄 Typical User Workflow

A typical MindBloom session can look like:

```text
Open MindBloom
      │
      ▼
Check Today's Wellness
      │
      ▼
Record Current Mood
      │
      ▼
Write in Journal
      │
      ▼
Complete Wellness Checklist
      │
      ▼
Practice Guided Breathing
      │
      ▼
Read an Affirmation
      │
      ▼
Build Your Streak
```

The goal is not to complete everything perfectly.

The goal is to encourage **small, consistent acts of self-care**.

---

## 🎯 Project Objectives

MindBloom was designed with several objectives:

- 🌱 Encourage healthy daily habits
- 😊 Help students recognize and record emotions
- 📓 Encourage journaling and reflection
- 🧠 Promote a growth mindset
- 🫁 Provide a simple breathing/relaxation activity
- 💚 Encourage self-compassion
- 🔥 Build consistency through streak tracking
- 🖥️ Provide an accessible desktop wellness experience
- 💾 Keep personal data available locally

---

## 🌟 Key Highlights

### Student-Focused

The application is designed specifically around common student experiences such as:

- Academic pressure
- Failure and setbacks
- Stress
- Emotional ups and downs
- Difficulty maintaining healthy routines
- Need for positive reinforcement

### Offline-Friendly

Core functionality works locally without requiring a web server or external database.

### Personal

Journal and mood information is stored locally on the user's computer.

### Interactive

The application is not simply informational—it allows users to actively:

```text
Track → Reflect → Learn → Breathe → Improve
```

---

## 🔐 Privacy Considerations

MindBloom stores wellness information locally in:

```text
wellness_data.json
```

The application does not require a remote database for its core data-storage functionality.

Because the data is stored on the user's computer, users should still protect access to their device and local files.

---

## ⚠️ Wellness Disclaimer

**MindBloom is an educational and wellness-support application. It is not a medical or mental-health treatment tool.**

The application's wellness tips, affirmations, breathing exercises, and motivational content are intended for general educational and self-care purposes.

They should not replace professional medical, psychological, or mental-health advice.

If you are experiencing severe emotional distress, feel unsafe, or believe you may harm yourself or someone else, seek immediate help from a qualified professional or appropriate emergency/crisis service in your area.

---

## 🔮 Future Enhancements

Potential improvements for future versions include:

- 📊 Mood analytics and visual charts
- 📈 Long-term wellness dashboards
- 📅 Calendar-based mood tracking
- 🔔 Daily wellness reminders
- 🎯 Personalized wellness goals
- 🔐 Optional encrypted journal storage
- ☁️ Optional cloud backup
- 👤 Multiple user profiles
- 🌓 Theme customization
- 🎵 Relaxation sounds and ambient music
- 🧘 Additional meditation exercises
- 🧠 More mental wellness educational resources
- 📱 Mobile application version
- 🌐 Web application version
- 🌍 Multi-language support
- 📤 Exportable wellness reports
- 🔎 Searchable journal history

---

## 🤝 Contributing

Contributions and suggestions are welcome!

### 1. Fork the repository

Create your own fork of the project.

### 2. Create a feature branch

```bash
git checkout -b feature/your-feature
```

### 3. Make your changes

Improve the UI, wellness modules, data management, animations, or functionality.

### 4. Commit your changes

```bash
git add .
git commit -m "Add your feature"
```

### 5. Push your branch

```bash
git push origin feature/your-feature
```

### 6. Open a Pull Request

Describe your changes and submit the pull request for review.

---

## 📄 License

No license is currently specified in the repository.

If you plan to distribute the project or accept external contributions, consider adding an appropriate open-source license.

---

## 🌱 Vision

MindBloom is built around a simple philosophy:

> **You don't have to change everything at once. One small step, one honest reflection, and one breath at a time can make a difference.**

---

###
