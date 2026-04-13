# Software Requirement Specification (SRS) Document

## Project: AI-Based Descriptive Exam Evaluation System

---

## 1. Introduction

The purpose of this Software Requirement Specification (SRS) document is to define the requirements for an AI-based descriptive exam system. This system allows users to write long-form answers (200–250 words) instead of selecting multiple-choice answers. The system evaluates responses either manually or using an AI model.

The system also tracks user behavior such as typing activity and time spent on each question to ensure fair evaluation.

---

## 1.1 Scope

The scope of this project includes:

- User attempting descriptive questions  
- Writing answers in a controlled environment  
- Tracking time spent on each question  
- Preventing copy-paste behavior  
- Evaluating answers using AI  
- Manual evaluation by admin  
- Displaying scores and feedback  

---

## 1.2 Out of Scope

The following are not included:

- MCQ-based exams  
- Video/audio-based answers  
- External plagiarism detection tools  
- Payment system  
- Certification generation  

---

## 2. Actors

- User (Student)  
- Admin (Evaluator/Teacher)  
- AI System (Answer Evaluator)  

---

## 3. Functional Requirements

### 3.1 User Authentication

- The system shall allow users to register and log in securely.  
- The system shall maintain user sessions during the exam.  

---

### 3.2 Exam Interface

- The system shall display questions to the user.  
- The system shall provide a textarea for writing answers.  
- The system shall enforce a word limit (200–250 words).  

---

### 3.3 Answer Writing and Tracking

- The system shall start tracking time only when the user starts typing.  
- The system shall pause tracking when the user becomes idle.  
- The system shall track time spent on each question.  
- The system shall detect tab switching behavior.  

---

### 3.4 Copy-Paste Prevention

- The system shall block copy, paste, and cut actions inside the answer field.  
- The system shall detect abnormal typing behavior.  

---

### 3.5 Answer Submission

- The system shall allow users to submit answers.  
- The system shall store answers along with time data and behavior metrics.  

---

### 3.6 AI Evaluation

- The system shall send the question and answer to an AI model.  
- The system shall receive a score and feedback from the AI.  
- The system shall store AI evaluation results.  

---

### 3.7 Manual Evaluation

- The admin shall view submitted answers.  
- The admin shall assign marks and feedback.  

---

### 3.8 Result Display

- The system shall display scores to users.  
- The system shall show AI feedback and/or manual feedback.  

---

## 4. Non-Functional Requirements

### 4.1 Performance

- The system shall respond quickly during typing and submission.  
- The system shall handle multiple users simultaneously.  

---

### 4.2 Security

- The system shall protect user data using secure authentication.  
- The system shall prevent unauthorized access.  

---

### 4.3 Reliability

- The system shall ensure minimal downtime.  
- The system shall prevent data loss during submission.  

---

### 4.4 Usability

- The system shall provide a simple and distraction-free interface.  
- The system shall display timers clearly to the user.  

---

### 4.5 Scalability

- The system shall support increasing number of users and exams.  

---

## 5. Use Case Scenarios

### 5.1 User Writes Answer

- Actor: User  
- Action: Starts typing answer  
- System Response: Starts timer and tracks activity  

---

### 5.2 User Submits Answer

- Actor: User  
- Action: Submits answer  
- System Response: Stores answer and triggers evaluation  

---

### 5.3 AI Evaluation

- Actor: System  
- Action: Sends data to AI  
- System Response: Receives score and feedback  

---

### 5.4 Admin Checks Answer

- Actor: Admin  
- Action: Reviews answer  
- System Response: Allows manual grading  

---

## 6. System Workflow

1. User logs in  
2. User starts exam  
3. Question is displayed  
4. User starts typing → timer starts  
5. User writes answer  
6. User submits answer  
7. AI evaluates answer  
8. Admin reviews (optional)  
9. Result is displayed  

---

## 7. Data Model Overview

### User
- id  
- name  
- email  
- password  

---

### Question
- id  
- questionText  
- wordLimit  

---

### Submission
- id  
- userId  
- questionId  
- answerText  
- timeSpent  
- aiScore  
- aiFeedback  
- manualScore  
- manualFeedback  
- tabSwitchCount  

---

## 8. Constraints

- The system must be built using JavaScript-based technologies.  
- The system depends on external AI APIs for evaluation.  
- Development should be completed within limited time.  

---

## 9. Assumptions

- Users have internet access  
- AI model is available and responsive  
- Users will follow exam rules  

---

## 10. Future Enhancements

- Advanced plagiarism detection  
- Proctoring using webcam  
- Detailed analytics dashboard  
- Multi-language support  
- Mobile application  

---

## Note

This document provides a structured overview of the AI-based descriptive exam system. It serves as a guide for development and implementation.