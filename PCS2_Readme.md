# Multiplayer Network Quiz

### Objective
Create an interactive online quiz platform where multiple users can participate simultaneously.

Technology Stack
* Python 3
* PyQt 5

Assumptions
* Users have access to the server's IP address.
* The server has a parameter `NUM_PLAYERS` to limit the number of participants.
* The quiz starts when all players have joined.
* Project folder structure remains unchanged.
* Client attempts connection only when the server is operational.
* No connectivity issues between server and client during the quiz.

Execution Instructions
* Set `NUM_PLAYERS`.
* Provide server IP address to clients.
* Launch the server.
* Clients join the quiz with updated server details.
* Terminate the server after the quiz.

Rules and Guidelines
* Each participant receives questions with options.
* Participants choose one option per question.
* Questions have a time limit.
* All questions carry equal weight.
* Failure to answer a question within the time limit results in a default wrong response.
* If an option is selected but not submitted, the chosen option is recorded.
* Scores are revealed at the quiz end.
* Tie-breaker considers the time taken to answer.

User Interface
The UI includes radio buttons for selecting options, a submit button, and a timer. Each question has a default time limit of 10 seconds (`WAIT_TIME`), adjustable in the code.

Question Bank
Questions are stored in a `questionBank.txt` file. `getQuestions.py` updates the server's question list upon startup.

Code Parameters
* `WAIT_TIME`: Time allotted for each question (modifiable).
* `NUM_PLAYERS`: Number of participants.
* `SERVER`: Server address.
* `PORT`: Port address.
* `FORMAT`: Packet format for network communication.
* `DISCONNECT_MSG`: Message to signal client closure.

Code Files
 - Server: `with_ui/socket/server.py`
 - Client: `with_ui/socket/client.py`
 - UI: `with_ui/ui/question.py`
 - Question Fetcher: `with_ui/socket/getQuestions.py`
