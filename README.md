# Ex-1-Developing-AI-Agent-with-PEAS-Description
### Name: JENISHA TEENA ROSE F

### Register Number: 2305001010

### Aim:
To find the PEAS description for the given AI problem and develop an AI agent.

### Theory :
PEAS stands for:
'''

P-Performance measure

E-Environment

A-Actuators

S-Sensors

'''

It’s a framework used to define the task environment for an AI agent clearly.

### Pick an AI Problem

```

1. Self-driving car

2. Chess playing agent

3. Vacuum cleaning robot

4. Email spam filter

5. Personal assistant (like Siri or Alexa)
```

### PERSONAL ASSISTANT
### Algorithm:

Step 1: Initialize the Environment

Step 2: Add Tasks to the Environment

Step 3: Initialize the Personal Assistant Agent

Step 4: Agent Loop (Sense-Think-Act Cycle)

Repeat the following steps until there are no more tasks in the environment:

Step 5: Print Summary after the loop ends , print the list of perceptions, print the list of actions.

### Program:
```
# Personal Assistant Environment
class Environment:
    def _init_(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)

    def get_next_task(self):
        if self.tasks:
            return self.tasks.pop(0)
        return None

# Personal Assistant Agent
class PersonalAssistant:
    def _init_(self):
        self.percepts = []
        self.actions = []

    def perceive(self, environment):
        # The assistant perceives the environment by checking for new tasks
        task = environment.get_next_task()
        if task:
            self.percepts.append(f"New task received: {task}")
            return task
        return None

    def act(self, task):
        # The assistant acts based on the perceived task
        if task:
            action = f"Processing task: {task}"
            self.actions.append(action)
            print(action)
           return action
        return None

# Example usage
if _name_ == "_main_":
    # P: Performance Measure (e.g., successfully completed tasks)
    # E: Environment (The task list)
    environment = Environment()
    environment.add_task("Send email to John")
    environment.add_task("Schedule meeting with Sarah")
    environment.add_task("Order groceries")

    # A: Actuators (Performing the tasks)
    assistant = PersonalAssistant()

    # S: Sensors (Perceiving new tasks)
    print("Personal Assistant started...")
    while True:
        task = assistant.perceive(environment)
        if task:
            assistant.act(task)
        else:
            print("No more tasks for now.")
            break

    print("\nAssistant's perceptions:", assistant.percepts)
    print("Assistant's actions:", assistant.actions)

```
### Output:

![WhatsApp Image 2025-09-22 at 13 13 05_71a58d8c](https://github.com/user-attachments/assets/3e64b2df-dc92-4cdd-8994-3d6b3b01d9fd)


### Result:

Thus the given program for Developing-AI-Agent-with-PEAS-Description has been executed successfully.
