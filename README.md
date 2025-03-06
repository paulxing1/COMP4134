java cProject in Advanced Algorithms and Data Structures COMP4134 UNNC

Overview For this project, you are tasked with solving a real-world transportation problem. Formally speaking, it is called the pickup and delivery problem with time windows (PDPTW). The pickup and delivery problem (PDP) is a type of vehicle routing problem in which customers are paired together, and a pair must be serviced by the same vehicle, see https://developers.google.com/optimization/routing/pickup_delivery for example. In other words, a load must be collected from one location and delivered to another location by a single vehicle. Clearly, there are also ordering or precedence constraints to ensure that the collection site is visited before the delivery site. If there are time windows during which the customers must be visited, then the problem is known as the PDPTW. This problem commonly arises in real-world logistics, and solution methodologies have significant practical applications.

While planning the routes, there are some driver break regulations that have to be met, which include drivers' hours rules and working time rules. To reduce complexity, we will focus on the rules highlighted in red circles, which pertain to the daily transportation problem. The objective is to decrease the total duty time necessary for the delivery of all orders.

The two regulations are briefly introduced below; detailed information can be found in Table 1 (see https://assets.publishing.service.gov.uk/media/5e14b5b040f0b65dbed713a0/simplified-guidance-eudrivers-hours-working-time-rules.pdf and Table 2). Regarding Regulation (EC) No 561/2006, the following constraints should be met: • The maximum daily driving time is 9 hours. • Driver breaks could be one of the following: (a) For every 4.5 hours of driving, drivers must take a break of at least 45 minutes. This break starts a new 4.5-hour driving period. (b) For every 4.5 hours of driving, drivers can take either one 45-minute break or two smaller breaks, one of at least 15 minutes followed by another of at least 30 minutes. Another regulation is Directive 2002/15/EC, which is a legislative act concerning the working time for mobile workers engaged in road transport activities. It sets out the maximum limits on working time, including driving time, other work-related activities, and on-call time. The following constraints should be met: • Drivers cannot work more than 6 hours without a break; a break should be at least 15 minutes long. • Drivers need a 30-minute break if they work between 6 to 9 hours in total. 2 Table 1 A summary of the EU drivers’ hours rules and sector specific working time rules

Table 2 Summarised daily allowed drive time, duty time and route duration

Deadline and Late penalty Deadline is 6pm Monday the 9th of December, for each day the coursework is late, a penalty of 10% will be deducted. Plagiarism is not allowed, and your source code and documentation will be examined for similarities. Please note that this is individual work, not a group project. You are encouraged to conduct individual research and free to implement algorithms that have already been published, but copying others’ work is strictly forbidden. (Please consult the academic misconduct policy for further details: https://www.nottingham.ac.uk/studentservices/servicedetails/appeals-complaints-andconduct/academic-misconduct.aspx)

Submission instructions To submit your code and report for this module, please use the provided link on the Moodle page. Your algorithm should be implemented in Java, and your report, which is limited to 2000 words, must be submitted in PDF format. Please refer to the “Grading Criteria” section below, which lists the requirements. The submission link will be active before the deadline. Please note that submissions sent via email will not be accepted. For comprehensive guidelines on the submission process, please consult the “Submission” section below. Submission Given that this is a Master's level project, it is designed to emphasize independent study and research. However, certain algorithms and data structures relevant to the project will be introduced in the course module COMP4133. Proficiency in Java is required for the successful completion of this project.

The necessary files for this assignment are available for download from Moodle. These include: • Input.json: An example file that you will read as input. • Output.txt: A sample output file that corresponds to the Input.json input.

Your Java code should fulfill the following requirements:

Read the content of Input.json.
You are required to devise your own algorithm and apply it to solve the given problem. Implementing an existing algorithm from the literature is fine, but please cite it in your report. You may select from various algorithmic approaches, including but not limited to dynamic programming, linear programming, and heuristics. Your implementation will be submitted for grading.
Print the solution follow the expected ‘Output.txt’.
For instance, given the content of 'Input.json' provided: Please refer to the video recording on the module page for this module for a detailed explanation of the JSON content. 4

The expected 'Output' should look like this:

Which appears as follows in the text file:

VehicleName,JobId,JourneyTime,ArrivalTime,WaitTime,DelayTime,ServiceTime,DepartureTime,Break1Ti me,Break1Duration,Break2Time,Break2Duration 1,Vehicle 1 start,0h0m,08:00,0h0m,0h0m,0h0m,8h0m,,,, 1,C-0,0h0m,08:00,0h0m,0h0m,0h0m,8h0m,,,, 1,C-1,4h0m,12:00,0h0m,0h0m,0h0m,12h0m,,,, 5

1,D-0,0h0m,12:00,0h0m,0h0m,2h0m,14h0m,14:00,0h15m,14:45,0h30m 1,D-1,2h0m,16:45,0h0m,0h0m,0h0m,16h45m,,,, 1,Vehicle 1 end,0h30m,17:15,0h0m,0h0m,0h0m,17h15m,,,,

Grading Criteria Criteria of code 50% Full mark Comment Is the output correct? 20% The correct answer will receive full marks. Marks may be deducted for the following reasons: partially correct answers with minor mistakes, or correct output accompanied by other issues. This will be tested using a new dataset, which is not provided by the module. For programs involving randomness, ensure that you use your student ID as the seed. How is the time complexity of the program? 10% For those who provide the correct answer, their run time will be recorded. Those whose run time falls into the first quantile will receive full marks. Those in the second quantile will receive 7.5% of the total marks, the third quantile 5%, and the last quantile 2.5%. How is the solution quality of the program? 10% Please indicate the duration required for the solution to complete all the service requests (i.e. pickup and delivery pairs) within run time of 30 seconds. For those whose solution is better than the benchmark solution, the ranking will be determined by the speed of completion; the quicker the completion, the higher the ranking. Participants whose solutions fall within the top 25% will be awarded full points. Those in the second 25% bracket will earn 75% of the total score, the third 25% will get 50%, and the bottom 25% will receive 25%. Well formatted code 5% Is the program well formatted (following Java naming conventions, high readablity, 6

appropriate error handling, adhere to Object-Oriented Programming paradigm etc.) Appropriate comments 5% Does the program contain appropriate comments? Criteria of report 50% Well-written literature review 10% In the literature review, is the literature sufficient, up-to-date, well-organised, and does it follow proper logical flow? The report should be confined to a maximum of 2000 words, excluding literature and pseudo code. Evaluation of the Chosen Algorithm, Data structure and Methodology 15% Provide a clear rationale for the algorithm selected and the approach taken to solve the problem. Indicate whether the algorithm is entirely of your own design or if it is an implementation of an existing algorithm from the literature. Discuss the innovative aspects or novelties that you have introduced to the project. Provide clear and effective documentation of your algorithm 10% In your report, ensure that you provide a clear and concise explanation of your algorithm. Utilise clear instructions, supported by pseudocode, diagrams, and other visual aids as necessary to enhance understanding. Evaluating solution quality and output validation accuracy 10% Justify the solution’s quality and confirm that the given output is correct. Report the result clearly 5% Report the results clearly, for example, by using visuals, plots, and statistics such as the mean and standard deviation of a number of runs.

Additional Credit: We are primarily evaluating compliance with the rules for individual days. However, an extra 10% bonus (up to maximum of 100%) will be awarded if rule sets beyond those highlighted in the red squares are taken into account.

Definitions Standard input 7

System.in, means that the stream from which input to the program is taken. Typically this is the keyboard, but it can be specified that input is to come from a serial port or a disk file. Standard output System.out, means that the stream to which output from the program is sent. Typically this is a display, but it can be redirected to a serial port or a file.

Submission You must submit a single Java source code file containing all your code for this coursework. This file must be called AADS.java and must not require any other files outside of the standard Java packages which are always available. The file must compile and execute without warnings or errors using the command. Compile: javac -encoding UTF-8 -sourcepath . AADS.java Execute: java -Dfile.encoding=UTF-8 -XX:+UseSerialGC -Xss64m -Xms1920m -Xmx1920m AADS Output.txt Your program SHOULD send its output to standard output (by executing above command, it will produce Output.txt in the same directory as AADS.java and Input.json, so no FileWriter is required).

Technical Notes This part contains important technical information and it is important that you read and understand all the information below. You program MAY have multiple classes if you wish, but only in one java file. And only the class with your main method SHOULD be marked as public. Your program MUST read its input from standard input. If your program exits with a non-zero exit code, it will be judged as a run-error. Program submitted will be run inside a sandbox. The sandbox will allocate 2GB of memory for your program. Your entire program, including its runtime environment, must execute within this memory limit. For Java, the runtime environment includes the interpreter (JVM). We suggest that you do not use package statements (that is, we suggest that your solution reside in the “default package”). Please use JDK versions later than 7.

Possible results A submission can have the following results: 8

CORRECT The submission passed all tests: you solved this problem! 0% will be given to errors listed below: COMPILER-ERROR There was an error when compiling your program. Note that when compilation takes more than 30 seconds, it is aborted and this counts as a compilation error. TIMELIMIT Your program took longer than the maximum allowed time for this problem, 5 seconds. Therefore it has been aborted. This might indicate that your program hangs in a loop or that your solution is not efficient enough. RUN-ERROR There was an error during the execution of your program. This can have a lot of different causes like division by zero, incorrectly addressing memory (e.g., by indexing arrays out of bounds), trying to use more memory than the limit, reading or writing to files, etc. Also check that your program exits with exit code 0! NO-OUTPUT Your program did not generate any output. Check that you write to standard out. OUTPUT-LIMIT Your program generated more output than the allowed limit. The solution is considered incorrect. WRONG-ANSWER The output of your program was incorrect. This can happen simply because your solution is not correct, but remember that your output must comply exactly with the specifications of the judges. See testing below for more details. The judges may have prepared multiple test files for each problem.

Some hints for you to improve your solution Scenario 1 a. The driver takes a break of 30 minutes after working for 6 hours. Then, the driver resumes driving for another 30 minutes, followed by another break of 30 minutes, because of the 4.5 hours of driving time accumulated.

Scenario 1 a b. However, this driver break assignment can be improved by allocating a 45- minute break when the duty time has been accumulated to 6 hours rather than allocating an additional 30-minute break when reaching 4.5 hours of driving because the driving hours have been reset by the 45-minutes break. 9

Scenario 1 b

Scenario 2 a. This scenario is similar to the previous one, but the driver in the previous scenario completes his journey after 2.5 hours of driving after the first break. In this case, however, the driver continues to drive for 4 hours and 40 minutes after the first break.

Scenario 2 a b. Allocating 45 minutes to reset the driving break is no longer a good idea in this scenario because another break will be triggered due to reaching 4.5 hours driving time. As a result, the journey will take 12 hours and 10 minutes.

Scenario 2 b Scenario 3 a. After working for 6 hours, a break of 30 minutes is given. Then, driving is resumed for 2.5 hours more and another break of 15 minutes is taken, as the duty time has reached 9 hours. After one more hour of driving, another break of 30 minutes is required, because the total driving time is 4.5 hours. 10

Scenario 3 a b. This driver breaks assignment can be improved by allocating a 45-minute break when the duty time reaches 6 hours. This journey requires no additional breaks because the 45-minute break reset the driving hours.

Scenario 3 b

Scenario 4 a. This scenario is similar to the previous one, except that in the previous scenario, the driver completes the journey after 2.5 hours of driving after the first break. However, after the first break, the driver continues to drive for 4 hours and 40 minutes.

Scenario 4 a

b. Allocating 45 minutes to reset the driving break is no longer a good idea in this scenario because another break will be triggered due to reaching 4.5 hours driving time. As a result, the journey will take 12 hours and 10 minutes.

Scenario 4 b

c. However, if we increase the second break in Scenario 4 a from 15 to 30 minutes, no further driver breaks are required. As a result, the journey is reduced to 11 hours and 40 minutes.

Scenario 4 c

Scenario 5 a. The arrival time at the customer site was 2:30, but a wait of 15 minutes was required due to the time window constraint. A break was assigned during the wait. A duty break of 15 minutes was given after working for 6 hours. After that, driving was resumed for 45 minutes, when a driving break was needed because the total driving time was 4.5 hours.

Scenario 5 a

b. This driver breaks assignment can be improved by allocating a 30-minute break after 6 hours of duty. Because the accumulated 45 minutes break reset the driving hours, this journey requires no additional breaks.

Scenario 5 b

Scenario 6 a. This scenario is similar to the previous one. But in this case, the driver continues to drive for 4 hours and 40 minutes after the second break.

Scenario 6 a

b. Allocating 30 minutes break instead of 15 mintues to reset the driving break is no longer a good idea in this scenario because another break will be triggered due to reaching 4.5 hours driving time. As a result, the journey will take 11 hours and 55 minutes.

Scenario 6 b 13

A summary of the scenarios

   加QQ codinghelp Email: cscholary@gmail.com
