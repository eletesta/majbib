Decomposition
=============

In this page, we lists work describing decomposition techniques using majority
functions.

Axiomatic majority-decision logic
---------------------------------

(Cohn, Lindaman, 1961) :cite:`CL61`

The paper introduces an axiomatic system consisting of 10 axioms that use
majority logic.  These 10 axioms contain, e.g., the variant :math:`\langle
xyz\rangle = \langle yxz\rangle` of the commutativity rule, and the variant
:math:`\langle xxy\rangle = x` of the majority rule.  From these 10 axioms,
first 13 theorems are derived that are useful for logic optimization.  Among
these 13 theorems, one finds inverter propagation and the associativity,
complementary associativity, and distributivity rule.  Finally, the authors
introduce what they call the *fundamental theorem of majority-decision logic*,
which they argue to be the majority-equivalent to Boole's law of development or
Shannon decomposition (*fundamental theorem of Boolean algebra* called in their
paper).  Their fundamental theorem states that

.. math::

    f(x_1, x_2, x_3, \dots, x_n) &= \langle\langle x_1x_2f_{x_1\bar x_2}\rangle\langle \bar x_1\bar x_2f_{x_1\bar x_2}\rangle f_{x_1x_2}\rangle &\quad\text{(a)} \\
                                 &= \langle\langle x_1\bar x_2f_{x_1x_2}\rangle\langle \bar x_1x_2f_{x_1x_2}\rangle f_{x_1\bar x_2}\rangle &\quad\text{(b)} \\
                                 &= \langle\langle \bar x_1x_2f_{x_1x_2}\rangle\langle\bar x_2x_3f_{x_2x_3}\rangle\langle\bar x_3x_1f_{x_3x_1}\rangle\rangle & \quad\text{(c)} \\
                                 &= \langle\langle x_1x_2f_{x_1\bar x_2}\rangle\langle \bar x_1x_2f_{x_1x_2}\rangle \bar x_2\rangle, & \quad\text{(d)}

where

.. math::

    f_{x_1x_2} &= f(x_1, x_1, x_3, \dots, x_n), \\
    f_{x_1\bar x_2} &= f(x_1, \bar x_1, x_3, \dots, x_n), \\
    f_{x_2x_3} &= f(x_1, x_2, x_2, \dots, x_n), \\
    f_{x_3x_1} &= f(x_3, x_2, x_3, \dots, x_n).

The theorem comes in four identities, called (a), (b), (c), and (d).

Majority gate networks
----------------------

(Amarel, Cooke, Winder, 1964) :cite:`ACW64`

The paper discusses the decomposition of simple threshold functions (i.e., all
weights are 1) by means of majority-:math:`n` gates.  It also discusses the
special case of decompositions of majority-:math:`n` in terms of smaller
majority gates.  In their paper they restate the problem *How can the 5-argument
majority function be realized with a network of 3-input majority gates?*
initially proposed by D.A. Huffman.  They conjectured that the best way to
represent the majority-7 function is by using 9 majority-3 gates, which was
later improved and is now known to be 7 majority-7 gates.

An extension of the method of Cohn and Lindaman
-----------------------------------------------

(Miyata, 1964) :cite:`Miyata64`

The paper discusses the exact conditions for functions :math:`A`, :math:`B`,
:math:`C`, and :math:`D`, which do not depend on variable :math:`x`, such that
:math:`F = \langle x\langle \bar xAC\rangle\langle \bar x BD\rangle\rangle`.

The minimization of schemes on a majority basis
-----------------------------------------------

(Rozenblyum, 1968) :cite:`Rozenblyum68`

The paper discusses majority decomposition identities for monotone and arbitrary
Boolean function.  It derives identities, which can act as rewriting rules and
allow to express a given majority decomposition in terms of another one by
simple Boolean transformations.
