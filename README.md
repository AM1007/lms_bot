# Interview Preparation Telegram Bot

[![Telegram Bot](https://img.shields.io/badge/Telegram-Bot-blue?logo=telegram)](https://t.me/Fortisec_LM_bot)

This Telegram bot helps users prepare for frontend development interviews by providing quizzes on HTML, CSS, JavaScript, and React topics.

## Features

- **Interactive Quizzes**: Multiple choice and explanatory questions on frontend technologies
- **Topic Selection**: Users can choose specific technologies or get random questions
- **Immediate Feedback**: Correct/incorrect answers with explanations
- **Error Handling**: Comprehensive error management and logging

## Technology Stack

- Node.js
- [Grammy](https://grammy.dev/) - Telegram Bot Framework
- [Express](https://expressjs.com/) - Web server for handling HTTP requests
- [random-js](https://www.npmjs.com/package/random-js) - Random number generation
- [dotenv](https://www.npmjs.com/package/dotenv) - Environment variable management

## How It Works

1. The bot greets users with a keyboard menu to select a topic
2. Upon selection, the bot delivers random questions from the chosen category
3. Users receive immediate feedback on their answers
4. For questions without multiple-choice options, users can request detailed explanations

## Project Structure

```
├── index.js         # Main bot application
├── package.json     # Dependencies and scripts
├── questions.json   # Quiz questions database
├── utils.js         # Helper functions
└── .env             # Environment variables (local development only)
```

## Installation and Setup

### Local Development

1. Clone the repository

   ```
   git clone https://github.com/AM1007/lms_bot.git
   cd lms_bot
   ```

2. Install dependencies

   ```
   npm install
   ```

3. Create a `.env` file in the root directory with your Telegram Bot API key:

   ```
   BOT_API_KEY=your_telegram_bot_api_key
   ```

4. Start the bot for development
   ```
   npm run dev
   ```

### Deployment on Render.com

1. Make sure your `package.json` has the correct scripts:

   ```json
   "scripts": {
     "start": "node index.js",
     "dev": "nodemon index.js"
   }
   ```

2. Create a new Web Service on [Render.com](https://render.com/)

   - Connect your GitHub repository
   - Select the Node environment
   - Set the build command: `npm install`
   - Set the start command: `npm start`

3. Add your environment variables:

   - `BOT_API_KEY`: Your Telegram Bot API key

4. Deploy your service and check the logs to ensure everything works correctly

## Usage

1. Start a chat with [@Fortisec_LM_bot](https://t.me/Fortisec_LM_bot) on Telegram
2. Send `/start` to begin
3. Select a topic (HTML, CSS, JavaScript, React) or choose "Випадкове питання" for a random question
4. Answer questions and get immediate feedback

## Contributing

Contributions are welcome! You can help expand the question database or improve the bot's functionality.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Deployment Status

[![Render](https://img.shields.io/badge/Render-Deployed-success)](https://render.com)

The bot is currently deployed on Render.com with an always-on web service to ensure prompt responses.

Happy interviewing! 💻 🚀
