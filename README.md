# DashboardAutomationTool (Code Confidential)
### Objective:
This project is one I created on the client side at Bet365. All the code is proprietary information and cannot be shown or publically. In this README I'll be going over from a high level what the details of the tool, tech stack, purpose, and any more info to the best of my ability.

### Role: Sole Developer/Tool Owner

## Tech Stack:
**Languages:** Golang, Javascript, Typescript <br>
**Tools:** Goland, Postman,Bet365 Internal tools <br>
**Principles:** REST API/Servies, Multi-threading/GO routines, concurrency, Error handling <br>
**Key features:** Concurrency, Multithreading via go routines, REST API, REST Service, Authentication, Data Processing, Unit testing, and HTML Templating) <br>

## Overview/Design
This tool was built for the sole purpose of automating work that was done as part of the Bet365 App rollout to different states. I created this tool to help automate repetitive processes that developers would usually spend days on for each state.

The tool can be broken down into the frontend and backend components:

**Frontend (Code Confidential):**
The frontend was created using HTML, CSS, tailwind, gohtml, typescript, and JavaScript. Using the tech stack mentioned, I designed a form to get all the input needed to call various APIs depending on what work needs to be automated at that moment. The user is able to choose the automation workflow and pass the required parameters to the server. Then the backend will handle the rest.

**Backend (Code Confidential):**
The Backend is the meat of the project, that handles all business logic, automation, and testing. The project is split up into multiple packages based on the internal tool that is being automated. Each package is structured following a conventional MVC pattern.

There are many different processes this tool looks at automating, including but not limiting to:
1.	Deployments- Can deploy many services automatically with a defined build configuration
2.	Config changes- Can make required config changes in Bet365 specific internal tools required for new state app deployments

Running the project starts up a local server with multiple routes for the user to hit. Based on the route you choose, you get a different form to fill out to run an automated process. Upon filling out the form and hitting submit, request will be sent to our server. Our server will send the data through a pipeline to clean and transform the data into GO HTTP Requests. Then using multiple go routines and wait groups, it will call the required REST APIs to finish your request. Each Api call has built in Authentication, Error handling, and logging.

### Performance wins:
What used to take up to 4 days now takes about 1-2 hours to complete



_____________
