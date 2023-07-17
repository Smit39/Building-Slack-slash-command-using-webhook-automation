# Streamline workflows with DronaHQ’s Automations for Slack slash commands

At DronaHQ, we believe in continuously improving our internal operations to enhance productivity and streamline workflows. Recently, we faced a common challenge many teams encounter – the need to retrieve lead details quickly without leaving our communication platform. In our case, it is Slack. To overcome this hurdle, we sought after Slack slash commands and DronaHQ’s Automation Builder, an add-on to our existing low code platform, and integrated it with our CRM tool. The result? A seamless and efficient lead management system that optimized our team’s productivity. In this blog, we’ll explore the benefits of leveraging DronaHQ’s Automation Builder to build Slack commands and bring everything under the Slack window.

## The Challenge: 
Like many teams, our communication heavily relies on Slack. We found ourselves constantly switching between Slack and our CRM tool to fetch lead details upon request. And while the process of looking up details from our CRM would take a few minutes at maximum, the task hindered collaboration and impacted our overall efficiency. We knew there had to be a better way to streamline this little process of back-and-forth communication.

![Slack conversation to request CRM lead details](https://cdn1.dronahq.com/wp-content/uploads/2023/05/image4-1-768x293.png)

## The Solution:
We turned to our Automation Builder, an incredible tool that lets one design [schedule-based or webhook-based automations](https://www.dronahq.com/automation/), tailored to our specific needs. Leveraging the power of the Automation Builder, we designed a solution that would fetch lead details from our database directly within Slack, eliminating the need for manual searches and minimizing disruption to our ongoing tasks.

>Learn how we use Automation to power our Slack Commands. [Watch tutorial](https://www.dronahq.com/tutorial-build-slack-commands/)

## The Slack Commands Implementation:
**1.Slack Slash Commands**:
The first step was to create a custom [Slack Slash command](https://api.slack.com/interactivity/slash-commands). This slash command will be driving the webhook trigger inside DronaHQ Automation, prompting the automation to fetch lead details based on specific requests. To ensure security and authorization, the slash command sent an authentication key and the user’s email ID to our system.

![triggering slack slash command](https://cdn1.dronahq.com/wp-content/uploads/2023/05/image3-1-768x453.png)

**2.Automation in DronaHQ**:
The magic happened within the Automation Builder.

1. We configured a webhook-based automation that received the trigger from the slash command. The automation, using the provided email ID, interacted with our CRM database, retrieving the requested lead details from our custom database.

![webhook based trigger to start the automation in dronahq](https://cdn1.dronahq.com/wp-content/uploads/2023/05/image1-1-768x387.png)

2. Next up we add tasks to [1] authorize the command to ensure only when it’s triggered by an approved user, we fetch further information about lead. [2] fetch the lead information from the database, and [3] to make the information more readable on Slack, we transform the data into a clean and organized JSON format.

3. Finally the message is sent over to Slack.

## The Results:
With a simple slash command, the requested lead information was delivered directly to Slack in a format that was easy to read and share.

But the benefits didn’t stop there. The custom automation not only streamlined our lead management process but also improved collaboration within the team. Our team members no longer have to leave Slack to fetch lead details, saving valuable time and reducing disruption to ongoing conversations. 

### DronaHQ as a middleware logic builder
DronaHQ provides a powerful platform for building middleware logic to process Slack commands and integrate them with your backend database. Here’s how DronaHQ can assist you in implementing and managing this process:

### Logic Implementation:
DronaHQ allows you to define the logic required to process Slack commands and perform the desired actions. Using the Automation Builder, you can design workflows that encompass the entire process, from receiving the command to executing the necessary operations.

### Command Validation:
With DronaHQ, you can validate the Slack command and its arguments to ensure correctness and completeness. You can define rules and conditions within the automation to verify the input before proceeding further.

### Backend Database Interaction:
DronaHQ supports integration with various backend databases through APIs and connectors. You can leverage these capabilities to interact with your backend database, whether it involves retrieving existing data, updating records, or inserting new information. DronaHQ provides a user-friendly interface to configure these database interactions.

### Business Logic and Data Transformations:
If you require additional business logic or data transformations, DronaHQ enables you to define and incorporate these within your workflows. You can use visual builders, scripting, or custom functions to manipulate data, perform calculations, or apply specific business rules as needed.

### Error Handling and Response Management:
DronaHQ allows you to handle error cases and provide appropriate responses back to Slack. You can define error-handling logic within your workflows, such as sending error messages or notifications to relevant stakeholders. DronaHQ also supports conditional branching and decision-making capabilities, allowing you to handle different scenarios based on the outcome of operations.

>Learn how to build Slack slash commands in under 10 minutes. [Register now](https://www.dronahq.com/tutorial-build-slack-commands/)

By utilizing DronaHQ’s Automation Builder, you can simplify the development and management of middleware logic for processing Slack commands and integrating with your backend database. It provides a low-code environment that empowers you to design complex workflows without extensive coding knowledge, accelerating your development process and improving efficiency.

Ready to streamline your Slack workflows with powerful middleware logic? [Explore DronaHQ’s Automation Builder](https://www.dronahq.com/automation/) today and take your integration capabilities to new heights!

>[Here is a quick video tutorial for you to follow along](https://www.youtube.com/watch?v=d_4CbEhldAc)


## FAQs
**1.What is a custom Slack slash command?**

A custom Slack slash command is a feature that allows you to create a custom integration in Slack, enabling users to trigger specific actions or retrieve information by typing a command into the message input field. When a user enters a slash command (e.g., “/weather San Francisco”), Slack sends a request to a specified endpoint (usually a web service or API) with the command and any additional parameters. The endpoint then processes the request and sends a response back to Slack, which is displayed to the user.
Custom slash commands are often used to integrate external services, tools, or bots into Slack, providing quick access to functionality without leaving the Slack interface. For example, you can create a slash command to search a company’s knowledge base, retrieve data from a database, perform actions in other applications, or interact with custom-built bots.

**2.What are some important Slack slash commands**

/help: Displays a list of available Slack commands and their descriptions.

/channel: Allows you to create or join a channel.

/invite: Invites a user to join a specific channel.

/leave: Allows you to leave a channel.

/topic: Sets or displays the topic of a channel.

/mute: Temporarily mutes notifications from a channel.

/unmute: Unmutes notifications from a channel.

/dm: Sends a direct message to a specific user.

/away: Sets your status as away.

/status: Sets a custom status message.

/remind: Sets a reminder for yourself or a channel.

/collapse: Collapses a long message or code block.

/snippet: Creates and shares a code snippet.

/poll: Creates a poll for a channel.

/giphy: Displays a random GIF based on a keyword.
