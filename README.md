# CollegeLife Kit

A responsive student dashboard built with HTML, CSS and vanilla JavaScript.

## Features
- **Overview:** attendance average, CGPA, monthly spending and quick navigation.
- **Attendance tracker:** add subjects, record classes held/attended, edit or remove records, and set a minimum attendance target.
- **CGPA calculator:** weighted CGPA based on course credits and grade points.
- **Expense tracker:** add transactions by category, set a monthly budget, and view your remaining/over-budget amount.
- **Grade predictor:** calculate the average score needed in remaining assessments to reach a target final grade.
- **Campus GPS:** browser geolocation, coordinates, accuracy, Google Maps link, and directions to a typed destination.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in Chrome, Edge or Firefox.
3. For GPS, browsers generally require a secure context (`https://` or `http://localhost`) and permission. If geolocation does not work from a directly opened file, run a local server:
   - With VS Code, install Live Server and choose **Open with Live Server**.
   - Or run `python -m http.server 5500` in this folder, then open `http://localhost:5500`.

## Data and privacy
The app saves data in the browser's `localStorage` on the current device/browser. It does not have a backend, account login, cloud sync, or database. Clearing browser site data will clear these records. GPS is requested only after the student taps **Detect my location**; coordinates are used to create the Google Maps link and are not saved by this app.

## Notes
- CGPA is calculated as `sum(credits × grade points) / sum(credits)`.
- Attendance percentage is `attended / held × 100`.
- Grade prediction assumes the completed and remaining assessment weights add up to 100%.
- This is a front-end starter project. For multi-device sync, user accounts, admin controls or institution-specific grading rules, add a secure backend.
