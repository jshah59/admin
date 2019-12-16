# Research Bay
DSC Annual Solution Challenge Project by [DSC @ UIUC](bit.ly/dscuiuc)

### Overview

Research Bay is a a web and mobile platform to help UIUC students find research opportunities with professors. This document serves as a final outline and overview of the project's details, including goals and tasks for each team. Changes are still ongoing.

### Architecture

Research Bay will be a fullstack and cloud-based (serverless) web/mobile application. At this time, we predict the following technologies for each aspect of the application:

- Frontend: React.js + Node.js
- Backend: Firebase + GCP in JavaScript/Python
- Mobile: Firebase + Flutter
- Data/ML: Integrated into backend functionality in Python

Further details are subject to change and left up to the individual sub-teams.

### Final Goal

Research Bay will be a web and mobile platform open to students and professors. In a broad sense, Research Bay can be thought to be similar to LinkedIn and Handshake. However, it is unique in that it solely focuses on academia and research opportunities in the University of Illinois at Urbana-Champaign.

Students will be able to create and customize personal profiles that detail their interests, experience, and skills. Professors will be able to create postings for open research positions that describe the necessary background and skills they are seeking from interested students. All users will be able to search postings, profiles, and other users by using keywords that describe skills, research topics, and names/netid. Research Bay will also include a recommendation system that automatically suggests and matches students with professors and their research positions according to their profiles.

Students who are interested in a posting will be able to easily apply, and the professor will be able to quickly filter through the applications in a streamlined and standardized manner. The objective is to make this matching/application process seamless and hassle-free for both parties while ensuring successful/quality matches. The professor will then decide a subset of applicants to personally chat with and screen, using a built-in chat interface on the platform. At this point, further contact details to continue the conversation will also be provided to both parties. The professor will then have options to make final decisions (accept/reject) for the student candidates.

More to be added, and additional details are provided below.

### Teams + Design Details

*Please feel free to reach out to the project mentors: Isaac, Kavi, and Jayam, and the project lead: Neil via Slack or email with any questions or concerns.*

#### Frontend

The frontend team will be responsible for everything that relates to the GUI for the website. This will involve a significant amount of collaboration with backend and mobile teams.

- Outline of pages in the web interface:
  1. Login page
    * Let users create accounts and fill out their profile with a form
  2. Chat interface
    * Chat using APIs such as ChatKit for professors and students to communicate with each other
  3. Website settings
    * Home page interface, user preferences
  4. Search + recommendations (*Home*)
    * Search bar shows results in two tabs: users and postings (for research positions)
    * Recommendations are displayed on the same page as the search bar, before any searching
  5. Profiles + postings
    * Let users create accounts and fill out their profile with a standardized form
    * Professors:
      * Can create personal profile that links to all of their open postings
      * Can create multiple postings (one for each open research position)
      * Each posting describe required/wanted skills, background
    * Students:
      * Can create personal profile to showcase their skill sets, interests and experiences


- Current TODOs
  1. As a team, design a basic mockup/sketch of all of the pages and start brainstorming design ideas for how the website should look and flow
  2. Learn basic React and JavaScript to prepare for development
    * Complete Codecademy's ["Introduction to JavaScript"](https://www.codecademy.com/learn/introduction-to-javascript) course, for JavaScript beginners
    * Complete Codecademy's ["Learn ReactJS: Part I"](https://www.codecademy.com/learn/react-101) and ["Learn ReactJS: Part II"](https://www.codecademy.com/learn/react-102) courses, for React begineers
  3. Continue communicating and meeting within team and mentors to finalize design
  4. Start development

#### Backend

The backend team will be responsible for implementing any functionality (API, Database, networking/HTTP, etc) that is necessary for the function and success of the web and mobile platforms. A significant amount of collaboration will be done with the frontend, mobile, and data/ml teams.

- Outline of required API endpoints + database work
  1. Authentication (login + account creation)
    * Firebase will likely work for this
  2. Profile creation + viewing + edits
    * Including file uploads for resumes, postings, papers, etc
  3. Running and fetching recommendation calculations for each user
    * Recommendations should either be auto-generated on a schedule or upon updates to a user's profile
    * Upon login, users should be able to see their pre-calculated recommended students/professors/postings
  4. Searching
    * Calculate and fetch search results according to search keywords and tagged data in database
    * Algorithm for this to be fast and accurate
  5. Chat system
    * Two-way communication via text (use existing library/framework for this)


- Current TODOs
  1. Learn basic Firebase and GCP to prepare for development
    * Complete Google's ["Firebase web"](https://Codelabs.developers.google.com/Codelabs/firebase-web/#0) and ["Get to know Firebase for web"](https://Codelabs.developers.google.com/Codelabs/firebase-get-to-know-web/index.html?index=..%2F..index) Codelabs
    * Google's ["Cloud Functions for Firebase"](https://Codelabs.developers.google.com/Codelabs/firebase-cloud-functions/index.html?index=..%2F..index) Codelab is also recommended
    * Note: [GCP vs. Firebase](https://stackoverflow.com/a/42859932)
  2. Start communication and reach out to frontend and data/ml teams on their design ideas to get a better sense of what your API will specifically do
  3. Start development and continue streamlining API design/functionalities

#### Mobile

The mobile team will be responsible for implementing the mobile app version of Research Bay. As a result, this will involve both frontend and backend work, and a significant amount of collaboration with the frontend and backend teams to make sure that each teams' goals and work will be aligned with one another.

- Much of the required work and functionality of the mobile app mirrors a subset of the details already covered in the frontend and backend sections, so please refer to those for now. We will adjust and refine requirements as development starts and the team learns Flutter.


- Current TODOs
  1. As a team, design a basic mockup/sketch of all of the screens in the app and start brainstorming design ideas for how the mobile app should look and flow (including backend functionality and overview)
  2. Learn basics of Flutter and Firebase to prepare for development
    * Go through these [slides](https://docs.google.com/presentation/d/1uub8s169NDJI4_r6iteykKKNaP9pZiusZ52JQ3N824s/edit?usp=sharing) and complete the first two Codelabs linked in the final slide
    * Complete Google's [Firebase for Flutter](https://codelabs.developers.google.com/codelabs/flutter-firebase/#0) Codelab
  3. Communicate with frontend and backend teams as necessary. Refer to Isaac for any clarification as we understand Flutter is a relatively experimental aspect for the project.
  4. Start development, starting with a sample app, and continue researching Flutter and Firebase integration details

#### Data/ML

The Data/ML team will be responsible for implementing the recommendation system that will suggest matches to professors and students. It will also help the backend team with Research Bay's searching algorithms/functionality as needed. As a result, there will be a lot of collaboration with the backend team.

- Outline for search + recommendation system
  1. Recommendations
    * Students will be recommended/matched to professors and research position postings
    * Professors' postings will be matched to potential quality/successful student candidates
  2. Search results
    * Much be generated upon user searching with a given set of keywords, such as topics, skills, names
     * Separate results by category (posting, user, etc)
  3. Database schema
    * Must store all relevant user data in an easily-accessible manner (tag profiles/users with keywords, parse resumes, etc)
    * Must be quick and easy to query data from (optimize schema as development continues)


- Current TODOs
  1. Learn basic Firebase and GCP to prepare for development
    * Complete Google's ["Firebase web"](https://Codelabs.developers.google.com/Codelabs/firebase-web/#0) and ["Get to know Firebase for web"](https://Codelabs.developers.google.com/Codelabs/firebase-get-to-know-web/index.html?index=..%2F..index) Codelabs
    * Google's ["Cloud Functions for Firebase"](https://Codelabs.developers.google.com/Codelabs/firebase-cloud-functions/index.html?index=..%2F..index) Codelab is also recommended
    * Note: [GCP vs. Firebase](https://stackoverflow.com/a/42859932)
  2. Brainstorm and design what kind and types of data the application will need in order to sufficiently implement a successful recommendation + search system
    * What data will we collect and store on students, professors, postings, and their profiles?
  3. Sketch out database format for all of the necessary user and meta data stored by Research Bay
  4. Manually acquire or generate sample/training/dummy data for now, according to above specifications, and write initial algorithms to generate recommendations and results

### Deadlines

**We are requiring each project developer to complete the learning exercises for his/her team that are linked above during this winter break. We also expect each team to start communicating within itself (via Slack) to start the design/brainstorming process for the items described in the team's outline and TODOs.** Mentors will be checking in sometime during break to make sure all of the required tasks are being met on time, so feel free to reach out to them for help. We understand that not everyone will have experience with these platforms right off the bat, so we are happy to be resources for you as everyone tries to get up to speed.

For example, we expect the frontend developers to start collaborating on their mockups/wireframes of the various pages and the mobile developers to put together a sample Flutter app to familiarize themselves. Data/ML should compile a set of features/attributes/tags for users, profiles, and postings that will be required for the recommendations and searches. The backend team should draw a mockup/diagram that details a high-level overview of all of the backend components of the application, including cloud.


### Development Practices/Guidelines

Specific guidelines and instructions on working with Git, setting up your dev environment, etc will be sent out in the future as teams get closer to actual project development.
