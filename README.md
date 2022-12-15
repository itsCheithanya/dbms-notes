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
    
   In this case A,B,E,D are prime attributes.
   
```
- Functional dependency tells the realtionship of attributes
## 1nf : a table should not contain multivalued attributes
## 2nf : 1nf + all the non prime attributes should be fully functional dependent on the candidate key.
```
if the candidate key is a combination of two attributes(**AB**) the non prime attribute(**C**)should not depent on a part of the candidate key (that is **A** or **B**) which is called partial dependency.
```
### REMEDY:make a new table having non-prime attribute with the part of the candidate key and make the part of the candidate key as the new primary key in that new table and remove the non-prime attribute from the original table

## 3nf : 2nf + no nonprime attribute of R is transitively dependent on the primary key.

that is left hand side of FD should be a candidate key or the right hand side of FD should be a prime attribute

### REMEDY: make a new table having the non-prime attribute with its dependending key and make its dependending key as the new primary key in that new table and remove the non-prime attribute from the original table

### BCNF :3nf + it is more restrictive than 3nf 

that is left hand side of FD should be a candidate key and the right hand side of FD can be a prime attribute/non-prime attribute

### REMEDY: make a new table having the dependent(prime/non-prime) attribute with non-candidate key and make the non-candidate key as the new primary key in that new table and remove its dependent from the original table.

## 4nf : 3nf + no multivalued dependency


## 5nf : 4nf + lossless decomposition.
