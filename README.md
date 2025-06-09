# DashboardAutomationTool (Code Confidential)
## Client: Bet365
### Objective:
This project is one I created on the client side at Bet365. All the code is proprietary information and cannot be shown or publically. In this README I'll be going over from a high level what the details of the tool, tech stack, purpose, and any more info to the best of my ability.

### Role: Sole Developer/Tool Owner

## Tech Stack:
**Languages:** (Go) Golang, Javascript, Typescript <br>
**Tools:** Goland, Postman,Bet365 Internal tools <br>
**Frontend Concepts:** HTML, CSS, Tailwind, Go HTML templates
**Backend Concepts:** REST APIs, Multithreading, Concurrency, Goroutines, Authentication, Data Processing, Error Handling, Logging
**Testing:** Unit Testing

**Key Features**:
- REST API Integration
- Concurrent Execution via Goroutines
- Scalable Modular Architecture
- Authentication & Secure Access
- HTML Form Rendering via Go Templates
- Configurable Workflows
- End-to-End Unit Testing

## Overview/Design
This tool was built for the sole purpose of automating work that was done as part of the Bet365 App rollout to different states. I created this tool to help automate repetitive processes that developers would usually spend days on for each state.

The tool can be broken down into the frontend and backend components:

**Frontend (Code Confidential):**
- Created a dynamic web UI using HTML, Tailwind CSS, GoHTML templates, and TypeScript.
- Webpage was mainly form-based inputs, depending on the server endpoints hit, allowing users to choose and run automation workflows based on required parameters
- After forms were submitted, the backend would call the required REST Apis to autoamte the workflow

**Backend (Code Confidential):**

The Backend is the meat of the project, that handles all business logic, automation, and testing. 

There are many different processes this tool looks at automating, including but not limiting to: <br>
**Deployments**- Can deploy many services automatically with a defined build configuration <br>
**Config changes**- Can make required config changes in Bet365 specific internal tools required for new state app deployments <br>


1. Project package structure was designed by each tool being automated and follow a standard MVC pattern using go modules
2. Created a local HTTP Go Server with multiple API routes that correspond to different automation workflows. Each route leads to a differnt frontend form which in turn follow a different backend flow.
3. Upon form submission the frontend Data would be passed to the backend a follow a data pipeline to clean and transform the data to be used for Restful HTTP requests
4. The Automated changes are done concurrently using Go Routines, Wait groups, and Channels to run a range of HTTP calls. Ive run build for over 100+ services at once, which manually can take a few days, which takes only a few seconds with Go routines.
5. Each Api call has built in Authentication, Error handling, and logging

### Performance wins:
Manual changes developers used to spend days work on now has been automated to finish within minutes. What used to take up to 4 days now takes about 1-2 hours to complete. This has reduced stress on developers, improved effenciency in our team, and allowed us to hit business milestones consistently ahead of schedule.





_____________
