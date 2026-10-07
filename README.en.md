<p align="right">
  <a href="README.en.md"><img alt="ENG" src="https://img.shields.io/badge/ENG-English-1f6feb?style=for-the-badge"></a>
  <a href="README.md"><img alt="RUS" src="https://img.shields.io/badge/RUS-%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9-2ea043?style=for-the-badge"></a>
</p>

# speech for Android · beta-0.6

**Sign language translation and speech-to-text on an Android phone**

The **speech** app helps people who are deaf or hard of hearing talk with people who don't know sign language:

- **🤟 Signs → text and voice.** A person shows signs to the camera — the words immediately appear on screen in large text, and the phone says them aloud.
- **🎙 Speech → text.** Everything said around you immediately appears on screen in large text. Each person's remark starts on a new line.

> 🚧 **Beta.** The app is still being tested on its first phones. If something doesn't work, open an [Issue](../../issues) (English is welcome) with a screenshot, your phone model and Android version.

> 🌍 **Language of the app.** The interface is in **Russian**, the voice that reads translations aloud is Russian, and speech-to-text currently recognises **Russian**. Sign translation works with any sign language: you teach the app your own signs and type the words for them in any language (words in other languages are read aloud by the Russian voice). This guide gives the English meaning of every button.

> 🔒 **Camera images never leave the phone** — signs are recognised on the phone itself. Speech is recognised by the Google speech service; with **Только на телефоне** (On device only) turned on, audio doesn't go to the internet either.

---

## What's new in beta-0.6

- **🎯 Fewer sign mistakes.** Similar words (for example, the same hand shape at the chin and at the chest) are checked more strictly and are no longer confused. A pose counts only once the fingers have stopped moving, so transitions between signs don't turn into extra words.
- **🗣 Speech of a person 10 metres away** (Android 13 and later). The 👂 button boosts a quiet, distant voice to normal volume and removes low hum. If your phone doesn't support this, the app goes back to the normal microphone by itself.
- **🎧 Bluetooth microphone.** Give the speaker headphones with a microphone — they can be heard from any distance, even in noise.
- **✋ The other hand doesn't interfere.** If one hand rests on a table or your lap, a sign with the other hand is recognised as usual.
- **🎨 Soft interface.** Calm colours, big buttons, a light vibration when a word is translated.

This is the first version in the [SignSpeech](https://github.com/SignSpeech) organisation. It continues beta-0.46 from the [previous repository](https://github.com/Fen1x678/sign_language_interpretation_on_camera).

---

## Will it work on my phone?

| What you need | Why |
|---|---|
| **Android 8.0 or later** | the app won't install otherwise |
| A camera | for signs (front or back camera) |
| The **Google** app | for speech-to-text — usually already installed |
| Android 13 or later | only for the distant-speech boost (👂 button) |
| Bluetooth headphones with a microphone | optional — if the speaker is far away or it is noisy |

To check your Android version: **Settings → About phone → Android version** (on some phones **Settings → System → About phone**).

---

## Installation

There is no ready-made install file (APK) yet — the app has to be built once on a computer. It's free and takes about half an hour; most of that time the computer is downloading what it needs. When a ready APK is available, it will be under [Releases](../../releases), and you won't need a computer.

### What you need

- a Windows, macOS or Linux computer with internet;
- [Android Studio](https://developer.android.com/studio) (free);
- a USB cable for the phone.

### 1. Download the app

On this page click the green **Code → Download ZIP** button and unpack the archive.

Or with Git:

```bash
git clone https://github.com/SignSpeech/Android.git
```

### 2. Open it in Android Studio

1. Start Android Studio → **Open** → choose the unpacked folder (it contains `settings.gradle.kts` and `gradlew`) → **OK**.
2. Wait until **Gradle Sync** at the bottom finishes. The first time it takes a few minutes.
3. If Android Studio offers to update something (Gradle, a plugin), you can accept or decline — the app builds either way.

### 3. Prepare the phone

1. **Settings → About phone** → tap **Build number** 7 times. You'll see "You are now a developer".
2. **Settings → System → Developer options** → turn on **USB debugging**.
3. Connect the phone to the computer with the cable. On the phone tap **Allow**.

### 4. Install

1. At the top of Android Studio choose your phone in the device list.
2. Click the green **▶ Run** button.
3. After about a minute **speech** opens on the phone. You no longer need the computer — the app stays on the phone.

**Install on another phone without a cable:** in Android Studio choose **Build → Build App Bundle(s) / APK(s) → Build APK(s)** → click **locate** in the message → send `app-debug.apk` to the phone (by messenger or email), open it and allow installing from that source.

---

## First launch

1. The app asks for **camera** access — tap **Allow**. Without the camera signs can't be recognised.
2. The app asks for **microphone** access when you open speech-to-text.
3. Recorded signs are stored only on your phone.

---

## How to use

The app's buttons are in Russian; their English meanings are given in brackets.

### Teach the app your signs

The app translates the signs you have shown it. Each word is recorded once:

1. At the bottom tap **«＋ Словарь»** (Dictionary).
2. Type a word in any language, for example "hello".
3. Choose the type: **«С движением»** (With movement — the hand moves) or **«Поза»** (Pose — the hand is still).
4. Tap **«Записать жест»** (Record sign). After the countdown show the sign. Recording runs 3 times: straight, slightly left and slightly right — so the sign is recognised at an angle too.

Record each word 2–3 times, ideally by different people, so it is understood for everyone.

### Translating signs

1. Show signs to the camera. The word appears at the bottom in large text and is spoken aloud. The phone vibrates lightly for each translated word.
2. Lower your hands for 2 seconds — the phrase ends and moves to the history.
3. Buttons under the phrase: **⌫** erase the last word, **✓ Готово** (Done) end the phrase, **▶** say it again, **🔊** voice on/off, 🗑 clear.

**Which camera to use** (🔄 button at the top):
- **back** — point the phone at the person signing; the translation appears on screen and is spoken;
- **front** — the signer sees whether their signs are translated correctly.

### Speech → text

1. Tap **«🎤 Речь → текст»** (Speech → text).
2. Put the phone between the speakers. Text appears immediately; the phrase still being spoken is highlighted in amber. (Speech is recognised in Russian.)
3. Buttons at the bottom:

| Button | What it does |
|---|---|
| 🗑 | clear the text |
| 👂 | distant speech: boosts a quiet, distant voice (Android 13+, on by default) |
| 🎤 / ■ | listen / pause |
| **Aa** | bigger or smaller text |
| 🎧 | Bluetooth headphones microphone |

4. The **⋯** button at the top: **Мои слова** (My words — names and rare words, recognised more accurately), **Новая строка после паузы** (New line after a pause), **Только на телефоне** (On device only, no internet, Android 12+), **Без звукового сигнала** (No beep).
5. Scroll up to re-read. **«↓ К новым»** (To new) returns to the live text.

### Person far away (up to 10 metres)

1. Check that the 👂 button is on (teal).
2. Point the **bottom of the phone at the speaker** — the microphone is at the bottom. Nothing should cover it.
3. The volume bar above the buttons turns mint — the phone hears a voice.
4. In a quiet room a voice from 10 metres is recognised. On the street, in transport or with music, give the speaker **Bluetooth headphones with a microphone** and tap 🎧.

### Light

The 🔦 button at the top: **Авто** (Auto — turns on by itself in the dark), **Всегда вкл.** (Always on), **Выключена** (Off). The back camera uses the flashlight, the front camera uses the screen (a bright white frame).

---

## Tips for accurate recognition

- Keep your hands 30–80 cm from the camera so the whole hand is in the frame.
- Keep your shoulders in the frame: then the same hand shape at the chin, at the chest and at the shoulder means different words.
- Show the sign the same way as when you recorded it.
- You need light. A bright window behind you gets in the way.
- If the other hand is not part of the sign, keep it lowered (it turns grey on screen).
- The hint «Похоже на «слово» — N%» (Similar to "word" — N%) shows how close the sign is to the recorded one. If the percentage is high but the word doesn't count, move **Чувствительность** (Sensitivity, in the Dictionary) to the right.

---

## Troubleshooting

| Problem | What to do |
|---|---|
| Black screen instead of the camera | **Settings → Apps → speech → Permissions → Camera** → allow. |
| A sign isn't recognised | Record the word 1–2 more times (ideally by another person), add light or move **Sensitivity** right. |
| Extra words appear | Move **Sensitivity** left. |
| A one-hand sign isn't recognised when the other hand is visible | Rest the other hand on the table or lap. If the sign was recorded with the other hand visible, record it again. |
| After an update a word is recognised less often | Similar words are now checked more strictly. Record the word 1–2 more times or move **Sensitivity** slightly right. |
| «Нет службы распознавания речи» (No speech recognition service) | Install or update the **Google** app from the Play Store. |
| «Русский язык для распознавания недоступен» (Russian is not available for recognition) | **Settings → System → Languages → Speech recognition** — download Russian, or turn off **Только на телефоне** (On device only). |
| The person is far away, no text | Turn on 👂 and point the bottom of the phone at the speaker. In noise — Bluetooth headphones on the speaker and the 🎧 button. |
| «Усиление дальней речи на этом телефоне не работает» (Distant-speech boost doesn't work on this phone) | Your phone's speech service doesn't support it, so the app uses the normal microphone. Update the **Google** app or use Bluetooth headphones. |
| «Наушники Bluetooth не подключены» (Bluetooth headphones not connected) | Connect the headphones in the Bluetooth settings and tap 🎧 again. |
| A beep at every phrase | **⋯ → «Без звукового сигнала»** (No beep). On some phones this beep can't be muted. |
| Android Studio: "Could not find …" | Check the internet and click **File → Sync Project with Gradle Files**. |
| Android Studio: the phone isn't in the list | Turn on USB debugging, reconnect the cable and tap **Allow** on the phone. |

Didn't find your problem? Open an [Issue](../../issues): what you did, what happened, your phone model and Android version.

---

## What it can't do yet

- The app doesn't know any sign language in advance — it translates only the signs you recorded.
- The interface, the voice and speech-to-text are in Russian for now.
- Facial expressions are not used.
- The dictionary is stored on one phone; it can't be moved to another phone yet.
- A phone call can't be translated: Android doesn't give apps the call audio.
- Speech-to-text doesn't tell people apart by voice: remarks are separated by pauses.

---

## For developers

**Tech:** Kotlin, Jetpack Compose, CameraX, MediaPipe (21 hand points and shoulders), Android system speech recognition.

```
app/src/main/java/com/fen1x/speech/
├── MainActivity.kt, GestureViewModel.kt — entry point and screen logic
├── camera/   — camera (CameraX) and MediaPipe
├── core/     — algorithms in plain Kotlin: pose features, k-NN, DTW, dictionary,
│               false-match protection, speech correction, distant-speech boost
├── speech/   — speech-to-text and microphone recording with the boost
└── ui/       — screens (Jetpack Compose) and theme
app/src/test/ — algorithm tests
app/src/main/assets/ — MediaPipe models
```

- **Tests:** `./gradlew test`, or in Android Studio right-click `app/src/test` → **Run Tests**. The algorithms are covered by 53 tests.
- **How recognition works:** camera → MediaPipe (hand points and shoulders) → smoothing → pose and movement features → k-NN / DTW → word. The algorithms are the same as in the iPhone version; see the [iPhone README](https://github.com/Fen1x678/sign_language_interpretation_on_camera/blob/main/README.en.md#how-it-works).
- **Contributing:** open an Issue or a Pull Request. New contributors are welcome — translating the interface into English is a great first task.

## License

[MIT](LICENSE) — you may freely use, change and port the code as long as you keep the copyright line.
