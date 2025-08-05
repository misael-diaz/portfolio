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
