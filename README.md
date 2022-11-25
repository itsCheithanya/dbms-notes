# dbms-notes
- Superkey is a set of attributes that uniquely identifies each tuple of a relation.
- Candidate key is a minimal superkey
- In a FunctionalDependency FD{A->B,B->C,C->D} closure helps in determining the candidate key 

   A*=ABCD
 
   B*=BCD
 
   C*=CD
 
   D*=D
 
   A,AB,AC,AD,ABC,ACD can take the place as a superkey but the minimal superkey is A, hence A is the candidate key 
