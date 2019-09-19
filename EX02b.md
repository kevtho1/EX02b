# EX02b Kevin Thomas and Chris Lopez 

## STEP ONE:
## PET-AND-OWNER (PetName, PetType, PetBreed, PetDOB, OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)
## Functional Dependencies:
## PetName - (PetType, PetBreed, PetDOB, OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)
## OwnerEmail - (OwnerLastName, OwnerFirstName, OwnerPhone)
## OwnerPhone - (OwnerLastName, OwnerFirstName, OwnerEmail)
## PET-AND-OWNER Candidate Keys: PetName
## Is every determinant a candidate key?
## NO—OwnerEmail and OwnerPhone are NOT candidate keys.
## STEP TWO:
## Break into two relations: OWNER and PET
## OWNER (OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)
## PET (PetName, PetType, PetBreed, PetDOB, {Foreign Key})
## FOR OWNER:
## Functional Dependencies:
## OwnerEmail - (OwnerLastName, OwnerFirstName, OwnerPhone)
## OwnerPhone - (OwnerLastName, OwnerFirstName, OwnerEmail)
## OWNER Candidate Keys: OwnerPhone, OwnerEmail
## Is every determinant a candidate key?
## YES—OwnerEmail and OwnerPhone are candidate keys
## We can choose either candidate key as primary key.
## (A) IF WE USE OwnerPhone as primary key, THEN:
## OWNER (OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
## PET (PetName, PetType, PetBreed, PetDOB, OwnerPhone)
## Functional Dependencies:
## PetName - (PetType, PetBreed, PetDOB, OwnerPhone)
## PET Candidate Keys: PetName
## Is every determinant a candidate key?
## YES—PetName is a candidate key
## FINAL NORMALIZED REALTIONS:
## OWNER (OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
## PET (PetName, PetType, PetBreed, PetDOB, OwnerPhone)
## (B) IF WE USE OwnerEmail as primary key, THEN:
## OWNER (OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
## PET (PetName, PetType, PetBreed, PetDOB, OwnerEmail)
## Functional Dependencies:
## PetName - (PetType, PetBreed, PetDOB, OwnerEmail)
## PET Candidate Keys: PetName
## Is every determinant a candidate key?
## YES—PetName is a candidate key
## FINAL NORMALIZED REALTIONS:
## OWNER (OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
## PET (PetName, PetType, PetBreed, PetDOB, OwnerEmail)
