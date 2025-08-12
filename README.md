# Standalone 12-Week Fitness Program App

This is a self-contained, single-file web application for planning and tracking a 12-week fitness program. It runs entirely in your browser with no need for installation, internet connection (after loading once), or user accounts.

The default program is designed for building the physical conditioning required for a basic mountaineering course, but it is fully customizable to fit any fitness goal.

  
Screenshots here

## Why Use This App?

*   **Privacy First:** All your data (current day, workout plan) is stored locally in your browser's `localStorage`. Nothing is ever sent to a server.
*   **Works Offline:** Once the HTML file is loaded, you don't need an internet connection to use it.
*   **Fully Customizable:** You can edit the entire workout plan, including warm-ups, exercises, and cool-downs, directly within the app. You can also import and export your configurations as a JSON file.
*   **Portable:** It's a single file. Save it anywhere, open it in a browser, and you're ready to go.
*   **Free & Open Source:** No ads, no subscriptions.

## Features

*   **Complete 12-Week Program:** A structured day-by-day plan with a 6-days-on, 1-day-rest cycle.
*   **Interactive Workout Mode:** An active session tracker with timers, set counters, rest periods, and audio cues.
*   **Exercise Guidance:** Each exercise includes a description, notes, and a direct link to a YouTube video guide.
*   **Custom Goal Setting:** Define and view your high-level fitness goals using a built-in Markdown-enabled editor.
*   **Light & Dark Modes:** A theme toggle for your viewing comfort.
*   **Progress Tracking:** The app automatically saves your progress, remembering which day you're on.

## How to Use

1.  **Download:** Get the `workout-app.html` file from this repository.
2.  **Open:** Open the file in any modern web browser (like Chrome, Firefox, Safari, or Edge).
3.  **Start:** That's it! The application will guide you through the program.

Your progress is automatically saved in the browser you use. To continue your program, simply open the same file in the same browser.

## For Advanced Users & Developers

This application is built with vanilla HTML, CSS, and JavaScript, making it easy to modify.

### Customizing the Workout Plan

You have two primary ways to alter the workout program:

1.  **Live Editor:** Click the "Edit Plan" button in the app. This opens a modal where you can directly edit the JSON that defines the entire workout structure.
2.  **Import/Export:** You can export the current configuration to a `.json` file. This is useful for backing up your plan or sharing it with others. You can then import a `.json` file to load a new program.

### The Configuration Structure

The core of the app is a single JSON object with a few key properties:

*   `fitnessGoals`: A string (with Markdown support) for your high-level goals.
*   `warmUp`: An array of exercise objects that runs before every workout.
*   `coolDown`: An array of exercise objects that runs after every workout.
*   `workoutPlan`: A nested array representing `[weeks][days][exercises]`.

An `exercise` object has the following structure:
```javascript
{
  "name": "Push Ups",      // The name of the exercise
  "type": "reps",          // "reps", "time", "failure", or "info"
  "reps": 10,              // Number of repetitions
  "sets": 3,               // Number of sets
  "time": null,            // Duration for time-based exercises
  "unit": null,            // "seconds" or "minutes"
  "description": "...",    // How to perform the exercise
  "notes": "...",           // Additional tips or modifications
  "youtubeLink": "..."     // A URL to a video guide
}```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
