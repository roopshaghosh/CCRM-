# CCRM- Markdown

# Campus Course & Records Manager (CCRM)

This is a comprehensive console-based Java application designed to manage the core data and processes of a higher education institution. It's built to handle everything from student and course information to managing enrollments and grades, all while keeping your data safe with robust file operations.

# Project Overview

The Campus Course & Records Manager (CCRM) is a hands-on project that puts fundamental and advanced Java programming concepts into a single, functional application. It's a great example of object-oriented programming, modern Java APIs, and file handling in action.

Key Features:

* Student Management: You can create, list, update, and even deactivate student records.
* Course Management: Easily create, update, and deactivate courses, and assign instructors to them.
* Enrollment & Grading: Manage student enrollments, making sure they don't exceed credit limits, and handle grading and GPA calculations.
* File Operations: Import and export data in CSV format using modern NIO.2 file operations.
* Backup System: Create timestamped backups with recursive directory operations to protect your data.
* System Reports: Generate comprehensive statistics and reports to get a clear overview of the system.

# The Evolution of Java

Java has a rich history of evolution, constantly improving to meet the needs of modern development. Here's a brief timeline:

* 1995: Java 1.0 - The original release that introduced the "Write Once, Run Anywhere" (WORA) philosophy.
* 1997: Java 1.1 - Added new features like inner classes and JDBC (Java Database Connectivity).
* 1998: Java 2 (J2SE, J2EE, J2ME) - A major update that established the three main platforms: Standard Edition, Enterprise Edition, and Micro Edition.
* 2004: Java 5 (J2SE 5.0) - A huge release that brought us generics, enums, and the enhanced for-loop, among other things.
* 2014: Java 8 - A game-changer with the introduction of lambda expressions and the Streams API, making functional programming in Java a reality.
* 2017: Java 9 - Introduced the Java Platform Module System (JPMS), which modularized the JDK.
* 2018: Java 11 - The first long-term support (LTS) release under the new release cadence, which removed some of the older Java EE modules.
* 2023: Java 21 - The latest LTS release, featuring modern concurrency with virtual threads and enhanced pattern matching.

# Java Platform Comparison

Here’s a simple breakdown of the different Java platforms:

* Java SE (Standard Edition): This is for building standard desktop, server, and embedded applications. It includes the core Java APIs, which is what this project uses.
* Java EE (Enterprise Edition): This platform is for large-scale, multi-tiered enterprise applications. It provides APIs for things like servlets, JSPs, and web services.
* Java ME (Micro Edition): This version is specifically for mobile and embedded devices with limited resources.

# Java Architecture: JDK, JRE, and JVM

The Java platform is built on three key components that work together seamlessly.

* JDK (Java Development Kit): Think of this as the complete toolbox for a Java developer. It includes the compiler ('javac'), a debugger, and all the other tools you need to write and build a Java program.
* JRE (Java Runtime Environment): This is what you need to run a Java program. It includes the JVM and the necessary class libraries. You can't develop with it, but you can definitely run applications.
* JVM (Java Virtual Machine): This is the magic behind Java's "Write Once, Run Anywhere" philosophy. The JVM takes the platform-independent bytecode from your compiled code and translates it into code that your computer can understand and execute.

# Getting Started

#### Prerequisites

* Java 8 or higher
* Any Java IDE (like Eclipse, IntelliJ IDEA, or VS Code)
* Command-line access

#### Installation & Setup

1. Clone or download the project
'git clone <repository-url>'
'cd campus-course-records-manager'

2. Compile the project
'javac -d . src/main/java/com/ccrm/*.java src/main/java/com/ccrm/**/*.java'

3. Run the application
'java com.ccrm.CampusCourseRecordsManager'

# Setting up the Project in Eclipse IDE

1. Launch Eclipse and select File > Import...
2. Choose Git > Projects from Git (with smart import) and click Next.
3. Select Clone URI and paste the project's repository URL. Click Next.
4. Choose the main branch and click Next.
5. Set the local directory for the project and click Next.
6. Eclipse will automatically recognize it as a Java project. Click Finish.

Now that the project is in your workspace, you can run it by right-clicking on 'CampusCourseRecordsManager.java' in the Package Explorer and selecting Run As > Java Application.

# Project Requirements Mapping

Here's a quick look at where you can find each key concept implemented in the code:

* Encapsulation: You'll find private fields with public getters and setters in files like 'model/Person.java' and 'model/Student.java', ensuring controlled data access.
* Inheritance: The abstract 'Person' class is the base for 'Student' and 'Instructor', allowing them to share common properties and behaviors.
* Abstraction: The 'Person' class defines abstract methods like 'getRole()' that its subclasses must implement, setting a clear contract.
* Polymorphism: A 'Person' reference can hold either a 'Student' or an 'Instructor' object, showcasing flexible code design.
* Singleton Pattern: The 'DataStore' class ensures that only one instance exists throughout the application to manage all data centrally.
* Builder Pattern: The 'CourseBuilder' and 'TranscriptBuilder' are used for building complex objects step-by-step.
* Custom Exceptions: We use our own exceptions like 'MaxCreditLimitExceededException' for more specific error handling.
* NIO.2: Modern file operations using the 'Path' and 'Files' APIs are demonstrated in 'utils/FileUtils.java' and 'utils/BackupUtils.java'.
* Streams: The Streams API is used for declarative data processing and filtering in files like 'core/DataStore.java' and 'services/StudentService.java'.
* Date/Time API: 'LocalDate' is used to handle dates without time zones in 'model/Student.java' and 'model/Enrollment.java'.
* Enums: Our enums like 'Semester.java' and 'Grade.java' provide type-safe constants with associated data and methods.
* Recursion: You can see recursive directory traversal and operations in the 'utils/BackupUtils.java' file.

  SCREENSHOT OF THE PROGRAM:
  Main menu of the program
  <img width="515" height="245" alt="image" src="https://github.com/user-attachments/assets/c345bd70-d2fc-4332-a2dc-4843f0dbceae" />
  student management
  <img width="500" height="230" alt="image" src="https://github.com/user-attachments/assets/0de16b13-79e4-4b84-9782-9c49ffd13444" />
  add new student
  <img width="406" height="189" alt="image" src="https://github.com/user-attachments/assets/f3fddd9d-b347-4d72-9602-ff6de23be83c" />
  view all students
  <img width="1048" height="69" alt="image" src="https://github.com/user-attachments/assets/46404ec0-377c-484a-9649-853aab5370b9" />
  view student details
  <img width="1074" height="161" alt="image" src="https://github.com/user-attachments/assets/63756bda-9d92-47be-88d6-aa723c43f89a" />
  update student
  <img width="1227" height="163" alt="image" src="https://github.com/user-attachments/assets/1ed45b9b-ebf4-4b2c-be80-705b8839b449" />
  deactivate student
  <img width="466" height="79" alt="image" src="https://github.com/user-attachments/assets/9618d7ac-e58b-43d7-a969-5006440f3080" />
  generate student transcript
  <img width="413" height="400" alt="image" src="https://github.com/user-attachments/assets/58bd1b0f-98ee-4261-bc73-6cec0770c09f" />
  course management
  <img width="439" height="212" alt="image" src="https://github.com/user-attachments/assets/cd041e43-036a-4fa2-863c-01c20c2cf369" />
  add new course
  <img width="693" height="581" alt="image" src="https://github.com/user-attachments/assets/e9d92ddc-ef53-428a-bb98-fbca5c8364d4" />
  view all courses
  <img width="1289" height="97" alt="image" src="https://github.com/user-attachments/assets/842c3e10-5f03-411d-87e6-2d65b3b40517" />
  course details
  <img width="1305" height="89" alt="image" src="https://github.com/user-attachments/assets/e73e5ba4-ae7c-4c59-b57c-9adeb47cb898" />
  update course
  <img width="1362" height="171" alt="image" src="https://github.com/user-attachments/assets/f7dc46c9-ba78-4009-9a75-733e67817da7" />
  deactivate course
  <img width="562" height="79" alt="image" src="https://github.com/user-attachments/assets/bde71147-6638-417c-ad5d-7473815a213f" />
  search courses by department
  <img width="1197" height="368" alt="image" src="https://github.com/user-attachments/assets/2c01007c-7a2c-4ec8-a58e-c54ed404772f" />
  search courses by semester
  <img width="1210" height="215" alt="image" src="https://github.com/user-attachments/assets/321752bf-a5ed-4193-bf83-f7bea62dc97d" />
  enrollment and grading
  <img width="378" height="190" alt="image" src="https://github.com/user-attachments/assets/b9e5799d-664f-4e77-afe0-006b162a604c" />
  enroll student in course
  <img width="778" height="112" alt="image" src="https://github.com/user-attachments/assets/b052da12-79c2-44fb-b4d9-b7b3d07ba50b" />
  view student enrollments
  <img width="534" height="113" alt="image" src="https://github.com/user-attachments/assets/fd919860-1d42-493c-9e5a-50a9a0a5ed60" />
  calculate student GPA
  <img width="435" height="150" alt="image" src="https://github.com/user-attachments/assets/8a16b7b4-5470-467f-8db3-3719b2109d56" />
  file operations
  <img width="418" height="225" alt="image" src="https://github.com/user-attachments/assets/0cb35ba7-8be0-43ba-b16d-8738bc47e4c7" />
  export students to CSV
  <img width="496" height="53" alt="image" src="https://github.com/user-attachments/assets/d9f966d6-febe-466c-b34b-84d920314e75" />
  export courses to CSV
  <img width="585" height="51" alt="image" src="https://github.com/user-attachments/assets/30c474d9-1af9-4e15-b159-25c8ea62a83c" />
  export enrollments to CSV
  <img width="563" height="50" alt="image" src="https://github.com/user-attachments/assets/ebc2013c-6afc-49cb-b793-407d43e70cd9" />
  system reports
  <img width="396" height="142" alt="image" src="https://github.com/user-attachments/assets/de227bec-426e-4d99-a6ec-f486158619b2" />
  system statics
  <img width="454" height="186" alt="image" src="https://github.com/user-attachments/assets/dd1300da-5385-48c4-a54d-a911e5f2e210" />
  GPA distribution reports
  <img width="575" height="100" alt="image" src="https://github.com/user-attachments/assets/89583d94-00b4-4812-9b05-fc3bb64462f9" />
  course enrollment statistics
  <img width="564" height="96" alt="image" src="https://github.com/user-attachments/assets/c36ceac6-d406-4442-9f7b-2dad07895be0" />
  department statistics
  <img width="504" height="92" alt="image" src="https://github.com/user-attachments/assets/54d44eac-46aa-4b34-abd5-a82d74946674" />
  backup operations
  <img width="359" height="184" alt="image" src="https://github.com/user-attachments/assets/825b8b4d-ad46-432e-ae8f-a9e933bda203" />
  create backup
  <img width="747" height="59" alt="image" src="https://github.com/user-attachments/assets/10420d15-4b8a-434a-9f5c-f814dcab1c05" />
  list backup files
  <img width="657" height="151" alt="image" src="https://github.com/user-attachments/assets/3c652cc1-790f-49c1-b943-c77b9a5dc5c5" />
  calculate backup size information
  <img width="518" height="100" alt="image" src="https://github.com/user-attachments/assets/0a5c2ba5-cb6c-44ae-a48c-a019c3e4e66d" />
  cleanup old backups
  <img width="670" height="78" alt="image" src="https://github.com/user-attachments/assets/a53368d4-7d48-42ec-8844-6a68564126a7" />



































  

  

# Enabling Assertions

To enable assertions, you just need to use the '-ea' flag when you run the Java application from the command line. This is super helpful for debugging and for internal consistency checks.

Sample Command:

'java -ea com.ccrm.CampusCourseRecordsManager'
