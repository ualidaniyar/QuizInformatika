# 💻 Информатика: Викторина — Android App

Приложение-викторина на 10 вопросов по информатике и компьютерным технологиям.

## 📱 Возможности
- 10 вопросов по информатике
- Таймер 20 секунд на каждый вопрос
- Подсветка правильного / неправильного ответа
- Объяснение после каждого ответа
- Экран результата с оценкой и процентом
- Тёмный дизайн

---

## 🚀 Сборка APK через GitHub Actions (автоматически)

### Шаг 1 — Загрузи проект на GitHub
1. Зайди на [github.com](https://github.com) → **New repository**
2. Назови репозиторий, например: `QuizInformatika`
3. Нажми **Create repository**

### Шаг 2 — Загрузи файлы

**Вариант А — через сайт GitHub:**
- Нажми **"uploading an existing file"**
- Перетащи все файлы проекта (сохрани структуру папок!)

**Вариант Б — через Git (рекомендуется):**
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/ВАШ_НИК/QuizInformatika.git
git push -u origin main
```

### Шаг 3 — Добавь gradle-wrapper.jar
> ⚠️ Этот файл обязателен для сборки!

Скачай его отдельно:
```
https://raw.githubusercontent.com/gradle/gradle/v8.4.0/gradle/wrapper/gradle-wrapper.jar
```
Положи в папку: `gradle/wrapper/gradle-wrapper.jar`
Загрузи на GitHub вместе с остальными файлами.

### Шаг 4 — Запусти сборку
После загрузки файлов GitHub автоматически начнёт сборку.

Или вручную:
- Зайди в **Actions** → **Build Android APK** → **Run workflow**

### Шаг 5 — Скачай APK
- Открой вкладку **Actions**
- Нажми на последний запуск ✅
- В разделе **Artifacts** нажми **QuizInformatika-APK**
- Скачай ZIP → внутри будет `app-debug.apk`

---

## 🛠 Сборка локально (Android Studio)

1. Установи [Android Studio](https://developer.android.com/studio)
2. Открой папку проекта: **File → Open → QuizApp**
3. Подожди синхронизацию Gradle
4. **Build → Build Bundle(s) / APK(s) → Build APK(s)**
5. APK будет в: `app/build/outputs/apk/debug/app-debug.apk`

---

## 📁 Структура проекта
```
QuizApp/
├── .github/
│   └── workflows/
│       └── build.yml          ← GitHub Actions
├── app/
│   └── src/main/
│       ├── java/com/quiz/informatika/
│       │   ├── QuizData.kt    ← Вопросы и ответы
│       │   ├── SplashActivity.kt
│       │   ├── MainActivity.kt
│       │   ├── QuizActivity.kt
│       │   └── ResultActivity.kt
│       ├── res/
│       │   ├── layout/        ← XML макеты экранов
│       │   ├── values/        ← Цвета, строки, темы
│       │   └── drawable/      ← Фоны
│       └── AndroidManifest.xml
├── gradle/wrapper/
│   ├── gradle-wrapper.jar     ← Скачать отдельно!
│   └── gradle-wrapper.properties
├── build.gradle
├── settings.gradle
├── gradlew
└── gradlew.bat
```

---

## 🎯 Минимальные требования
- Android 7.0 (API 24) и выше
- Kotlin 1.9+
