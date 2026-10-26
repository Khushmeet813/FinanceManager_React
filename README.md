ApexLedger
ApexLedger is a personal finance management web application built with React and Vite. It brings common finance tasks together in one interface, including a dashboard, receipt storage, bill and subscription tracking, financial news, and reports.
Features
- Dashboard — access the main finance workspace.
- Receipt Vault — organize and review receipt records.
- Bills & Subscriptions — keep track of recurring bills and subscriptions.
- Financial News — browse finance and market-related articles using the GNews API.
- Reports — access finance reporting tools.
- Authentication pages — sign-up, login, and profile pages.
- Client-side routing — navigate between pages using React Router.
- State management — Redux Toolkit and React Redux are included for application state.
- Export support — ExcelJS and jsPDF are included for spreadsheet and PDF-related functionality.
Tech Stack
- React
- Vite
- React Router
- Redux Toolkit
- React Redux
- GNews API
- ExcelJS
- jsPDF
- HTML and CSS
Requirements
Install the following before running the project:
- Node.js (a current LTS release is recommended)
- npm (included with Node.js)

Getting Started
1. Clone or download the repository
If you are cloning the repository, run:
git clone <repository-url>
Then open the project folder that contains package.json. In this project, that folder is ApexLedger_Project.
2. Open the project in VS Code
Open the ApexLedger_Project folder in Visual Studio Code, then open Terminal → New Terminal.
3. Install dependencies
npm install
4. Configure the GNews API key
Create a .env file in the same folder as package.json and add:
VITE_GNEWS_API_KEY=your_gnews_api_key
Replace your_gnews_api_key with your own API key from GNews.

Environment variables are read when Vite starts, so restart the development server after changing .env.
Security note: Vite variables prefixed with VITE_ are exposed to client-side browser code. Do not use this setup to protect a secret API key in a public production deployment. For production, route API requests through a backend that keeps the key private.

5. Start the development server
npm run dev
Open the local URL printed in the terminal, usually http://localhost:5173/. If that port is already occupied, Vite may select another available port and print a different URL.
Available Scripts
Command	Description
npm run dev	Starts the Vite development server.
npm run build	Creates a production build in the dist folder.
npm run preview	Serves the production build locally for preview.


Project Structure
ApexLedger_Project/
├── public/
│   ├── CSS/
│   ├── JS/
│   └── pages/
├── src/
│   ├── features/
│   │   └── news/
│   ├── main.jsx
│   ├── router.jsx
│   ├── store.js
│   └── app.css
├── .env.example
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
The public/pages/ directory contains page assets used by the application, while src/ contains the React entry point, routing, state setup, and feature components. Some filenames may vary as the project evolves.