
# Soul Sync

Soul Sync is an AI-powered mental health chatbot designed to provide emotional support, stress management techniques, and well-being assistance.

## Installation & Setup

### Prerequisites

Ensure you have the following installed:
- **Node.js** (Latest LTS version recommended)
- **npm** or **yarn**

### Clone the Repository

```bash
git clone https://github.com/kedar49/soul-sync.git
cd soul-sync
```

### Install Dependencies

```bash
npm install
```

### Configure API Key and Model

Create a `.env.local` file in the project root and add:

```ini
GEMINI_API_KEY=your-api-key-here
```

Then, update the model configuration in `src/config/gemini.js`:

```javascript
const apiKey = process.env.GEMINI_API_KEY;

import {
  GoogleGenerativeAI,
  HarmCategory,
  HarmBlockThreshold,
} from "@google/generative-ai";

const genAI = new GoogleGenerativeAI(apiKey);

const model = genAI.getGenerativeModel({
  model: "tunedModels/mentalhealthchatbot-02-7ul5vhgobzol", // update this model name if needed
});
```

Restart the development server to apply changes.

### Run the Application

```bash
npm run dev
```

Access the application at [http://localhost:5173](http://localhost:3000).
```

Simply replace the placeholder repository URL (`https://github.com/yourusername/soul-sync.git`) with your actual repository URL as needed.