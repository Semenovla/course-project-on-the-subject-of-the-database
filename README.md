1. Introduction
This task involves the development of conceptual and logical models of a database intended for information support (service) of a hypothetical business process.
2 basis for development
Coursework in the discipline “Databases” is provided for by the curriculum of the training direction 03/09/04 “Software Engineering”.
3 purpose and development goals
In accordance with the “Regulations on course design” of USATU, the goal of course design is to develop experience in comprehensively solving specific problems of professional activity, in this case, the tasks of developing conceptual and logical models of an information system database. This general goal includes teaching, educational, and developmental goals.
Learning Objectives:
 consolidation, deepening, expansion and systematization of knowledge obtained from the study of this and other disciplines that preceded it,
consolidating the skills to apply this knowledge to solve typical problems;
 formation of skills to work with software tools;
development of skills in working with specialized literature and other information sources;
 formation of skills to formulate logically substantiated conclusions, proposals and recommendations based on the results of the work performed;
developing the ability to competently write a report from a philological and psychological point of view and prepare a presentation of the project (work) being defended;
developing the ability to speak in front of an audience with a report when defending a project (work), competently answer questions, conduct a professional discussion, and convince opponents of the correctness of the decisions made.
Educational goals designed to educate students:
confidence in your creative and communication capabilities;
independence, responsibility for the engineering work performed;
skills of systematic, regular work to solve a given problem.
Developmental goals that help students develop:
systemic thinking;
intellectual creative potential;
professional written and oral speech.
4 requirements for the development object
This task involves the development of conceptual and logical models of a database intended for information support (service)
4.1 Business process served by a database
The database designed within the framework of this assignment is intended for information support (service) of the business process “University. Cultural department."
4.1.1 Brief description of the business process. The process of organizing and holding cultural events at the university.
4.1.2 List of business process functions. A business process is usually divided into subprocesses, procedures, and functions. In this course work, a business process consists of functions. For the business process “University. Cultural Department" requires information support for the following functions:
1) “Preparation of events” The process of preparing cultural events.
2) “Financial support for events” The process of financing cultural events.
3) “Holding events” The process of holding cultural events.
4.2 Information for servicing business process functions
The database must satisfy the information needs of the above business process functions. To do this, it must provide for storing information related to the basic entities (participants) of these functions. Listed below are
4.2.1 Function “Preparation of events”. The information structure of this function contains the following aggregates:
Unit "Event". Information about the preparation of a cultural event. The structure of the unit is as follows:
● “Event Registrar” – attribute. Numbering without duplicates.
● “Event name” – attribute.
● “Culturally Responsible Code” – attribute. A culturally responsible employee is an employee. An employee is a person. Persons are encoded without duplicates.
● “Name of culturally responsible person” – attribute.
● “Position code” – attribute. The employee has a position. Coding without duplicates.
● “Job title” – attribute.
● “Event type code” – attribute. Coding without duplicates.
● “Name of event type” – attribute.
● “Date” – attribute.
● “Place code” – attribute. Coding without duplicates.
● “Place name” – attribute.
► “Performance” is a nested unit. Several applications are being received to participate in the event.
"Performance" unit. Several applications are being received to participate in the event. The structure of the unit is as follows:
● “Application registration number” – attribute. Numbering without duplicates within the event.
● “Speech title” – attribute.
● “Application date” – attribute.
● “Performance type code” – attribute. Coding without duplicates.
● “Name of type of performance” – attribute.
► “Participant of the speech” is a nested aggregate.
Unit “Participant of the performance”. The structure of the unit is as follows:
● “Participant code” – attribute. A participant is a student. A student is a person. Persons are encoded without duplicates.
● “Participant’s full name” – attribute.
● “Group code” – attribute. Coding without duplicates in pwithin the specialty.
● “Year of group organization” – attribute.
● “Specialty code” – attribute. Coding without duplicates.
● “Name of specialty” – attribute.
● “Participant role” – attribute. May be missing.
4.2.2 Function “Financial support for events”. The information structure of this function contains the following aggregates:
Unit "Event". Information about the financing of cultural events. The structure of the unit is as follows:
● “Event Registrar” – attribute.
● “Date” – attribute.
● “Accountant code” – attribute. An accountant is an employee. An employee is a person. Persons are encoded without duplicates.
● “Accountant's full name” – attribute.
● “Position code” – attribute. The employee has a position. Coding without duplicates.
● “Job title” – attribute.
► “Receipt of funds” is a nested aggregate. An event may receive funds from several sources.
► “Event expenses” is a nested aggregate. There may be several expenses incurred for an event.
Unit “Receipt of funds”. An event may receive funds from several sources. The structure of the unit is as follows:
● “Receipt registration number” – attribute. Numbering without duplicates.
● “Receipt date” – attribute.
● “Receipt type code” – attribute. Coding without duplicates.
● “Name of receipt type” – attribute.
● “Receipt amount” – attribute.
● “Admission sponsor code” – attribute. The receipt may be from a sponsor. If from the university budget, then it is missing along with other information about the sponsor.
● “Name of sponsor of receipt” – attribute.
● “Sponsor condition” – attribute. May not be available upon receipt from the sponsor.
“Event expenses” unit. There may be several expenses incurred for an event. The structure of the unit is as follows:
● “Flow meter” – attribute. Numbering without duplicates.
● “Date of consumption” – attribute.
● “Expense type code” – attribute. Coding without duplicates.
● “Name of expense type” – attribute.
● “Expense amount” – attribute.
● “Financial responsible code” – attribute. The person financially responsible for the expense is the employee. An employee is a person. Persons are encoded without duplicates.
● “Full name of the person responsible” – attribute.
● “Position code” – attribute. The employee has a position. Coding without duplicates.
● “Job title” – attribute.
4.2.3 Function “Carrying out events”. The information structure of this function contains the following aggregates:
Unit "Event". Information about holding a cultural event. The structure of the unit is as follows:
● “Event Registrar” – attribute. Numbering without duplicates.
● “Event name” – attribute.
► “Event presenter” is a nested aggregate. The event can be hosted by several presenters.
► “Member of the competition committee” is a nested aggregate. The commission has several members.
► “Performance” is a nested unit. The event includes several performances.
“Event presenter” unit. The event can be hosted by several presenters. The structure of the unit is as follows:
● “Leader code” – attribute.
● “Full name of presenter” – attribute.
● “Leader position code” – attribute. The employee has a position. Coding without duplicates.
● “Leader’s position title” – attribute.
● “Leader role” – attribute. At this event.
Unit “Member of the competition commission”. The commission has several members. The structure of the unit is as follows:
● “Commission member code” – attribute. A member of the commission is an employee. An employee is a person. Persons are encoded without duplicates.
● “Full name of commission member” – attribute.
● “Commission member position code” – attribute. The employee has a position. Coding without duplicates.
● “Position name of a commission member” – attribute.
● “Role of a committee member” – attribute.
"Performance" unit. The event includes several performances. The structure of the unit is as follows:
● “Application registration number” – attribute. Numbering without duplicates within the event.
● “Speech title” – attribute.
● “Reward code” – attribute. Coding without duplicates. May be missing with other award information.
● “Award name” – attribute.
► “Evaluation of performance by nomination” is a nested aggregate. The performance is judged in several categories.
Unit “Evaluation of performance by nomination”. The performance is judged in several categories. The structure of the unit is as follows:
● “Nomination code” – attribute. Coding without duplicates.
● “Name of nomination” – attribute.
● “Score by nomination” – attribute.
5 Stages and milestones of development
Completion of the course work is designed for 10 academic weeks and includes the following stages and phases:
Stage, stage Education. a week
1. Obtaining technical specifications 4
2. Model development:
a) development of local hierarchical models 5
c) development of local ER models 7
d) development of a global ER model 8
e) development of a relational model 9
f) development of display models 10
3. Development and debugging of program code 11
4. Registration of results and preparation of presentation 12
5. Submission of coursework 13

6 Documentation requirements
In the process of completing coursework, it is necessary to developb the following documents.
Document designation Document title
2023-2.5.BD.RGR.PRO-331.21130104.TZ Technical specifications
2023-2.5.BD.RGR.PRO-331.21130104.LI Local hierarchical model
2023-2.5.BD.RGR.PRO-331.21130104.LP Local intermediate model
2023-2.5.BD.RGR.PRO-331.21130104.LN Local normalized model
2023-2.5.BD.RGR.PRO-331.21130104.GS Global “entity-relationship” model
2023-2.5.BD.RGR.PRO-331.21130104.GR Global relational model
2023-2.5.BD.RGR.PRO-331.21130104.LO Local display model
2023-2.5.BD.RGR.PRO-331.21130104.TP Program text
2023-2.5.BD.RGR.PRO-331.21130104.PZ Explanatory note
2023-2.5.BD.RGR.PRO-331.21130104.VP Video presentation
2023-2.5.BD.RGR.PRO-331.21130104.VD List of documents
Graphic documents are executed in the Microsoft Office Visio graphic editor, version 2007 and higher (vdx file format), and text documents are executed in the Microsoft Office Word editor, version 2007 and higher (docx file format). Documents are placed in the document album. Electronic versions of all documents are placed in an album on a CD. Paper versions of all documents, except for the explanatory note and video presentation, are also placed in the album.
7 Control and acceptance procedure
Coursework includes:
1) step-by-step monitoring of progress with credit for each intermediate stage;
2) final defense of the work with a final grade.
The transition to the next stage is possible only after the current stage has been completed.
Based on the results of the completed development stages, a 7-minute video presentation is prepared, on the basis of which the defense takes place.
Criteria for evaluation:
excellent – ​​all stages were completed in full and on time, the protection is good;
