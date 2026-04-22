Project Description: NutriScan – Smart Calorie Measurement Website

NutriScan is a web-based calorie measurement platform that helps users track food intake, understand nutritional value, and reach health goals without the guesswork. The core idea is simple: take the friction out of calorie counting by combining food recognition, manual logging, and personalized analytics into one fast, privacy-respecting dashboard.

Problem We Solve
Most calorie apps rely on tedious search and select logging. Users quit because it takes two to three minutes per meal. Portion sizes are hard to estimate, home cooked meals are not in the database, and feedback is just numbers with no context. NutriScan reduces a food log to under 15 seconds while actually teaching portion awareness.

Core Features
Instant Food Recognition: Upload a photo or use your webcam. Our image model identifies items on the plate and estimates portion size using reference objects like cutlery. Users confirm or adjust with one tap. For packaged foods, barcode scan pulls exact label data.

Smart Manual Entry: A type ahead database of over one million foods with regional dishes, including Indian staples like roti, dal, chole, and street foods. Users can save custom recipes and the system auto calculates nutrition per serving.

Real Time Macro and Micro Breakdown: Every entry updates daily totals for calories, protein, carbs, fats, fiber, sugar, sodium, and key vitamins. Visual rings show progress toward user set targets.

Goal Based Coaching: On signup, NutriScan calculates BMR and TDEE using Mifflin St Jeor, then adjusts for activity level and goal: fat loss, maintenance, or muscle gain. Weekly check ins adapt targets based on logged weight and adherence.

Meal Insights: The Plate Score rates meals on protein density, fiber, and processing level. Over time, it highlights patterns like low protein breakfasts or weekend calorie spikes with actionable swaps.

Water, Steps and Weight Sync: Optional integration with Google Fit, Apple Health, and wearables so nutrition sits next to movement and body metrics.

Offline First PWA: Works on patchy networks. Logs cache locally and sync when online. Installs to home screen for app like speed.

Tech Stack
Frontend: React with TypeScript for a responsive SPA, TailwindCSS for styling, and Vite for sub second builds. Charting via Recharts for daily and weekly trends.

Backend: Node.js with Express, PostgreSQL for user data, Redis for session caching. Image recognition served by a Python microservice using a fine tuned EfficientNet model plus OpenFoodFacts API fallback.

Data: USDA FoodData Central, Indian Food Composition Tables, and user contributed recipes with moderation. Portion estimation uses depth cues and standard utensil sizes.

Auth and Privacy: OAuth2 plus email login. All images are processed ephemerally. Only the extracted text metadata is stored unless the user saves the photo. GDPR ready export and delete.

User Flow
Onboard: Enter age, sex, height, weight, activity, goal. Get daily calorie and protein targets.

Log: Snap meal, confirm items, adjust portions, done. Dashboard updates instantly.

Review: End of day summary shows remaining macros, streaks, and one insight like add 20g protein to hit your target.

Adapt: Weekly report auto adjusts calories by 100 to 200 based on weight trend and adherence.

Target Audience
Busy professionals, fitness beginners, and home cooks who want accuracy without spreadsheets. Especially useful in regions like India where existing apps miss local foods.

What Makes It Different
Instead of treating users like data entry clerks, NutriScan behaves like a nutritionist in your pocket. The focus is speed, local food accuracy, and feedback that teaches. No ads, no long paywalls. Free tier includes unlimited logging. Pro adds advanced micronutrient tracking and recipe scaling.

Roadmap
Phase 1: Core logging, barcode, Indian food database.  
Phase 2: Meal photo history, AI coach chat, family meal plans.  
Phase 3: Clinician dashboard for dietitians to monitor clients with consent.

NutriScan turns “What is in this thali” from a five minute research project into a ten second snapshot, so users spend time eating well, not logging it.
