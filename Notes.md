# Notes

## Preparations for the Work to be Done
* Write a Project Plan, including:
    * A description of the problem to solve, listing:
        * The current problem that exists
        * The population who will benefit from your solution
    * Current existing solutions attempting to address the stated problem
        * For each solution, you should also address a short explanation of why the solution is not ideal
    * A detailed decsription of the proposed solution that will be put in place by your project
        * You should sell the reader on why your solution is superior to the existing ones currently being employed. 
        * Be critical: list the possible issues with the proposed solution
    * Development Details (including proposed technologies you plan to use, a general list of the features your solution will cover, etc.)
* Set up a regular meeting with your partners in the capstone project in order to decide on a proper divisoning of labor, how to best leverage each of your strengths and knowledge, and strategize over the work to be done each week.  

## First Phase: Planning and Scoping out the Project
* Look into relevant research in the areas related to your work.  This will allow you to leverage the knowledge of others who have come before you, and incorporate their learnings in the design of your own project.  
* Name the roles for each partner, so everyone is clear on their focus. 
* Carefully consider the audience you are targeting with the project.  
* Gather the technologies you plan to use to implement the project successfully.  Think carefully about the experience each team member has with the technologies, and the ease their use, and the timeline you are constrained by.  
* Brainstorm different challenges you may encounter, whether it is the prospect of reimbursing your interviewees, technicalities around gathering personal data in interviews or surveys, scheduling constraints, etc.  
* Confer with partners and be able to clearly state the goal of the app.  
* After each weekly meeting, walk away with clear action items for each member of the team so everyone is on the same page and all have the correct expectations. 
* Complete Needs Assessment assignment
    * Plan interview question beforehand carefully
        * Think carefully about how you phrase questions - try to do so in a neutral way, rather than placing judgment on alternate solutions to your project. (i.e., "How do you find the process of ___?" rather than "How much do you feel like you struggle in doing __")
* Storyboarding
    * Include what different main pieces of the app would look like, put to paper/google doc what you are envisioning so everyone is on the same page
    * Break down the entire app into subtasks for easier digestion
    * Envision scenarios of users actually navigating through the app to segment the app into individual pieces in need of storyboarding.  
    * Consider collecting data through surveys and interviews to inform the design of your project. 
        * Be thoughtful about the demographics of the participants in the survey.  They should be a good representation of the overall audience you are trying to serve (regional distribution, educational background, professions, age, gender, etc-- try to get a good mix). 
        * Think carefully about what sorts of demographic questions are necessary and appropriate for inclusion in the survey. 
        * Consider the accessibility of the interviews themselves, and how best to accommodate the participants to make the interview comfortable for them. 
* Design Document: 
    * List technologies to be used
    * Include general tasks with description of how to approach (links to tutorials you plan to use, why you think these components will work together well, etc.)
    * Include general timeline for each task and the order in which you will do them (dependency matrix of what tasks need to be completed before what other tasks, etc.).  
    * Other things to consider (perhaps that you foresee you may run into, but are not yet sure or need to still work out).  
* Consider the more specific research questions you are trying to answer with your project. 
* Funding: 
    * For compensating interviewees and participants, funding for interpreters
    * Examine potential funding opportunities (AccessComputing, Husky Seed Fund, etc.)
    * Complete applications for funding as required. 
* IRB:
    * Consider types of CITI training needed -- include in IRB to get approval of which trainings are necessary before actually completing them in case they are incorrect.  
    * Work with PI to come up with appropriate consent documents for different types of interaction with subjects (this is a big focus in filling out the IRB so they need to be prepared carefully beforehand unless the study is exempt).
    * When in doubt, contact the IRB office with questions and they can guide you along the right path (e.g., is my study heading towards exemption, review, or full board review?).  
    * Consider whether any parts of the overall study are IRB exempt, so those parts of the study can be acted upon earlier.  
* Set up GitHub repo (with appropriate permissions and associations with the correct organizations).
* Create a mailman list or email dedicated to the research group/project. 

## Second Phase: Development and Implementation
* We chose to use: GitHub pages, Firebase, Bootstrap
* To set up GitHub pages:
    * Create repository and under Settings, go to the Pages section.  Choose a source from which the site will be hosted, and click 'Save'.  
* To set up a Firebase instance:
    * Following this [tutorial](https://medium.com/pan-labs/dynamic-web-apps-on-github-pages-for-free-ffac2b776d45). 
    * Create a Firebase account
    * Create a project and give it an appropriate name
    * On the next page, choose to "Add Firebase to your web app"
    * You will be provided with some code to include in your html pages, and where to put it.  
        * [Here](https://firebase.google.com/docs/web/setup) is another great resource.  In particular pay attention to Step 3: Add Firebase SDKs and initialize Firebase.  We used the "From the CDN" option, in which case you need to include the specific Firebase products you want to use (Analytics, Authentication, etc.).  
    * Edit security permissions in Firebase by navigating to "Database" and then "Rules" and publish to save your changes.  
* Bootstrap Template
    * Find a Bootstrap template online that fits what you want for your web app and adjust to your app's specifications (listing your app's name, description, etc.). 
* Authentication
    * Include Firebase authentication tool (as in Step 3: Add Firebase SDKs and initialize Firebase listed above). 
    * Sign up:
        * Make form for getting email and password for sign up.  
        * Use `createUserWithEmailAndPassword` to create a new user account with the password the user provided. 
            * Note that Firebase hashes account passwords before storing (read more [here](https://firebaseopensource.com/projects/firebase/scrypt/)). 
        * Appropriately handle errors. 
    * Sign in:
        * Make form for getting email and password for sign in
        * Use `signInWithEmailAndPassword` to check the provided password against the account associated with the provided email.  
        * Upon successful sign in, redirect to desired page (such as profile).  
        * Appropriately handle errors. 
* Profile 
    * Find appropriate bootstrap template that will fit your needs.  
    * Include Firebase database tooling (as in Step 3: Add Firebase SDKs and initialize Firebase listed above). 
    * Make an "Edit Profile page" and on save, update database through Firebas API, with appropriate fields for saving user information.   
* Badges
    * Make a JSON file with badge values and their hierarchy, upload to Firebase Realtime Database. 
    * Populate a dropdown of badges on the "Edit Profile" page. 
        * Including hierachy -- add submenus!  
    * Create a structure for saving badges to each profile. 
    * Display a Bootstrap pill for each badge saved to a user's profile. 
    * Also allow users to remove badges! 
* Search
    * Sophie add here! :) 

## Third Phase: Testing & Interviews
