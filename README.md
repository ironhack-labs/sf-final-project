![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Enhance Banking and Loan Experiences

_Find below the general guidelines. Please check in with your instructor to confirm their specific requirements (if they have any). Good luck!_

<br>

## Introduction

This application is applicable for creating 3 types of Bank Accounts in the system. These bank accounts will notify users for their FD renewal and interest rates. Also timely Loans related requirement mails should be triggering to the users.

To make it a seamless experience for the end users, we need to make a strong system which can take required information from users and can utilize it for the respective user's view and their growth in terms of profit for both bank and users.

### Instructions: 

Mini projects are to be completed in groups. You will have to collaborate with classmates on this assignment. Should you need assistance, you should reach out to your instructional staff. This project will help you to be a good team player.

This project is Salesforce configuration project. Use this as an opportunity to challenge yourself and learn new things. You should meet all of the requirements listed below.

<br>

## Prerequisites

Because this project is Salesforce Configuration project you must complete the following tasks before starting:

- Use the new playground and implement the new configurations in it.
- Present the project in a custom Salesforce Application and ensure that all automations are thoroughly tested.
- App must include only the related tabs for these requirements. None other tabs should be part of the app.

<br>

## Submission

Once you finish the project, create a document having screenshots for all the requirements point by point and submit the same document on the provided URL.

**Note**: Upload document on Google Drive (or any other online platform that allows public sharing) and share public link to the document in the submission field in Student Portal.

<br>

## Technical Requirements

### Application must manage data for:

1. Account -> All accounts will be stored in it and should have 3 record types named - Salary Accounts, Transactional Accounts, Current Account.
2. Contact -> Related contacts for Accounts if the Account is a business or company Account.
3. Cases -> All the issues raised by respective contacts should be captured in case object.

**Note:** - Go through the entire user story and create fields per object as per usage. Test

<br>

### Development Requirements:

1. A welcome email should be triggered whenever there is any new Account or Contact gets created.
2. Required fields validations for all 3 involved objects.
3. Few new fields needs to be created on Account Object named- Interest Rate(Formula), Account Balance (currency), Calculated Interest (currency), Loan Type (PickList: Home Loan, Car Loan), Total Loan Amount (Currency), Loan Interest Rate (Mark Read Only on Page Layout), Monthly EMI (Currency), Remaining Loan Amount (Currency).
4. Interest Rate is a formula field, which needs to be calculated upon multiple record types, like for Salary Accounts it should be 6%, for Transactional Accounts it should be 5% and for Current Accounts it should be 3.8%
5. Salary Account may have 0 balance by the time of Account creation, whereas rest other type of account must have min 100 USD balance while creating them.
6. A trigger named AccountTrigger must be used to calculate and show Calculated Interest for all record types as per their respective interest rate and current balance.
7. Use the same AccountTrigger to calculate Loan Interest Rate for below Record Types, Loan Types and Loan Range Combination:<br>
   * Salary Account for Home Loan - Loan Range 0 - 100000, Loan Interest Rate = 8%;<br>
                    - Loan Range 100001 - 500000, Loan Interest Rate = 11%;<br>
                    - Loan Range 500001 - 1000000, Loan Interest Rate = 14%;<br>

   * Salary Account for Car Loan - Loan Range 0 - 100000, Loan Interest Rate = 8.4%;<br>
                    - Loan Range 100001 - 500000, Loan Interest Rate = 110.3%;<br>
                    - Loan Range Greater than 500000 - Error message - we do not provide loan beyond 500000 for this type of accounts.<br>
   
   * Transactional Account for Home Loan - Loan Range 0 - 100000, Loan Interest Rate = 9%;<br>
                           - Loan Range 100001 - 500000, Loan Interest Rate = 11.8%;<br>
                           - Loan Range 500001 - 1000000, Loan Interest Rate = 15.9%;<br>

   * Transactional Account for Car Loan - Loan Range 0 - 100000, Loan Interest Rate = 7%;<br>
                           - Loan Range 100001 - 500000, Loan Interest Rate = 10.9%;<br>
                           - Loan Range 500001 - 1000000, Loan Interest Rate = 13.6%;<br>

   * Current Account for Home Loan - Loan Range 0 - 1000000, Loan Interest Rate = 10%;<br>
                     - Loan Range 1000001 - 5000000, Loan Interest Rate = 12.5%;<br>
                     - Loan Range 5000001 - 10000000, Loan Interest Rate = 16.2%;<br>

   * Current Account for Car Loan - Loan Range 0 - 1000000, Loan Interest Rate = 9%;<br>
                     - Loan Range 1000001 - 5000000, Loan Interest Rate = 11.9%;<br>
                     - Loan Range 5000001 - 10000000, Loan Interest Rate = 14.6%;<br>

8. Calculate remaining Loan Amount as per Total Loan Amount and Loan Interest Rate.
9. Calculate Monthly EMIs for all types of loans and store the values in respective fields.
10. Create a lightning Web Component to display Account and Loan related information to the end Users while they are willing to see it. You can launch these details using an action as well.
11. Create a scheduled triggered flow to deactivate all the accounts which have not used (no transaction history) in past 3 years.
12. Use flow to send a thank you mail if any end user opt-in for any type of Loan. Use different templates for different types of loans.
13. Send email Reminder for Monthly EMIs payments along with the remaining amount details.
14. Create a feedback form using Lightning Web Components and send it to the Account holders for quarterly feedback.
15. Send a mail if any Case gets created against any issue, having information related to case which explains the SLA and resolving time for the end users.
16. Create a separate queue for all high priority cases and assign all the high priority cases to the same queue as owner. 
17. Create an application named Banking with Banco and add these 3 tabs (Accounts, Contacts, Cases) into it.

<br>

## Deliverables

- A working application having all listed features should be ready to be used.
- All the welcome mails should be triggers as per requirements.
- Entire process of Patient Journey should be streamlined.
- Project development and testing should be completed within 2 days.

<br>

## Presentations

For each of the projects you make at Ironhack, you will also have to make a presentation about it. Communication (including public speaking) is an important skill to practice.

### Format

- Talking with Slides: **10 minutes**
- Demo: **15 minutes**
- Total: **25 minutes**

<br>

### Presentation Structure

1. **Title Slide** (1 slide): your project's name & your name
2. **About Me** (1-2 slides):
   - Where are you from?
   - What are some interesting facts about you? (hobbies, travels, etc.)
3. **Project Elevator Pitch** (1-2 slides):
   - What is your project?
   - How does it work?
   - Why did you choose it?
4. **Technical Challenge** (1-2 slides):
   - What was **the most important** technical challenge you faced?
   - How did you overcome that challenge?
5. **Big Mistake** (1-2 slides):
   - What was **the biggest** mistake you made during this project?
   - What did you learn from it?
6. **Demo Slide** (1 slide): literally says "DEMO"
   with **a link** to your project so you can open it easily
7. **Closing Slide** (1 slide): your project's name, your name & a _"Thank You"_
8. **Total**: 7-11 slides

<br>

#### Presentation Structure Notes

- **Don't** include a slide just for the technologies.
- **Don't** include any code in your slides. Nobody will read it.
- **Don't** go into detail about how the app works. Your demo is where you want to do that.
- If you think that deviating from the structure improves your presentation, feel free to do so. This suggested structure is mostly for people who don't know what to do.

<br>

## Rubrics

In order to assess your project and ensure all requirements are met, a **rubric** will be used. This rubric is used to **evaluate your project** by your teaching staff but also to **communicate** what constitutes incomplete, acceptable and excellent performance across each of the learning outcomes for the final project. Take some time to review the rubric and ask your lead teacher any questions about it if necessary.

<br><br>

| **Learning outcomes**                                                                                                                            | **Domains**                                               | **0 - Incomplete**                                                                                                                                                                                                                                                                                                                                                                              | **1 - Fair**                                                                                                                                                                                                                                                                | **2 - Good**                                                                                                                                                                                                                                                                                                                                                                                                                                         | **3 - Excellent**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **_Create all custom objects, fields, record Types, Page Layouts and Validation rules_**                                                                                               | Salesforce Configuration, Databases, Application Architecture | Student failed to implement the basic Salesforce Object Structure. Student showed no evidence of creating any fields, record types or page layout. Basic Configuration is missing.                                                                                                                                                   | Student implemented necessary fields and other configs, but with an incomplete set of features. Fields validation have been partially completed.                                                                      | Student created a Salesforce object structure with the full set of features. The schema is well-defined with a partially implemented validation.                                                                                                                                                                                                                        | Student successfully implemented a Salesforce Object Structure with the full set of features following best practices. Students Created a full fledge Salesforce Structure to maintain data for all types of banking Accounts and having right fields and respective validations along with the right match fo record types and page layouts.                                                                                                                           |
| **_Properly create formula fields and flows_**                                                                                                   | Salesforce development, Databases, Process Automation | Student failed to create all the formula fields needed and implement the basic flows to automate the email processes.                                                                                                                                                                                                                                   | Student created all formula fields and flows but none of them are working properly as per requirements. Flows has been created but not triggering email and formulas are not calculating correct values.                            | Student adequately created all formula fields needed along with the creation of flows to automate the processes. Few of the functionality like email templates are not that much in shape, Rest other is good.                                                                                                                                                                                                                                   | Student adequately created all formula fields needed along with the creation of flows to automate the processes. All the flows and formulas are working as expected and all the best practices and naming conventions has been followed.                                                                                                                                                                                                                                                                            |
| **_Implement Triggers and other Back end Development_**                                                                                                 | Server-side development, Triggers                                   | Student didn’t implement the necessary triggers on their project.                                                                                                                                                                                                                                                                                                                 | Student implemented the triggers but their logic is not working as expected.                                                                                               | Student adequately implemented the triggers along with handlers. Logic is also working fine but trigger is not bulkified and hence will be broken up for bulk records DMLs.                                                                                                                                                                                                                               | Student successfully implemented all the triggers along with handlers and necessary logic which is working as per expectations. Also triggers are bulkified and following all the best practices.                                                                                                                                                                                                                                                    
| **_Implement Lightning Web Components with necessary back end Development_**                                                                                                 | Front-end development, Lightning Web Components                                   | Student didn’t implement the necessary Lightning Web Components in their project.                                                                                                                                                                                                                                                                                                                 | Student implemented the Lightning Web Components but their logic is not working as expected.                                                                                               | Student adequately implemented the Lightning Web Components along with their actual functionality. Everything looks good except few cosmatic changes and some JS glitches.                                                                                                                                                                                                                               | Student successfully implemented all the Lightning Web Components along with their actual functionality expectations. Also all the JS and related back-end operations are working as expected. 
| **_Test the functionalities of the application_**                                                                                                | Client and Server-side development, Testing, Code Quality            | Student didn't create any tests cases and classes (0% test coverage).                                                                                                                                                                                                                                                                                                                                             | Student created very few test classes so the bare minimum of the application is being tested (<50% test coverage).                                                                                                                                                                 | Student managed to create test classes for some of the functionalities in the application (50-75% test coverage).                                                                                                                                                                                                                                                                                                                                           | Student successfully created test classes for the majority of functionalities of the application (>75% test coverage).                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **_Properly handle exceptions and errors_**                                                                                                      | Client and Server-side development                                   | Student didn't implement error handling.                                                                                                                                                                                                                                                                                                                                                        | Student only applied generic error responses, or he/she didn't properly handle errors.                                                                                                                                                                                      | Student handles most of the errors properly but uses generic classes as Exception to catch every exception instead of using the specific ones.                                                                                                                                                                                                                                                                                                       | Student successfully implemented robust error handling over wrong data entry to the system also there is no glitches during email alerts and custom pages.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **_Write clean, modular and efficient code following best practices_**                                                                          | Code Quality                                              | Student has not followed best practices in writing clean, modular and efficient code. Student has unused code in the project and functions that are considered too large or perform multiple tasks. Student has not followed a consistent approach in naming the structure and organization of the files/folder. Student has not applied indentation conventions making the code hard to read. | Student has named files and folders logically and has organized them clearly and consistently. Student has partially applied indentation conventions to the source code and has mostly named functions and variables logically. Some unused code is within the project.     | Student has adequately named files and folders and has organized them clearly and consistently. Student has also applied indentation conventions to the source code and has named functions and variables logically. Student used advanced approaches to extract values from complex data structures to enhance code readability. There is no unused code within the project and utility functions are contained in separate self-descriptive files. | Student has adequately named all files and folders and has organized them clearly and consistently. Student applied indentation conventions to the source code and was meticulous in commenting on the code. Student has named functions and variables logically following the industry conventions. There is no unused code within the project and utility functions are contained in separate self-descriptive files. Student used advanced approaches to enhance code readability. |
| **_Document the application's features, configuration and technical specifications. Deliver a simplified Class Diagram and Use Case Diagram_**. | Career development                                        | Student didn’t make any attempt to document the project’s specifications.                                                                                                                                                                                                                                                                                                                       | Student provided a partially completed project README. Student has only partially documented the application’s features, configuration, or specifications in the README file. Student didn’t make a Class Diagram or diagram is created but it is not following UML syntax. | Student has created a well-structured and clear README file that covers all of the application’s features, configuration and specifications. Student has included credits, clearly listing any collaborators, team members and resources used that contributed to the project. Student created a Class diagram but there are some differences between the diagram and the final code.                                                               | Student has created a fully comprehensive and well-structured README file that not only clearly communicates the application’s features, configuration and specifications but goes into further detail justifying the choice for inclusion in the application. The student has added a license to the file and included credits, clearly listing any collaborators, team members and resources used that contributed to the project as well as badges. Class Diagram have been made and define the system clearly.                                   |
| **_Use Trello/other tools for Project Management_**                                                                                              | Client-side development                                   | Student has not used any Project Management Solution.                                                                                                                                                                                                                                                                                                                                           | Student has made use of a Project Management Solution.<br/>There are some tracked tasks that are left as uncompleted/unfinished and/or not all aspects of the project have been split into tasks.                                                                           | Student has made use of a Project Management Solution.<br/>All tracked tasks are completed and there are an adequate number of tasks that demonstrate that most of the project has been broken down into smaller tasks.<br/>The organization of the project management solution is basic or messy.                                                                                                                                                   | Student has made use of a Project Management Solution. <br/> All tracked tasks are completed and there are an adequate number of tasks that demonstrate that most of the project has been broken down into smaller tasks.<br/>Student has used tools such as color coding, subtasks, tags, etc. to properly organize the tasks in their project management solution making its use efficient and easy to read.                                                                                                                                          |
| **_Save and track changes in the source code using Git and GitHub_**                                                                             | Version Control                                           | Student did not create a repository for an app or has less than one commit per day.                                                                                                                                                                                                                                                                                                             | Student has created a repository for the project and has at least 2 commits per day.<br/>Student has not made use of feature-branch workflow to structure the development of the project.                                                                                   | Student has created a repository for the project and has at least 2 commits per day.<br/>Student has made use of feature-branch workflow to structure the development of the project.<br/>Student has unclear or ambiguous commit messages.                                                                                                                                                                                                          | Student has created a repository for the project and has at least 2 commits per day.<br/>Student has made use of feature-branch workflow to structure the development of the project.<br/>Student has clear and concise commit messages for most if not all commits that describe the purpose and changes since the last commit was made.                                                                                                                                                                                                             |
| **_Build a presentation and perform a demo to deliver your final results or the results of your group_**                                         | Career development                                        | Student did not present or demo their application or talk through their slides during the project presentations.                                                                                                                                                                                                                                                                                | Student presented and demoed their work.<br/>Key aspects of the project were missing from the presentation or parts were hard to understand leaving the audience confused.                                                                                                  | Student presented and demoed their work.<br/>All important information was presented in a way that someone would be able to follow and understand.<br/>There were some issues with timing, the aesthetic quality of the slides or an obvious lack of structure to the presentation.                                                                                                                                                                  | Student presented and demoed their work.<br/>All important information was presented in a way that someone would be able to follow and understand.<br/>The presentation stuck close to the agreed upon timing, the slides were aesthetically pleasing and easy to read and presentation followed a clear and logical structure taking the audience step by step through the project.                                                                                                                                                                  |
| **_BONUS: Enhance the application solution with extra features_**                                                                                | Server-side development                                   | Student didn’t implement any extra features.                                                                                                                                                                                                                                                                                                                                                    | Student implemented some extra features that may be partially working or that it is shown that there has been an effort in the design and development of the solution.                                                                                                      | Student implemented functional extra features that add value to the application. Extra features are properly tested and documented.                                                                                                                                                                                                                                                                                                                  | Student implemented fully functional extra features that add value to the application that goes beyond the scope of the project showing exceptional understanding of one or more concepts that were not covered in class (e.g. advanced data structures, advanced SOQL queries, or secure coding practices). The extra features are properly tested and documented.                                                                                                                                                                                    |

<br><br>

**Good luck and have fun!**