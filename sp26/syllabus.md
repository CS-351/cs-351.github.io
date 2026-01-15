## [<< back](./index.html)

# CAS CS 351 -  Course Syllabus Fall 2025

**Instructors**: Anna Arpaci-Dusseau  
**Teaching Fellows**: Matias Ou, Naima Abrar Shami

**Lectures**: Mon/Wed 2:30pm-3:45pm, 4:00-5:15
**Discussions**: Wed 9:05am - 2:15pm, 7 sections; multiple locations; check MyBU Student

**Instructor Office Hours**: TBD  
**TF Office Hours**: Tuesday 11:30am - 1pm, Thursday 2pm-4pm (CDS 1001), Friday 1-3pm (CDS 1001) and 4-5:30pm (CDS 364)

**IMPORTANT**: Refrain from using email to reach the course staff. **_Use Piazza for all class communication_**, including to privately contact the instructors or TFs.


## 1. Overview
_“You know your **distributed systems theory**: You know about **logical time**,
**snapshots**, **stability**, **message ordering**, but also acid and multi-level **transactions**. 
You have heard about **the FLP impossibility argument**. You know why **failure detectors** can solve it. 
You have at least once tried to understand Paxos by **reading the original paper**._

_You have a good sense for **distributed systems practice**: 
you can reason about **churn** and locality in DHTs. 
You intuitively know when to apply **ordered communication** and when to use transactions. 
You can reason about **data consistency** in a system where hundreds of nodes are geographically distributed […].
You have a solid intuition about the impact of design decisions on the ability to achieve data consistency, 
and you are not scared by the idea of building systems based on **eventually consistent** data.”_

The above is an excerpt from the blog post [Job Opening for a Senior Research Engineer](https://www.allthingsdistributed.com/2007/07/job_opening_for_a_senior_resea.html)
by Werner Vogels, CTO of Amazon. CS 351 teaches you the fundamental theory and practice of distributed systems 
and will be your first step towards becoming a successful applicant for such a position.

### 1.1 Course topics
In CS 351, you will learn fundamental concepts of distributed systems and distributed computing (logical clocks, causal order, snapshots, consensus, atomic commit), communication and synchronization primitives, concurrency control, task and data parallelism, data consistency, replication, and fault tolerance. 
Below is a detailed list of topics:

- Computation and communication primitives (Threads, Remote Procedure Call)
- Concurrency Control (Mutexes, Optimistic vs Pessimistic control)
- Task Parallelism, Data Parallelism, Pipeline Parallelism
- Time in Distributed Systems (Causal Order, Lamport Clocks, Vector Clocks)
- Distributed Snapshots (Chandy-Lamport protocol)
- Replication (Primary-Backup Replication, Chain Replication, Replicated State Machines)
- Distributed Consensus (Raft)
- Data Consistency (Strong vs Weak consistency, Linearizability, Sequential Consistency, Causal Consistency, Eventual consistency)
- Distributed Transactions (ACID, Serializability, Two-Phase Commit)
- Sharding and Consistent Hashing
- Distributed Shared Memory
- TLA+
- Golang (Go runtime, Go routines, Go channels, etc.)

### 1.2 Prerequisites
**CS 210 or equivalent (will be enforced!)**

Students must also have good programming skills (C/Java/Python) and basic knowledge of data structures and algorithms.

## 2. Instructional Format and Course Materials

### 2.1 Courseware
- We will use [the course website](https://cs-351.github.io/fall25/index.html ) to maintain an up-to-date class schedule.
- We will use [Piazza](https://piazza.com/bu/fall2025/cascs351 ) for announcements, questions, discussions, and all other communication.
- We will use [Github Classroom](https://classroom.github.com/) for the discussions and assignments.
- We will use [Gradescope](https://www.gradescope.com/courses/1111176) for assignment submissions.

### 2.2 Lectures
Lectures will be held during the assigned time slots. 
[The detailed lecture schedule](./lectures.html) provides the topic and assigned readings for each lecture. 
**You are expected to complete the readings before the day of the lecture** and actively participate in class discussions. 
Lecture slides will be made available on Piazza prior to the lectures or shortly after.

#### Lecture material and readings
The best material to study from are the lecture and lab slides, as well as the notes you take in class. 
While the course does not have a required textbook, the following seminal book covers many of the lecture topics, 
and we highly recommend using it to supplement your learning:

- [Distributed Systems](https://www.distributed-systems.net/index.php/books/ds4/) 4th Edition (by Maarten van Steen, Andrew S. Tanenbaum). You can request a free pdf version of the book in the provided link.

Lectures may have pointers to readings, which you should complete prior to the lecture. In the [lecture schedule](./lectures.html), 
**MSAT** refers to the textbook above.

If you are looking for additional resources, the following are also excellent books:

- Distributed Systems: Concepts and Design (by G. Coulouris, J. Dollimore, T. Kindberg, Gordon Blair).
- Designing Data-Intensive Applications: The Big Ideas Behind Reliable, Scalable, and Maintainable Systems (by Martin Kleppmann).

To further understand the practical challenges and impact of distributed systems, we will also assign additional readings and discuss the following distributed systems from industry:

- [Raft](https://www.usenix.org/conference/atc14/technical-sessions/presentation/ongaro)
- [MapReduce](https://dl.acm.org/doi/10.1145/1327452.1327492)
- [The Google file system](https://dl.acm.org/doi/10.1145/945445.945450)
- [Dynamo](https://dl.acm.org/doi/10.1145/1323293.1294281)
- [Spanner](https://www.usenix.org/conference/osdi12/technical-sessions/presentation/corbett)

### 2.3 Discussions
[Discussions](./discussions.html) are a core component of the course and **discussion attendance is mandatory**. 
The Teaching Fellows will lead the discussion sessions and present material on programming tools and answer questions (or provide clarifications) 
regarding the assignments. The Teaching Fellows will post information to Piazza as necessary. 

**You must attend the discussion section you have registered for**. Instructors and Teaching Fellows do not have access to the registration system and cannot help you switch discussion sections.

### 2.4 Programming Language and Software Tools
All programming assignments will be in [Golang](https://cacm.acm.org/research/the-go-programming-language-and-environment/), 
and we recommend using [VSCode](https://code.visualstudio.com/) for development. 

_No prior knowledge of Go is required to succeed in the course_; the lab sections will gradually introduce you to the language.
For code management, we will be using Git. You are expected to regularly push your code to your Github repository. 
We will provide instructions on how to set up your programming environment on Piazza. Make sure your code is well-documented and always use meaningful commit messages. 
We will be using your Git commit history to track your progress and give you feedback.

### 2.5 Office Hours
We will be holding office hours every day to further discuss lecture material (with instructors) and hands-on assignments (with instructors or TAs).
We may also have extra OHs before some assignment deadlines. Instructors and TFs will be giving you advice on good coding practices but they are not there to debug your code. 
_Debugging is your responsibility_.

## 3. Assignments, Exams, and Grading Criteria

### 3.1 Grading Scheme

The course includes reading assignments, in-lecture quizzes, programming assignments, a midterm exam, and a final exam. 
Your final grade will be determined as follows:

- Reading assignments + Git commit history: 5%
- Midterm exam: 20%
- Quizzes: 20%
- Final exam: 30%
- Programming assignments: 25% (weights: A0: 2%,  A1: 3%, A2: 5%, A3: 8%, A4: 7%)

### 3.2 Midterm and Final Exams

The midterm will take place during lecture time on **March 4th** and the final exam is to be announced.

**These dates are not flexible**. Please plan your work and travel plans accordingly.

Both exams are open-book, however, the use of electronic devices during the exams is strictly prohibited. 
In the midterm and final, you are only allowed to bring hard copies of the lecture and lab slides, your notes, 
and any papers we have covered in class.

### 3.3 In-class quizzes

We will have three in-class quizzes on **2/11, 3/25, and 4/15**. **These dates are not flexible**. Please plan your work and travel plans accordingly.

In-class quizzes will be administered on paper or on Gradescope. More information about quiz conduct and grading will be provided on Piazza.

### 3.4 Programming Assignments

We will release five programming assignments during the semester:

| Assignment | Release Date | Due Date | Late Due Date | Duration | 
|----------|----------|----------|----------|----------|
| A0: Go Primer        |  1/21    |  1/30  | |  8 days  |
| A1: Weather Service  |  2/2   |  2/13  |  |  12 days |
| A2: Futures          |  2/16   |  2/27 | | 12 days  |
| A3: Raft A           |  3/2  |  3/20 |  | 12 days |
| A4: Raft B           |  3/2  |  4/3 | | 1 month |
| A5: 3PC or Multicast (TBD)              |  4/6 |  4/30 | - | 16 days |


**All assignment deadlines will be on Friday at 11.59pm (midnight)**. 
After each deadline, you will have 1 more week (7 days) to _submit late with a 30% penalty_. 
Submissions will not be accepted after this extended period.

## 4. Class and University Policies

### 4.1 Attendance
We will not be taking attendance in lectures and labs. All course material will be posted on Piazza. Ultimately, you are responsible for your own learning and for keeping up with the homework.
Lectures and labs will not be recorded. If you are unable to attend a lecture or a lab discussion, please come to our OHs to catch up.

### 4.2 Academic Conduct
Academic standards and the code of academic conduct are taken very seriously at our university. 
Please take the time to review the CAS Academic Conduct Code: http://www.bu.edu/academics/resources/academic-conduct-code/ and the GRS Academic Conduct Code: http://www.bu.edu/cas/students/graduate/grs-forms-policies-procedures/ academic-discipline-procedures/. 
Please review the sections regarding plagiarism and cheating carefully. Copies of the CAS Academic Conduct Code are also available in room CAS 105. 
A student suspected to violate this code will be reported to the Academic Conduct Committee, and if found culpable, the student will receive a grade of "F" for the course

All assignments must be completed individually, unless instructed otherwise. 
Discussions with fellow students via Piazza or in-person are encouraged, but presenting the work of another person as your own is expressly forbidden. 
This includes “borrowing”, “stealing”, copying programs/solutions or parts of them from others. 
**We will be using automated plagiarism checkers**. If your submission has more than 50% similarity with another submission or a publicly available solution we have crawled from the web, 
you will automatically receive 0 points. **Cheating will not be tolerated under any circumstances**.

Any resources, including material from other students (current or past), that are used, beyond the text or that provided by the TF or professor must be clearly acknowledged and attributed. 
Using such material may result in a lower grade. However, if such material is used and not acknowledged and attributed, it will automatically be considered as possible academic misconduct.

### 4.3 On the use of GenAI tools

The use of AI tools, such as chatGPT or TerrierGPT, to generate written text or code for your assignments in this course is forbidden. 
**Uploading any course content (assignments, papers, slides) to a Generative AI tool will be treated as a case of possible academic misconduct**. 
However, you are allowed to use AI tools for enhancing your understanding of core concepts, brainstorming, and identifying external knowledge sources. 

Beware that using AI-generated content in your assignments and projects could negatively affect your grade, as it may contain subtle errors, omissions, bugs, and misinterpretations. Any use of AI software must be explicitly disclosed in your submissions, including the prompts you used.

## 5. Accommodations
If you are a student with a disability or believe you might have a disability that requires accommodations, please contact the Office for Disability Services (ODS) at (617) 353-3658 or access@bu.edu to coordinate any reasonable accommodation requests. ODS is located at 25 Buick Street on the 3rd floor.
