```
# 1
According to the diagram fulltime student has no methods itself. But in reality an empty class is a useless class
so at the very least it would have methods calling other classes.
```

```
# 2
Part time student can only have 1 PhDprogram but in that program they are able to have
anywehre from 0 to infinte thesis according to the diagram. 
PartTimeStudent has a 1 to 1 relationship to PhDProgram. Which in turn has a 0 to many relationship to PhDThessis.
meaning 1 parttime student can have many thesis.
```

```
# 3
get rid of the Student, FullTimeStudent and PartTimeStudent classes. Aswell as getting rid of getStudent method from PhDThesis
```

```
# 4
HDRManager sits between fulltime/parttime student and PhDProgram. 
The student to HDRManager would be 1 to 1 and HDRManger to student would be 0 to many.
The HDRManager to PhDProgram would have 1 to 1 relationship while the otherway around being 1 to many.
"requestEnrollThesis() would be added to student as well void setStudentThesis()"
Student would request to enroll in a thesis by requestEnrollThesis()
This goes to the HDRManager who then checks to see if the code exists by getThesisCode()
If getThesisCode returns null HDRManager returns an error.
If getThesisCode() returns a value HDRmanager uses setStudentThesis() to enroll the student.
```