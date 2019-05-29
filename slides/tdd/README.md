# tdd-docs



## Intro

1. Terminology

    - Functional Test == Acceptance Test == End-to-End Test

1. Naming convention:
 Functional tests  - how the application functions from the user’s perspective.

1. How Unit Tests differ from Functional Tests ?

    - Functional — test the application from the outside
    - Unit — test the application from the inside, from the point of view of the programmer.

1. TDD is there to help us out when we’re not so smart.

1. Analogies

    - Kent Beck (who basically invented TDD) uses the metaphor of lifting a bucket of water out of a well with a rope: when the well isn’t too deep, and the bucket isn’t very full, it’s easy. And even lifting a full bucket is pretty easy at first. But after a while, you’re going to get tired. TDD is like having a ratchet that lets you save your progress, take a break, and make sure you never slip backwards. That way you don’t have to be smart all the time.
    - TDD is a discipline, and that means it’s not something that comes naturally;



1. Rules

    - one of the rules of unit testing — "Don’t Test Constants".
        - Note: testing HTML as text is a lot like testing a constants

              wibble = 3  
              # There’s not much point in a test that says:
              from myprogram import wibble 
              assert wibble == 3

        - Note: Unit tests are really about testing logic, flow control, and configuration



1. The TDD Process

    - Main aspects of the TDD process:
        1. Functional tests
        1. Unit tests
        1. The unit-test/code cycle
        1. Refactoring

    - Overall TDD process:
    ![tdd_process](./img/twp2_0403.png)


    - The TDD process with functional and unit tests:
    ![tdd_process](./img/twp2_0404.png)
    Note: One of my eminent tech reviewers, Emily Bache, wrote a [blog post](http://coding-is-like-cooking.info/2013/04/outside-in-development-with-double-loop-tdd/) on the topic, which I recommend for a different perspective.



1. Better Unit Testing Practice: Each Test Should Test One Thing.
   The reason is that it makes it easier to track down bugs.

1. Rules of thumb:

    - "YAGNI"
        - "You ain’t gonna need it!" ("We _might_ need it")
        - Avoid the temptation to write code that you think _might_ be useful
        - it is the mantra we use to resist our overenthusiastic creative urges
    - "three strikes then refactor"
    - going from working state to working state
        - The Testing Goat encourages us to take one step at a time, and go from working state to working state
        - Split work out into small, achievable tasks



## Recap: On Testing Design and Layout

Section: [static_files_in_django](https://www.obeythetestinggoat.com/book/chapter_prettification.html#_static_files_in_django)


The short answer is:
- you shouldn’t write tests for design and layout per se. It’s too much like testing a constant, and the tests you write are often brittle.

As a result,
- it is valuable to have some kind of minimal "smoke test" which checks that your static files and CSS are working

Why?
- it can help pick up problems when you deploy your code to prod

Aim
- to leave yourself in a position where you can freely make changes to the design and layout, without having to go back and adjust tests all the time
