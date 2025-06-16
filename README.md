# dialogflow-api-gateway
This project serves as an API gateway for Dialogflow, designed to facilitate communication between frontend applications and the Dialogflow service. It acts as an adapter, simplifying the integration of Dialogflow's conversational AI capabilities into web or mobile interfaces. This gateway handles request authentication, session management, and streamlines the data exchange between the client-side and Dialogflow's API.

## Features
- **Request Handling:** Manages and forwards API requests from the frontend to Dialogflow.
- **Session Management:** Handles Dialogflow session creation and maintenance.
- **Authentication:** Securely authenticates requests to Dialogflow.
- **CORS Support:** Includes `cors` middleware, allowing cross-origin requests from frontend applications.
- **WebSocket Support:** Includes `ws` library, potentially for real-time communication.

## Prerequisites
- **Node.js and npm:** You'll need Node.js (which includes npm) installed on your system.
- **Dialogflow Account:** A Google Cloud Project with the Dialogflow API enabled.
- **Dialogflow Agent Credentials:** You will need a service account JSON key file for your Dialogflow agent to authenticate requests.

## Installation
1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd dialogflow-gw
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```

## Usage
1. **Running the application:**
   Start the API gateway using the following command:
   ```bash
   npm start
   ```
   This will typically start the server on `http://localhost:3000` (or another port if configured differently).

2. **Interacting with the gateway:**
   Once the server is running, frontend applications can make API requests to the gateway's defined endpoints. The gateway will then forward these requests to your Dialogflow agent, handle session management, and return Dialogflow's responses.

## Configuration
Before running the application, you need to set up the following environment variables:

- **`GOOGLE_APPLICATION_CREDENTIALS`**: The absolute path to your Dialogflow service account JSON key file. This file is necessary for authenticating with the Dialogflow API.
  ```bash
  export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account-file.json"
  ```

- **`DIALOGFLOW_PROJECT_ID`**: Your Google Cloud Project ID where your Dialogflow agent is located.
  ```bash
  export DIALOGFLOW_PROJECT_ID="your-dialogflow-project-id"
  ```

- **`PORT`** (Optional): The port on which the API gateway will listen. If not set, it will default to the application's preset (e.g., 3000).
  ```bash
  export PORT=3000
  ```

You can set these variables in your shell environment or use a `.env` file with a library like `dotenv` if you prefer to manage them per project.

## Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix:
    ```bash
    git checkout -b feature-or-bugfix-branch
    ```
3.  Make your changes. Please ensure your code adheres to the existing style and that all tests pass.
4.  Commit your changes with a clear and descriptive commit message:
    ```bash
    git commit -am 'feat: Add some amazing feature'
    # or
    # git commit -am 'fix: Resolve a pesky bug'
    ```
5.  Push your changes to your forked repository:
    ```bash
    git push origin feature-or-bugfix-branch
    ```
6.  Create a new Pull Request against the main repository's `main` or `master` branch.

We appreciate your contributions!

## License
This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
