# Software Architectures Assignment 4
From the assignment sheet:

In this assignment, you will refine the Families metamodel from the tutorial, and write a new ATL transformation to create an instance of this refined metamodel:

- [X] Create a new metamodel named “ExtendedFamilies.ecore”. Create a `Family` class and a “Person” class. The `Person` class is an abstract class. Create two subclasses of `Person`: `Male` and “Female`.
In the `Family` class, create a `lastName` attribute [1..1] of type `Estring` and a `members` reference [0..\*] of type `Person`, `members` is a containment reference. Also add a `noOfChildren` attribute [0..\*] of type `EInt`. In the `Person` class, create a `firstName` attribute [1..1] of type `EString`, a `family` reference [0..1] of type `Family`, a `children` reference [0..*] of type `Person`, and a `parents` reference [0..2] of type `Person`. The `family` reference is the opposite of the `members` attribute in the `Family` class, and the `children` reference is the opposite of the `parents` reference.
- [X] Create a new ATL transformation module named `Families2ExtendedFamilies.atl`. This transformation should transform each Member to a Male or a Female and set the correct parent/child references. Also add to the above `noOfChildren` attribute the number of children of each family.
- [X] A new policy requires that the transformation output to also indicate if a family is single-parent or not as an attribute (in addition to the `lastName`). Add the necessary setup/rules to enforce this. Use the same transformation module as in Q2.

Use abstract rules, helpers and rule inheritance where possible (e.g. A `Member2Person` abstract rule that specifies how a Member instance is transformed to a Person instance, without going into details about Male/Female or parent/child), and make sure you comment your intentions in the code.
