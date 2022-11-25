# dbms-notes
- Superkey is a set of attributes that uniquely identifies each tuple of a relation.
- Candidate key is a minimal superkey
- symbols and their meanings
```
Symbol Meaning
*      closure
->     determines
FD     FunctionalDependency

```
- Examples
``` 
   In a FunctionalDependency FD{A->B,B->C,C->D} closure helps in determining the candidate key 

   A*=ABCD
 
   B*=BCD
 
   C*=CD
 
   D*=D
 
   A,AB,AC,AD,ABC,ACD can take the place as a superkey but the minimal superkey is A, hence A is the candidate key 
   The prime attributes are the ones that can become a candidate key.In this case A is a prime attribute.
   Non prime attributes are B,C,D
  ```
 ```
   In a FunctionalDependency FD{A->B,B->C,C->D,D->A} closure helps in determining the candidate key 

    A*=ABCD
 
    B*=BCDA
  
    C*=CDAB
 
    D*=DABC
 
    A,B,C,D can take the place as a superkey and also the candidate key.
    
    In this case all keys A,B,C,D are prime attributes
   
```
 ```
   In a FunctionalDependency FD{A->B,BC->D,E->C,D->A} 
   BDCA are all getting determined and hence E is the only one attribute which is not being determined.
   So E should be in the formation of candidate key
   E*=EC
   
   AE*=ABECD
   
   DE*=DABEC
   
   BE*=BECDA
   
   CE*=CE
   
   So,AE,BE and DE can take the place as a candidate key.
    
   In this case AE,BE,DE are prime attributes.
   
```
