# Python Activity-Based Learning
## Case Study 20 – University Admission Decision Engine

### 1. Problem Statement
Design a Python program to evaluate university admission applicants based on subject-wise eligibility, aggregate marks, course-specific minimum thresholds, and predefined tie-breaking rules. The program identifies eligible applicants and ranks them according to their performance.

### 2. Objectives
1. Check minimum marks in all subjects.
2. Calculate aggregate percentage.
3. Apply course-specific minimum aggregate requirements.
4. Separate eligible and ineligible applicants.
5. Rank eligible applicants using predefined tie-breaking rules.

### 3. Assumptions
- Three subjects are considered: Mathematics, Physics, and Computer Science.
- Minimum subject mark is 50.
- Course-wise aggregate requirements:
  - CSE = 70%
  - ECE = 65%
  - EEE = 60%
- Ties are resolved by:
  1. Higher Mathematics marks.
  2. Higher Computer Science marks.
  3. Alphabetical order.

### 4. Algorithm
1. Store applicant details in a list of tuples.
2. Store course thresholds.
3. Calculate total and aggregate for each applicant.
4. Check subject-wise minimum marks and course threshold.
5. Store applicants in eligible or ineligible lists.
6. Rank eligible applicants using nested loops and tie-breaking rules.
7. Display the final ranking and ineligible applicants.

### 5. Pseudocode
```text
START
    Set minimum subject mark = 50
    Set course thresholds
    Store applicant details

    FOR each applicant:
        Calculate total and aggregate
        Check subject eligibility
        Check course threshold

        IF eligible:
            Store in eligible list
        ELSE:
            Store in ineligible list

    FOR each pair of eligible applicants:
        Compare aggregate marks
        Compare Mathematics marks
        Compare Computer Science marks
        Compare names
        Swap when required

    Display ranking and ineligible applicants
STOP
```

### 6. Flowchart
```text
START
   |
Store Applicant Details
   |
Set Minimum Marks and Course Thresholds
   |
Calculate Aggregate
   |
Check Subject Eligibility
   |
Check Course Threshold
   |
Eligible?
  /    \
YES    NO
 |      |
Eligible  Ineligible
 List      List
   \      /
 Rank Eligible Applicants
          |
 Apply Tie-Breaking Rules
          |
 Display Results
          |
         STOP
```

### 7. Python Source Code

The program uses:
- Variables
- Lists and tuples
- Conditional statements
- Loops
- Tuple unpacking
- Sorting using nested loops

### 8. Test Cases

| Test Case | Applicant | Course | Expected Result |
|---|---|---|---|
| 1 | Anil | CSE | Eligible |
| 2 | Bhavya | ECE | Eligible |
| 3 | Charan | CSE | Eligible |
| 4 | Divya | EEE | Eligible |
| 5 | Esha | CSE | Ineligible |
| 6 | Farhan | ECE | Eligible |

### 9. Sample Output

```text
UNIVERSITY ADMISSION RANKING
----------------------------

Rank: 1
Name: Anil
Course: CSE
Aggregate: 82.0 %

Rank: 2
Name: Charan
Course: CSE
Aggregate: 73.33 %

Rank: 3
Name: Bhavya
Course: ECE
Aggregate: 70.0 %

Rank: 4
Name: Farhan
Course: ECE
Aggregate: 70.0 %

Rank: 5
Name: Divya
Course: EEE
Aggregate: 65.0 %

INELIGIBLE APPLICANTS
----------------------------

Name: Esha
Course: CSE
Aggregate: 72.0 %
```

### 10. Conclusion

The University Admission Decision Engine evaluates applicants using subject-wise minimum marks and course-specific aggregate requirements. It separates eligible and ineligible applicants and ranks eligible candidates using predefined tie-breaking rules.

The program demonstrates variables, data types, operators, conditional statements, loops, lists, tuples, and tuple unpacking.
