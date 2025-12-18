# NutriBot

A comprehensive web application for meal planning, recipe management, and nutritional tracking designed to help users maintain a healthy lifestyle through intuitive meal organization and dietary goal tracking.

---

## Overview

NutriBot is a modern React-based web application that simplifies the process of meal planning and nutritional tracking. Developed as a team project, this application addresses the common challenge of maintaining healthy eating habits by providing users with an integrated platform to plan meals, discover recipes, track nutritional goals, and generate shopping lists automatically.

### Purpose and Motivation

In today's fast-paced world, many individuals struggle to maintain consistent, healthy eating habits due to poor planning and lack of organization. NutriBot was created to solve this problem by providing a centralized, user-friendly platform that makes meal planning accessible and manageable for everyone, regardless of their culinary expertise or dietary requirements.

### Key Features

- **Dashboard**: Provides a comprehensive overview of daily meals and nutritional information, offering users quick insights into their dietary intake and progress toward health goals
- **Meal Planner**: Features an interactive calendar interface that allows users to plan meals for days or weeks in advance, ensuring better preparation and reducing last-minute unhealthy food choices
- **Recipe Management**: Enables users to browse, search, filter, and save their favorite recipes, building a personalized recipe collection tailored to their preferences and dietary needs
- **Shopping List**: Automatically generates organized shopping lists based on planned meals, streamlining grocery shopping and reducing food waste
- **Weekly Reports**: Tracks nutritional goals and meal planning progress over time with visual charts and analytics, helping users understand their eating patterns and make informed decisions
- **User Authentication**: Implements a secure login system with persistent sessions and cross-tab synchronization, ensuring data privacy and seamless user experience across multiple browser windows
- **Onboarding Experience**: Guides new users through personalized setup including dietary preferences, budget constraints, scheduling preferences, and health goals

### Technology Stack

This application demonstrates proficiency in modern web development technologies and best practices:

- **Frontend Framework**: React.js (v18.2.0) - Component-based architecture for building interactive user interfaces
- **State Management**: Recoil - Modern state management library providing atomic state updates and derived state
- **Routing**: React Router DOM (v6.20.0) - Client-side routing for seamless navigation
- **UI Components**: Headless UI and Heroicons - Accessible, unstyled components and beautiful icons
- **Data Visualization**: Recharts and Chart.js - Interactive charts for nutritional tracking and progress visualization
- **Date Management**: date-fns and react-datepicker - Powerful date manipulation and calendar components
- **Styling**: Custom CSS with modern design principles - Responsive, accessible, and visually appealing interface
- **Testing**: React Testing Library and Jest - Comprehensive unit and integration testing suite

### Project Architecture

```
src/
├── components/           # Reusable UI components
│   ├── layout/          # Layout components (Header, Footer, etc.)
│   └── MealNotification # Notification system for meal reminders
├── pages/               # Page-level components
│   ├── dashboard/       # Main dashboard with meal overview
│   ├── meal-planner/    # Interactive meal planning calendar
│   ├── recipes/         # Recipe browsing and search
│   ├── recipe-details/  # Detailed recipe view with instructions
│   ├── shopping-list/   # Automated shopping list generation
│   ├── weekly-report/   # Progress tracking and analytics
│   ├── login/           # User authentication
│   └── onboarding/      # Multi-step user onboarding flow
├── recoil/              # Global state management atoms
├── data/                # Static data and mock recipe content
├── styles/              # Global styles and theme configuration
└── AuthContext.js       # Authentication context provider
```

### Team Contributions

This project was developed collaboratively by a team of four students:

- **Matthew Thao** - Project lead and initial architecture
- **Eli Goldberger** - Authentication system, secure login, and session management
- **Daniel Bauer** - UI/UX design, component styling, and frontend development
- **Lukas Singer** - Backend integration, data management, and API structure

---

## Installation Instructions

Follow these steps to set up NutriBot on your local development environment:

### Prerequisites

Before installing NutriBot, ensure you have the following software installed on your system:

- **Node.js** (version 14.0 or higher) - [Download here](https://nodejs.org/)
- **npm** (usually comes with Node.js) or **yarn** package manager
- **Git** - [Download here](https://git-scm.com/downloads)
- A modern web browser (Chrome, Firefox, Safari, or Edge)

### Step 1: Clone the Repository

Open your terminal or command prompt and clone the repository:

```bash
git clone https://github.com/yourusername/nutribot.git
cd nutribot
```

*(Replace `yourusername` with the actual repository owner's username)*

### Step 2: Install Dependencies

Install all required npm packages by running:

```bash
npm install
```

This command will install all dependencies listed in `package.json`, including:
- React and React DOM
- React Router for navigation
- Recoil for state management
- Recharts and Chart.js for data visualization
- Heroicons for UI icons
- Testing libraries (Jest, React Testing Library)
- And other supporting packages

The installation process may take a few minutes depending on your internet connection.

### Step 3: Verify Installation

After installation completes, verify that everything is set up correctly by running the test suite:

```bash
npm test
```

Press `a` to run all tests. You should see all tests passing (or at minimum, no critical errors).

### Step 4: Start the Development Server

Launch the application in development mode:

```bash
npm start
```

This command will:
- Start the React development server
- Automatically open your default browser to `http://localhost:3000`
- Enable hot reloading (changes to code will automatically refresh the browser)

If your browser doesn't open automatically, manually navigate to [http://localhost:3000](http://localhost:3000).

### Step 5: Build for Production (Optional)

To create an optimized production build:

```bash
npm run build
```

This creates a `build` folder with optimized, minified files ready for deployment to a web server.

### Troubleshooting Installation Issues

**Port 3000 is already in use:**
```bash
# On macOS/Linux:
lsof -ti:3000 | xargs kill

# Or specify a different port:
PORT=3001 npm start
```

**npm install fails:**
- Try clearing npm cache: `npm cache clean --force`
- Delete `node_modules` folder and `package-lock.json`, then run `npm install` again

**Module not found errors:**
- Ensure you're in the correct directory (project root)
- Try deleting `node_modules` and running `npm install` again

---

## Usage Instructions

### Getting Started with NutriBot

#### First-Time User Experience

1. **Launch the Application**
   - Open your browser to `http://localhost:3000`
   - You'll be greeted with the login page

2. **User Onboarding**
   - Click "Sign Up" or "Get Started" to begin the onboarding process
   - The multi-step onboarding flow will guide you through:
     - **Body Metrics**: Enter your height, weight, age, and activity level
     - **Dietary Preferences**: Select dietary restrictions (vegetarian, vegan, gluten-free, etc.)
     - **Health Goals**: Choose your primary goals (weight loss, muscle gain, maintenance, etc.)
     - **Budget Settings**: Set your weekly meal planning budget
     - **Schedule Preferences**: Configure your meal times and frequency

3. **Login**
   - After completing onboarding, use your credentials to log in
   - Your session will persist across browser tabs and page refreshes

### Core Features and How to Use Them

#### Dashboard

The Dashboard is your home base, providing an at-a-glance view of:
- Today's planned meals
- Daily nutritional summary (calories, macronutrients)
- Quick access to all features

**How to use:**
- Navigate to the Dashboard using the home icon in the navigation header
- View your meal plan for today
- Click on any meal card to see detailed recipe information
- Check your nutritional progress bars to track daily goals

#### Meal Planner

The Meal Planner helps you organize meals for the week or month ahead.

**How to use:**
1. Click "Meal Planner" in the navigation menu
2. Select a date on the calendar
3. Click "Add Meal" for breakfast, lunch, or dinner
4. Browse or search for recipes
5. Click a recipe to add it to that meal slot
6. Meals are automatically saved to your plan
7. Drag and drop meals to rearrange (if implemented)
8. Remove meals by clicking the "X" or trash icon on a meal card

#### Recipe Browser

Explore hundreds of recipes tailored to your dietary preferences.

**How to use:**
1. Navigate to the "Recipes" section
2. Use the search bar to find specific recipes by name or ingredient
3. Apply filters:
   - **Dietary restrictions**: Vegetarian, vegan, gluten-free, dairy-free
   - **Meal type**: Breakfast, lunch, dinner, snacks
   - **Cooking time**: Under 15 min, 15-30 min, 30-60 min, 60+ min
   - **Difficulty level**: Easy, medium, hard
4. Click any recipe card to view full details
5. Save favorites by clicking the heart or bookmark icon

#### Recipe Details

View comprehensive information about any recipe.

**Features include:**
- Full ingredient list with quantities
- Step-by-step cooking instructions
- Nutritional information breakdown
- Estimated preparation and cooking time
- Difficulty level
- Servings (adjustable)
- Option to add to meal plan
- Option to add ingredients to shopping list

#### Shopping List

Automatically generate shopping lists based on your meal plan.

**How to use:**
1. Plan your meals for the week using the Meal Planner
2. Navigate to "Shopping List"
3. View automatically compiled ingredients organized by category:
   - Produce
   - Proteins
   - Dairy
   - Grains & Bakery
   - Pantry Staples
   - Condiments & Spices
4. Check off items as you shop
5. Manually add or remove items as needed
6. Export or print your shopping list for grocery trips

#### Weekly Report

Track your nutritional progress and meal planning consistency.

**How to use:**
1. Click "Weekly Report" in the navigation
2. View visualizations including:
   - Calorie intake over the past 7 days
   - Macronutrient distribution (proteins, carbs, fats)
   - Meal planning adherence rate
   - Most frequently planned recipes
3. Use date selectors to view reports for previous weeks
4. Analyze trends to adjust your meal planning strategy

### Tips for Optimal Use

- **Plan ahead**: Schedule meals for the entire week on Sunday to ensure you stay on track
- **Batch cooking**: Look for recipes that can be prepared in bulk and stored
- **Flexibility**: Don't be afraid to swap meals if your schedule changes
- **Regular reviews**: Check your Weekly Report every Sunday to understand your patterns
- **Save favorites**: Build a collection of go-to recipes for quick meal planning

### Keyboard Shortcuts (If Implemented)

- `Ctrl/Cmd + K`: Quick search for recipes
- `Ctrl/Cmd + N`: Add new meal to today's plan
- `Esc`: Close modal windows

### Mobile Responsiveness

While optimized for desktop use, NutriBot is responsive and can be accessed on tablets and mobile devices for on-the-go meal planning and grocery shopping.

### Data Persistence

- All meal plans, recipe favorites, and user preferences are automatically saved
- Authentication tokens persist in localStorage for seamless login
- Cross-tab synchronization ensures consistent data across multiple browser windows

### Logging Out

- Click your profile icon or "Logout" button in the navigation header
- Your data is saved and will be available when you log back in

---

## Development and Testing

For developers who wish to contribute or modify the codebase:

### Running Tests

```bash
# Run all tests in watch mode
npm test

# Run tests once with coverage report
npm test -- --coverage --watchAll=false
```

### Code Structure Guidelines

- Components follow React functional component patterns with hooks
- State management uses Recoil atoms for global state
- Authentication state is managed through AuthContext
- Styling is component-scoped with CSS modules where appropriate

### Available Scripts

- `npm start` - Starts development server
- `npm test` - Launches test runner
- `npm run build` - Creates production build
- `npm run eject` - Ejects from Create React App (⚠️ one-way operation)

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Acknowledgments

- **React.js community** for the powerful and flexible framework
- **Heroicons** for the beautiful, accessible icon set
- **Recoil team** for modern state management solutions
- **University of St. Thomas** for supporting this capstone project
- All team members for their dedication and collaborative effort

---

*Developed as part of CISC 480 - Senior Capstone, Fall 2025*  
*University of St. Thomas* 