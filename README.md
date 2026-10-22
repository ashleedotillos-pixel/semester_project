# Student Portal

## Summary

A web-based student portal designed to streamline academic updates and account
access for students, addressing communication gaps and manual record tracking
within the school community. Initial features include a login interface and
structured navigation views.

**Activity 9** extends the same Activity 8 project with a Report Form screen
(`lib/screens/report_form_screen.dart`), reusable widgets and four working
asynchronous UI responses - Loading, Success, Empty and Error.

## Current stack

Flutter Web / Dart; planned REST API and PostgreSQL. All asynchronous
responses used in Activity 9 are **simulated** with `Future.delayed`, no
database record is created.

## Folder structure

```
lib/
  main.dart
  app.dart
  screens/
    home_screen.dart
    login_screen.dart
    report_form_screen.dart   <- new in Activity 9
  widgets/
    app_button.dart
    app_text_field.dart
  services/
    report_service.dart       <- simulated data service
  models/
    student_report.dart
  routes/
    app_routes.dart
  constants/
    app_constants.dart
```

## Run locally

```bash
flutter pub get
flutter run -d chrome
```

## How to reproduce the four UI responses

| Response  | What to do                                                                    |
| --------- | ----------------------------------------------------------------------------- |
| LOADING   | Fill the form and press **Submit Report** (the request takes 3 seconds).      |
| SUCCESS   | Let the request finish - the confirmation and the saved report are shown.     |
| EMPTY     | Press **View Reports** before creating a report, or filter to no match.      |
| ERROR     | Turn on **Simulate a server error (demo only)** and submit a valid form.     |

After an error the screen offers **Retry** (repeats the request) and
**Edit Report** (returns to the filled form). Turn the switch off before
pressing **Retry** to see the request succeed.

## Screenshots (Activity 9)

All screenshots are in `screenshots/activity9/`.

| # | File                              | What it shows                                                       |
| - | --------------------------------- | ------------------------------------------------------------------- |
| 1 | `screenshot1_project_structure.png` | VS Code Explorer with the Activity 8 files and the new `lib/screens/report_form_screen.dart`. |
| 2 | `screenshot2_widget_reuse.png`      | `AppTextField` / `AppButton` used in `report_form_screen.dart` (left) and `AppButton` used again in `home_screen.dart` (right). |
| 3 | `screenshot3_loading_state.png`     | **LOADING** - spinner banner and the disabled *Submit Report* button. |
| 4 | `screenshot4_success_state.png`     | **SUCCESS** - confirmation and the saved report.                     |
| 5 | `screenshot5_empty_state.png`       | **EMPTY** - no report exists yet, with the first-report action.      |
| 6 | `screenshot6_error_state.png`       | **ERROR** - error message plus the *Retry* and *Edit Report* actions. |

## First checkpoint

Date: October 15, 2026 | Commit: 4ec4b31

## Second checkpoint (Activity 9)

Date: October 22, 2026 | Commit: see the Activity 9 commit in the repository history

Repository: https://github.com/ashleedotillos-pixel/semester_project
