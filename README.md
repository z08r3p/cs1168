java cFinal Project Due: Jan. 10 2025
The grading of the final project is based on the code development displayed in your github repository (50 points) and your submitted report (50 points).
Submission Guidelines:
1. Provide the code development history in the github repository with clear file structures and a README file describing how to run the code.
2. Submit a PDF of the report.
Code development:
Consider a plane elasticity problem defined on the x-y plane. Implement a finite element code using bilinear quadrilateral element or linear triangle element.
• Generate the mesh (including the nodal coordinates, the IEN connectivity, etc.)
using Gmsh. Allow the user to specify different geometries
(10 points).
• Regarding the boundary conditions, you need to allow the specification of either
displacement (Dirichlet) or traction (Neumann) boundary condition on these
boundary edges in your code (10 points).
• Regarding the model, you may allow the users to specify either plane strain or
plane stress for the two-dimensional analysis. The material is homogeneous
isotropic elastic (5 points).
• Provide a visualization routine that can draw the displacement, strain, and stress
on the modeled elastic body (10 points).
• Provide an error calculator that may calculate the relative errors in the 𝐿!- and
𝐻"-norms (15 points).
Final project report:
• State the strong-, weak-, and Galerkin formulations. Discuss the boundary
conditions (5 points).
• Discuss your chosen implementation of the element stiffness. Consult Sec. 3.10 of
the textbook for different implementations (5 points).
• Verify the implementation of the code using a manufactured solution. Report the
errors and convergence rates measured in the 𝐿!- and 𝐻"-norms, respectively (10 points).
   1

• For an infinite plate with stress-free circular hole under constant far-field in-plane tension, the exa代 写data 、 java/Python
代做程序编程语言ct stress has been found (see M.H. Sadd, Elasticity: Theory, Applications, and Numerics, pp. 176-177),
𝑇 𝑅! 𝑇 𝑅! 𝑅% 𝜎##(𝑟,𝜃)= $-1− !1+ $-1−4 !+3 %1𝑐𝑜𝑠2𝜃,
2𝑟2𝑟𝑟
𝑇 𝑅! 𝑇 𝑅% 𝜎(𝑟,𝜃)= $-1+ !1− $-1+3 %1𝑐𝑜𝑠2𝜃,
2𝑟2𝑟
𝑇 𝑅! 𝑅% 𝜎#(𝑟,𝜃)=− $-1+2 ! −3 %1𝑠𝑖𝑛2𝜃.
2𝑟𝑟
Use the above analytic stress result to design a verification for the finite element code. You may consider a quarter of the plate with finite size (see Fig. 1 Elastic plate with a circular hole: problem definition), by leveraging symmetry boundary conditions. This may significantly reduce the computational load. Discuss the symmetry boundary condition and its implementation in the code. On the outer boundary of the finite quarter plate, apply Neumann boundary conditions using the exact stress results given above. Progressively refine the mesh. Monitor the stress error and convergence rate (15 points).
   !" = $
Exact solution
Symmetry
Fig. 1 Elastic plate with a circular hole: problem definition
• The stress analysis for structures with holes can be common in engineering practice. Consider the following plane elastic body with side length 4m and a hole in the center (see Fig. 2). The hole has radius 0.5m. It is loaded with a uniform traction of 10 kPa over its left and right faces. There is no body force. Again, only a quarter of the domain needs to be analyzed, which is shown as the dark area in the following figure. The Young’s modulus is 10' Pa and Poisson’s ratio is 0.3. Use your own code to perform a plane stress and plane strain analysis of this problem. Provide displacement and stress visualizations. Discuss results, including insights into stress concentrations (15 points).
  2
Symmetry
Exact solution

  R=0.5 m
Symmetry Plane
10 kPa
10 kPa
 4.0 m
Fig. 2 Geometrical setting of a square plate with a hole.
3
Symmetry Plane

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
