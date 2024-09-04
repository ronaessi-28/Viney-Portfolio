# Viney-Portfolio
Portfolio showcasing projects, including TuneTalk.

## TuneTalk: Revolutionizing Music Discovery
### Project Overview
TuneTalk is a platform designed to enhance music discovery through personalized recommendations and social interaction.

### Problem Statement
The platform addresses the challenge of users struggling to discover new music tailored to their unique tastes.

### Solution
- **Personalized Playlists:** Based on user activity and preferences. 
- **Social Sharing:** Discover music through friends.
- **Integration:** Works with popular music streaming platforms.
- **Community-Driven:** Music discussions and recommendations.

### Development Process
- **Research:** Conducted user surveys and market analysis.
- **Design:** Created wireframes and UI/UX designs using Figma.
- **Technology Stack:**
  - **Frontend:** React.js for building a responsive and dynamic user interface.
  - **Backend:** Node.js with Express.js for handling API requests and managing the server-side logic.
  - **Database:** MongoDB for storing user data, preferences, and music metadata.
  - **Authentication:** Implemented user authentication with JWT (JSON Web Token).
  - **Music Integration:** Utilized Spotify's API to fetch music data and provide streaming capabilities.
  - **Hosting:** Deployed the application on Heroku for hosting the backend and Netlify for the frontend.
  - **Version Control:** Used Git and GitHub for collaborative development and version control.
  - **Testing:** Employed Jest for unit testing and Postman for API testing.


### Challenges & Solutions
- **Challenge 1: Integrating Spotify API**
  - **Problem:** While integrating the Spotify API, we encountered issues with rate limits and data consistency, which affected the performance of real-time music recommendations.
  - **Solution:** Implemented caching strategies using Redis to reduce the number of API calls and improve response times. We also optimized data fetching by prioritizing frequently accessed information.

- **Challenge 2: User Authentication**
  - **Problem:** Implementing secure and scalable user authentication was challenging, particularly in managing session tokens and preventing unauthorized access.
  - **Solution:** Adopted JWT for token-based authentication and implemented secure cookies with HTTPOnly and Secure flags. This ensured that user sessions were managed securely across different devices.

- **Challenge 3: UI/UX Design for Personalization**
  - **Problem:** Designing a user interface that adapts to user preferences while maintaining a consistent and intuitive experience was difficult, especially given the wide range of user tastes.
  - **Solution:** Conducted user testing and iterated on the design based on feedback. We employed A/B testing to compare different layouts and interactions, leading to a more personalized and user-friendly interface.

- **Challenge 4: Scalability and Performance**
  - **Problem:** As the user base grew, the application began to experience performance bottlenecks, particularly in database queries and API response times.
  - **Solution:** Refined the database schema for better indexing, optimized query performance, and introduced load balancing to distribute traffic evenly across servers.


### Outcome & Impact
TuneTalk has the potential to significantly improve the music discovery process for users.

### Visuals & Media
- **Home Screen:**
  ![TuneTalk Home Screen](images/tunetalk-home.png)
- **Playlist Recommendations:**
  ![Playlist Recommendations](images/tunetalk-playlist.png)
- **Interactive Prototype:**
  [View TuneTalk Prototype on Figma](https://figma.com/proto/your-project-link)

### Reflection
- **Lessons Learned:** 
- Improved my understanding of integrating third-party APIs like Spotify's API.
- Learned how to effectively manage user authentication and session handling using JWT.
- Gained experience in designing user-centric interfaces that cater to diverse user preferences.
- Enhanced my problem-solving skills, especially in optimizing performance and scalability.

- **Future Plans:** 
- Plan to introduce a mobile app version of TuneTalk to reach a broader audience.
- Considering adding AI-driven music recommendations to further personalize user experiences.
- Exploring partnership opportunities with music streaming platforms for deeper integration.
- Planning to conduct more user testing to continuously improve the platform based on feedback.




### Steps

To run the entire TuneTalk project, which consists of a backend and a frontend, follow these steps:

1. Set Up Your Environment
Make sure you have the following installed on your system:

Node.js and npm: These are required to manage and run both the backend and frontend. You can download and install them from Node.js official website.

MongoDB: If you're using MongoDB for your database, ensure it’s installed and running. Alternatively, you can use a cloud service like MongoDB Atlas.

2. Clone the Repository
If you haven't already, clone your TuneTalk repository from GitHub
git clone https://github.com/ronaessi-28/Viney-Portfolio.git
cd Viney-Portfolio

3. Set Up the Backend
Navigate to the Backend Directory:

cd backend

Install Backend Dependencies:

npm install

Configure Environment Variables:

Create a .env file in the backend/ directory if it doesn't already exist.

Add necessary environment variables, such as the MongoDB connection URI and any other secrets:

MONGO_URI=mongodb://localhost:27017/tunetalk
PORT=5000

Start the Backend Server:
npm start

If you're using nodemon for development:

npm run dev
This will start the backend server, typically running on 

http://localhost:5000.

4. Set Up the Frontend

Navigate to the Frontend Directory:

cd ../frontend

Install Frontend Dependencies:

npm install

Start the Frontend Development Server:

npm start

This will start the frontend server, usually running on http://localhost:3000.

5. Verify Everything Is Working

Backend: Open your browser or use tools like Postman to test the backend API endpoints. For example, you can visit http://localhost:5000/api/users to ensure the API is working.

Frontend: Open your browser and go to http://localhost:3000 to check if the React frontend is loading correctly and interacting with the backend.

6. Additional Tips

Concurrent Development: 

If you want to run both servers simultaneously from the root directory, you can use a package like concurrently to manage both processes. Install concurrently in the root directory and create a script in the root package.json:

cd ..

npm install concurrently --save-dev

Add the following to the root package.json:

json
"scripts": {
  "start": "concurrently \"npm run start:backend\" \"npm run start:frontend\"",
  "start:backend": "cd backend && npm start",
  "start:frontend": "cd frontend && npm start"
}

Then run:

npm start

Database Seeding: If your project includes database seeding scripts, make sure to run them after setting up your backend.

Deployment: For deploying your project, you’ll need to configure deployment services (e.g., Heroku, Vercel, Netlify) and set up build processes and environment variables accordingly.


