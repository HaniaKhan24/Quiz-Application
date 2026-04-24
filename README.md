# Quiz Management System

A comprehensive web-based Quiz Management System built with **ASP.NET Web Forms (VB.NET)** and **SQL Server**. This application provides a robust platform for administrators, teachers, and students to manage and participate in educational quizzes.

##  Features

###  Admin Dashboard
- **Overview**: Centralized control for system management.
- **Schedule Quizzes**: Assign specific times and subjects for upcoming quizzes.

###  Teacher Portal
- **Dashboard**: Track created quizzes and student performance.
- **Subject Management**: Organize questions by categories/subjects.
- **Question Bank**:
    - Add multiple-choice questions (MCQs).
    - Add True/False questions.
    - Set difficulty levels for each question.
- **Quiz Creation**: 
    - Create custom quizzes by selecting specific questions from the bank.
    - Set total time and total questions for each quiz.
    - Enable randomization of questions and shuffling of options.

###  Student Portal
- **Dashboard**: View available and upcoming quizzes.
- **Take Quiz**: 
    - Interactive quiz interface with a real-time countdown timer.
    - Instant submission upon completion.
- **Results**: View detailed results and performance history.

##  Tech Stack

- **Frontend**: ASP.NET Web Forms, CSS3 (Vanilla CSS).
- **Backend**: VB.NET.
- **Database**: SQL Server (Express/Standard).
- **Data Access**: ADO.NET (SqlClient).

##  Prerequisites

- **Visual Studio** (2019 or later recommended).
- **.NET Framework 4.8**.
- **SQL Server / SQL Server Management Studio (SSMS)**.

## Setup & Installation

1.  **Database Setup**:
    - Create a database named `QuizApplication` in your SQL Server instance.
    - Ensure you have the necessary tables: `Users`, `Subjects`, `Questions`, `QuestionOptions`, `Quiz`, `QuizQuestions`, and `Results`.

2.  **Configure Connection String**:
    - Open `Web.config`.
    - Update the `connectionString` under `<connectionStrings>` to match your SQL Server instance:
      ```xml
      <add name="QuizDB" connectionString="Data Source=YOUR_SERVER_NAME;Initial Catalog=QuizApplication;Integrated Security=True" providerName="System.Data.SqlClient"/>
      ```

3.  **Run the Project**:
    - Open the solution file in Visual Studio.
    - Build the project.
    - Press `F5` to start the development server and launch the application.

##  Project Structure

- `Login.aspx`: User authentication and role-based redirection.
- `AdminDashboard.aspx`: Administrator control panel.
- `TeacherDashboard.aspx`: Teacher-specific management tools.
- `StudentDashboard.aspx`: Student's personalized dashboard.
- `Teacher_AddQuestions.aspx`: Interface for building the question bank.
- `Teacher_CreateQuiz.aspx`: Quiz assembly and configuration.
- `Student_TakeQuiz.aspx`: Interactive quiz attempting interface.
- `StyleSheet.css`: Global styling for a modern and responsive UI.

## Security

- **Role-Based Access Control (RBAC)**: Ensuring users can only access pages relevant to their role (Admin, Teacher, or Student).
- **SQL Injection Prevention**: Using parameterized queries for all database interactions.
- **Session Management**: Secure user sessions to maintain state across pages.
