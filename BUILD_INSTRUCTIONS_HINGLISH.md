# JARVIS 2.0.0 Autopilot — APK Build & Setup Guide

## APK Kaise Banayein? (2 Aasan Tarike)

### Tarika 1: Bina PC ke Cloud me APK Banayein (GitHub Actions — Free)
1. GitHub.com par ek naya private/public repository banayein (phone browser se bhi ho jayega).
2. Is zip (`Jarvis-2.0.0-Autopilot.zip`) ki saari files us repository me upload/push karein (`.github/workflows/build_apk.yml` pehle se included hai).
3. GitHub repo ke **Actions** tab me jayein -> **Build JARVIS Autopilot APK** -> **Run workflow** par tap karein.
4. ~4 minute me `JARVIS-2.0.0-Autopilot-APK` (`app-release.apk`) download karne ke liye ready mil jayega!

### Tarika 2: PC / Laptop par Build Karein
```bash
flutter pub get
flutter build apk --release
```
APK yahan banega: `build/app/outputs/flutter-apk/app-release.apk`

---

## Naye Features (v2.0.0 Autopilot)
1. **Native Gemini 3.8 Flash Support**: Default model `gemini-3.8-flash` set hai with `thinkingLevel` (`LOW` ultra-fast autopilot, `MEDIUM`, `HIGH`).
2. **Multi-Model API Key Vault**: Settings me ab aap **Google Gemini, OpenAI, Anthropic Claude, DeepSeek, Groq, xAI Grok, OpenRouter, Mistral, Perplexity, NVIDIA NIM, Ollama** sabhi ke API keys ek saath save kar sakte hain — switch karne par purani key delete nahi hoti, aur **Auto-Failover** on hai.
3. **Termux & Code Writing Automation**: `AgentAccessibilityService` me terminal/Termux ke liye automatic clipboard-paste + Enter fallback add kiya gaya hai. Bas bolein: *"Hey Jarvis, open Termux and write a Python script"*.
4. **Ultra-Fast Autopilot (250ms)**: Step delay 1200ms se 250ms kar diya gaya hai aur max steps 30 tak badhaye gaye hain.
5. **Hacker Hologram HUD**: Live active model, `AUTOPILOT // ULTRA-250MS`, aur `DAEMON // 24X7-ACTIVE` telemetry HUD par dikhta hai.
