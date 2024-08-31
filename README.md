# DigitalClock Component

*Deployed on Netlify 😉*\
[![Netlify Status](https://api.netlify.com/api/v1/badges/2e395283-300f-421c-8df7-c989163c8f6d/deploy-status)](https://digital-clock-app-ahmmmyoo.netlify.app/)

This `DigitalClock` React component is a simple digital clock that displays the current time, updates every second, and shows the time in 12-hour format with AM/PM notation. It also sets the document title to "My Digital Clock" when the component is mounted.

### React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Features

- Displays the current time in `HH:MM:SS AM/PM` format.
- Updates every second to show the accurate time.
- Changes the document title to "My Digital Clock" when the component is mounted.

## Installation

To use this component in your project, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Ahmmmyoo/vite-DigitalClockApp
   ```

2. **Navigate to the Project Directory**:

    ```bash
    cd your-repo-name
    ```

3. **Install Dependencies**:

    ```bash
    npm install
    ```

4. **Run the Application**:

    ```bash
    npm run dev
    ```

## Usage 

To include the DigitalClock component in your React application, import and use it as follows:

```jsx
import React from "react";
import DigitalClock from "./DigitalClock"; // Adjust the path as necessary

function App() {
  return (
    <div className="App">
      <DigitalClock />
    </div>
  );
}

export default App;
```

## Code Explanation

### Main Components and Logic

- **useState Hook**:

  - `const [time, setTime] = useState(new Date());`\
  - Manages the current time state, initialized to the current date and time.

- **useEffect Hook**:

  - The first `useEffect` sets the document title to "My Digital Clock" when the component mounts.
  - The second `useEffect` creates a timer using `setInterval` to update the time every second. It also returns a cleanup function to clear the interval when the component unmounts.

- **formatTime Function**:

  - Formats the current time into a    format.
  - Converts 24-hour time to 12-hour time and adds leading zeros where necessary.

- **padZero Function**:

  - Ensures that hours, minutes, and seconds are always displayed as two digits (e.g., `09` instead of `9`).

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to fork the repository, make changes, and submit a pull request. Please ensure that your contributions align with the project's coding standards and conventions.

1. Fork the Repository
2. Create a New Branch (`git checkout -b feature-branch`)
3. Commit Your Changes (`git commit -m 'Add some feature'`)
4. Push to the Branch (`git push origin feature-branch`)
5. Open a Pull Request

## LICENSE
[**MIT License**](./LICENSE)

Feel free to modify and use this DigitalClock component in your projects! 😊