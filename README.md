# portfolio
hosts the content for my portfolio webpage

I try not to be overly technical (though I must admit that sometimes I have) so that it
can be understood by professionals from various disciplines.

## Singularities in reactive separation processes

This [work](https://doi.org/10.1021/ie0716159) was published in the Industrial and
Engineering Chemistry Research and it involved the development of numerical code
written in Matlab to simulate a process that involved phase separation (liquid and vapor)
and a chemical reaction at steady-state conditions. We were concerned with the detection
of process singularities such as multiple steady-states, meaning that the process could
have more than one possible state for the same operating conditions with some of those
states being unstable.

This was my first research project as a graduate student in the University of Puerto
Rico -- Mayaguez. At that point I had already done some programming with Matlab for
the Advanced Chemical Engineering Thermodynamics course though my first programming
experience was with the C language. I like to bring this up because I was among the last
generation of chemical engineers who learned the C language, for the following semester
the engineering program was revised and Matlab would be taught instead. And that
change made sense because Matlab is a mathematically oriented programming language;
on the other hand, C even though is a general purpose language it's usually considered
to be a systems programming language. Anyone that knows a little about the development
of Unix and later Linux operative systems knows this for a fact. Nevertheless, I see
my exposuse to the C language as a great experience and I encourage anyone passionate
about programming to learn C at some point in their careers. For example it gives you
the intuition to tell that the `const` qualifier in JavaScript hints at the fact that
the variable is really a pointer to the underlying type and that the `const` allows
you to modify the object but not the reference to the object.

Gerardo Ruiz was a senior in this project and he had already published in the area
and was well versed in the craft of writing numeric code and the process that we were
trying to simulate. His input was instrumental for me for the development of my own code.
Instead of running his code, my task was to develop the whole code from scratch so that
I could use that experience to study other processes. I remember that I began by adding
functions to compute thermodynamics and dynamic properties (activity coefficients,
viscosity, kinetic constants, etc.). I am surprised that by then I had the discipline to
write my functions so that they would do one thing alone (single purpose principle) and
that I should test my code often to fix bugs early on, for I did not have any other
experiences with courses about software development and best practices. I remember
that I read a little about that in a book we had about Matlab at the office and probably
by heeding Gerardo's advice.

After writing the code that the sets the thermodynamic properties and the dynamic
properties of the fluids that pass through the system I had to express the model
equations (conservation of chemical species and energy) into the form that Matlab's
numerical optimization solver expects. The experience that I had with the solution of
engineering thermodynamics problems allowed me to write the code with confidence. One
could think that once one has written down all the equations into a way that can be
handled by the numerical solver that the problem has been practically solved but that's
not the case. We were dealing with a non-linear model and that meant that the solver
can still fail to converge to a solution if the starting point (or initial guess) is
not close enough. As a result of that we had to break up the solution into stages,
first obtain an approximate solution without the intricancies of the non-linear model and
then hope that that solution is good enough for a starting point for the non-linear
model. And from there we applied a numerical technique known as homotopy continuation
to arrive at other solutions and check for process singularities.

At that point we crossed check our codes to make sure that we arrive at the same results.
As you may imagine this took a considerable time to fix implementation errors that
affected the results. The issue with numerical simulations is that you may get results
that seem right but are not because of some minor thing like a typo in a contant or
a sign. And those errors are hard to detect with the number of lines of code that
comprise the numeric application.

That experience taught me how to tackle hard problems by breaking them down into smaller
units and to write code to test those units for correctness. I also learned the
importance of teamwork, for I would not have been able to solve the problem on my own
in a relatively short time (just a couple of months) if it weren't for Gerardo's
input. All of this probably sounds familiar to you but I don't think there's another way
to get things done other than work on it everyday, communicate ideas with your peers,
learn things as you go, and most importantly believe in your ability to solve a
problem that at first migth seem daunting.
