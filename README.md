# Cake

Cake is a private, offline birthday reminder app for Android. I built it because a normal calendar did not give me the mix I wanted: a clean month-wise view, different reminder rules for different people and an alarm that is difficult to miss for close friends.

I vibecoded Cake with Claude. I supplied the product idea, reminder behaviour, phone target and design direction; Claude planned and implemented the native Android project; and I refined the scope before the final build.

## What it does

- Saves names, birthdays and optional birth years
- Shows upcoming birthdays, a month-wise view and a searchable people list
- Calculates the next birthday and upcoming age
- Supports adjustable reminders before or on the birthday
- Provides normal notifications or full-screen birthday alarms
- Lets alarms be snoozed or dismissed
- Reschedules reminders after a phone restart
- Handles February 29 birthdays with a configurable policy
- Exports and imports a local backup
- Stores everything on-device

## Tech stack

- Kotlin and Java 17
- Jetpack Compose with Material 3
- Android SDK 35, minimum SDK 29
- Kotlin Serialization and Coroutines
- Local JSON storage
- Android AlarmManager, notifications and boot receiver
- Gradle 8.10.2 / Android Gradle Plugin 8.7.3

## Download the app

[Download Cake v1.0](Cake-v1.0.apk). Android may ask you to allow installation from your browser or file manager because this is a personal APK rather than a Play Store release.

This repository is a project showcase and download page. The source code and private signing key remain private.

## AI build prompt

The original brief asked for a personal birthday reminder with adjustable timing, different rules for close friends, month-wise browsing and a highly polished interface.

[Read the reconstructed production prompt](PROMPT.md). It is the improved specification I would use to recreate the app, not a verbatim chat transcript.

## Privacy

Cake stores birthday data locally. It does not require an account or internet access.
