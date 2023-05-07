Download Link: https://assignmentchef.com/product/solved-esc794-homework-1
<br>
<ul>

 <li>Dynamic Matrix Control (DMC) uses a specific kind of plant model to make predictions for a receding-horizon optimal control implementation. Do a little research and write a 1-page (plus at most 5 references) summary of DMC, focusing on the plant model, the history and the applications.</li>

 <li>When forward Euler discretization is applied to a linear state-space system ˙<em>x </em>= <em>Ax</em>, the following discrete equivalent is obtained:</li>

</ul>

<em>x</em><sup>+ </sup>= (<em>I </em>+ <em>δA</em>)<em>x</em>

where <em>δ </em>is the sampling interval. Find the continuous/discrete eigenvalue mapping as done in class for backward Euler and comment on any stability preservation properties upon forward Euler discretization.

<h1>3  (mini-project)</h1>

A mechanical system (robotics) model without gravity effects is given by

<em>M</em>(<em>q</em>)<em>q</em>¨+ <em>C</em>(<em>q,q</em>˙)<em>q</em>˙ = <em>u</em>

where <em>q </em>is the vector of joint coordinates, <em>M</em>(<em>q</em>) is the mass matrix (always symmetric and positive-definite) and <em>C</em>(<em>q,q</em>˙) is a matrix containing Coriolis and centripetal effects. The control torque vector is <em>u</em>.

A nonlinear state-space model can be obtained by defining the state vector as [<em>q<sup>T </sup>q</em>˙<em><sup>T</sup></em>]. With these definitions, the state-space model is

<em>z</em>˙<sub>1 </sub>=      <em>z</em><sub>2</sub>

<em>z</em>˙<sub>2 </sub>=          <em>M</em><sup>−1</sup>(<em>z</em><sub>1</sub>)(<sup>−</sup><em>C</em>(<em>z</em><sub>1</sub><em>,z</em><sub>2</sub>)<em>z</em><sub>2 </sub>+ <em>u</em>)

Symbolic Matlab code has been provided to obtain and evaluate ˙<em>z</em><sub>2</sub>, and a Simulink template to simulate the nonlinear dynamics has also been provided.

<ol>

 <li>Note that any state of the form [ 0] is an equilibrium point with <em>u </em>= 0. Use Matlab’s diff to linearize the state-space model at <em>q<sup>T </sup></em>= [0 <em>π/</em>4 0 <em>π/</em>4]. Obtain continuous-time matrices <em>A </em>and <em>B </em>for the linearization.</li>

 <li>Use nilpotent matrix approach to obtain the ZOH discrete equivalent Γ and Φ sampledat <em>T</em><em>s </em>= 0<em>.</em>01 s.</li>

 <li>You now have 3 models. Test the accuracy of the linearization and the discretization by applying the test torque inputs provided in the template to each model. Note that the linearized system and its discretization use incremental states and inputs, therefore appropriate shifting must be used.</li>

 <li>Show plots of each one of the eight states, as obtained by each model.</li>

 <li>Design a discrete LQR controller to stabilize the discretized system at the equilibrium.Use <em>Q </em>= <em>I </em>and <em>R </em>= 0<em>.</em>1<em>I </em>as initial tuning. Test the operation of this controller against the discretized system, the linearized C-T system and finally the nonlinear system. Shift as required. Simulate the deadbeat regulator applied to the nonlinear system using some initial condition near the equilibrium condition in use. Informally run some simulations to see how far the initial conditions can be from the equilibrium without losing stability.</li>

</ol>

<strong>4 </strong>Reproduce the procedure described in class to find the largest invariant ellipsoid contained in a set of box constraints for the double-integrator plant.

Note: Running code must be submitted for 3 and 4.