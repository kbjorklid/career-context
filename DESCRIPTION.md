# AI Professional Writing Assistant

## Project Purpose

This project is a desktop application designed to help users create high-quality, personalized professional documents such as cover letters, CV text, and more. ✍️

The application works by first building a comprehensive professional profile for the user. It gathers context from multiple sources:
* **Free-form narratives**: The user's own description of their professional identity.
* **Structured work history**: A formal list of roles and responsibilities.
* **AI-driven Q&A**: An interactive session to uncover key skills and accomplishments.
* **Document analysis**: The ability to parse uploaded documents like existing CVs.

This rich, aggregated context is then used by an AI to generate tailored documents that accurately reflect the user's unique experience and skills.

***

## Core Frameworks & Tools

The application will be built as a modern, efficient desktop application using a pure TypeScript/JavaScript stack.

* **Build Tool & UI Library**: **Vite + React**
    * We will use Vite to provide an extremely fast development server and to build the application. This is simpler and faster than other frameworks for a desktop app. The UI itself will be built with React.

* **UI Component Library**: **shadcn/ui**
    * To ensure a professional and polished look without deep CSS knowledge, we will use `shadcn/ui`. It provides beautiful, accessible, and customizable components that we can easily adapt.

* **AI Orchestration**: **LangChain.js**
    * This powerful library will allow for sophisticated management of prompts, connection to various LLMs, and the creation of complex chains needed to process the user's profile and generate documents.

* **Desktop Packager**: **Tauri**
    * To transform the React application into a native desktop executable, we will use Tauri. This ensures the final app is lightweight, fast, and secure, using the OS's native web-view for maximum efficiency.

***

## Core Libraries & Utilities

To accelerate development and handle common tasks efficiently, we will use the following libraries:

* **Routing**: **TanStack Router**
    * To manage navigation between different pages of the application. We will use its file-based routing system, which is intuitive and simplifies page management.

* **Form Management**: **React Hook Form**
    * For creating performant and flexible forms to capture user input, such as their work history and Q&A answers.

* **Schema Validation**: **Zod**
    * To define data schemas and ensure all user input is valid and type-safe. This will be used alongside React Hook Form for robust validation.

* **Icons**: **Lucide React**
    * The default icon library for `shadcn/ui`, providing a clean, consistent, and comprehensive set of icons to enhance the user interface.

***

## Data Storage & Configuration

To ensure simplicity, user control, and portability, the application will use a local file-based system for storing all data—no external databases are required.

* **User Content (Markdown Files)**: All user-generated context—narratives, work history, Q&A answers, and extracted CV text—will be stored in individual `.md` files. This approach makes the data human-readable, easily editable with any text editor, simple for the LLM to parse, and straightforward for the user to back up or move.

* **Application Settings (JSON File)**: A single `settings.json` file will be used to store user preferences and application configuration. This includes settings like the selected AI model, theme choice (e.g., dark/light mode), and API keys. This standard JSON format is easy for the application to read and write.