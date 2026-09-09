# Reconstructed production prompt

This is a structured, reusable version of the real brief behind Cake.

```text
Act as a senior Android product engineer, notification-systems specialist, UX designer and QA lead. Build a polished native birthday reminder app named Cake for a OnePlus 13. It must be a complete installable app, work offline and make important birthdays difficult to miss.

PRODUCT GOAL
Let one person save birthdays, see what is coming up and choose different reminder timing and intensity for each person. A close friend might need a 10 PM reminder the night before plus a 9 AM alarm on the day; another person may need only a morning notification.

REQUIRED EXPERIENCE
1. Save a person's name, birthday, optional birth year and optional note.
2. Allow multiple reminder rules per person. Each rule needs an offset (for example, same day or one day before), time and delivery type (notification or alarm).
3. Provide sensible global defaults but allow per-person overrides.
4. Show an Upcoming screen ordered by the next occurrence, with countdown and upcoming age when known.
5. Provide a month-wise browser and a searchable people list.
6. Let the user add, edit and delete birthdays with clear confirmation where data would be lost.
7. For high-priority reminders, show a full-screen alarm with snooze and dismiss actions.
8. Reschedule all future reminders after a device restart or app update.
9. Define and expose a policy for February 29 birthdays in non-leap years.
10. Support local backup export and import.

DESIGN DIRECTION
Use a warm, celebratory visual system without making it childish or cluttered. Prioritize names, dates and countdowns. Use polished empty states, subtle confetti only where meaningful, accessible typography and large touch targets. Keep common actions obvious and make reminder rules understandable in plain language.

TECHNICAL CONSTRAINTS
- Kotlin, Jetpack Compose and Material 3.
- Minimum Android 10 (API 29); target the current installed SDK.
- Kotlin Serialization with atomic local JSON storage.
- No account, cloud database, analytics or INTERNET permission.
- Use Android notification channels, AlarmManager, runtime notification permission, exact-alarm capability checks and a boot receiver.
- Use stable unique identifiers for people and reminder rules so edits cannot trigger another person's alarm.
- Keep signing material outside source control.

WORKING METHOD
Before implementation, explain the data model, scheduling model and Android-version limitations. Ask only questions that change behaviour. Build scheduling and date calculations as testable logic before UI polish. Use platform APIs directly unless a dependency clearly reduces risk. Do not claim an alarm is guaranteed if the OS can defer it; handle permission and battery-optimization states transparently.

ACCEPTANCE TESTS
- Add people with and without birth years and calculate the next occurrence correctly.
- Verify month ordering across year boundaries.
- Verify February 29 behaviour in leap and non-leap years.
- Schedule same-day and previous-day rules at different times.
- Confirm notification and alarm paths open the correct person.
- Confirm snooze and dismiss behave independently.
- Reboot an emulator and confirm reminders are rescheduled.
- Confirm export/import round-trips all people, settings and rules.
- Confirm the manifest has no internet permission and no signing secret is present.
- Run a clean Gradle build and smoke-test major flows on an API 35 emulator.
- Deliver exact build and install instructions plus known limitations.
```
