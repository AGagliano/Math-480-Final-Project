Math-480-Final-Project
======================

5 Pages of written text. 

Topic: The Simplex Algorithm

Goal: The program will attempt to solve a standard form linear optimization problem in standard form using
      the simplex algorithm. 

#Outline of paper:

I) Overview of linear optimization problems.
      a) Standard form:
            min cx
            such that Ax <= b
            x1...xn >= 0
      b) real world uses.
II) Geometry of linear optimization problems.
      a)Feasible solutions
      b)No solutions/infeasibility
      c)Solutions at vertices (include diagram)
III) Overview of how simplex algorithm works.
      a) diagrams of this process...vertex checking
      b) the basis
      c) tableau
      d) examples
      e) cases when simplex algorithm fails
IV) Code for the simplex aglorithm
V) Example outputs. 
      

#Outline of code:

Input objective function and constraints
  c = objective vector
  A = constraint coefficient vector
  b = constraint vector
  #I don't think I need to define variables x1....xn, because not necessary for simplex algorithm
  
Set up initial tableau as a matrix filled with matrices that are simply lists of lists(?).

  [0  A I b]  #note, if A is (m X n), then I is (m X m), b is (m X 1), c is (1 X n).
  [-1 c 0 0]

Perform a pivot on the initial tableau

  1. choose column such that the value of c is the largest.
  2. choose row such that the ratio b/A(column values of the column chosen) is smallest.
  3. pivot on this entry. (i.e. row reduce to make an identity column)
  4. repeat on largest value of c until all c values are less than 0.
  5. Note, technically conducting this on c + vector of 0's that are in the basis, so will need to redefine this vector.
  6. check for infeasibility, cycling/degeneracy, etc.
  7. output the optimal solution and value. 


  
  







