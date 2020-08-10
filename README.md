# Game Tower of Hanoi

**Projects of Elementary Number Theory Course (MA2252)**

2nd Semester of Academic Year 2018/2019


Lecturer : Hilda Assiyatun, M.Si., Ph.D.

![alt text](doc/menu.png "Main Menu")

Game created by:
* 10117005 Irma Nazelia
* 10117019 Ilma Aliya Fiddien
* 10117073 Nurul Syafithri
* 10117113 Agapitus Keyka Vigiliant


## How To Play

In this game, there are three pegs and some discs of different sizes. The objective of this game is to move the discs on the leftmost peg to the rightmost peg. You can use the middle peg to help you. There is only one rule of this game. That is, a disc cannot be placed over a larger disc. To move a disc, drag and drop the disc to the targeted peg. Do this procedure repeatedly until you manage to move all the discs to the rightmost peg.


## History

The Tower of Hanoi is a puzzle that was widely believed to be invented by the French mathematician Eduoard Lucas in 1883. The puzzle, also called the Tower of Brahama or End of the World Puzzle, was created out of an old Hindu legend. The story tells of a Hindu temple at the center of the world where priests were given a stack of 64 golden disks of decreasing size. The disks were stacked on one of three towers. The priests were to transfer the stack of disks from the starting tower to another, using some given rules. The priests were to work diligently. There are some variations of this legend.


## The Secret

There is a mathematical secret behind this game… It turns out you only need no more than 2n-1 moves to move n discs from the initial peg to the final peg. This optimum solution is based on a recursive process. That is, a process which is done repeatedly. By knowing this process, you can solve this game much quicker! All you need to do is memorising this process (or as we like to call it, algorithm). To make things easier, we label the peg A, B, and C, as follows.

So the main idea behind the algorithm to solve the game using n discs can be summarised as follows:
1. Move all discs, except the largest one, from initial peg (A) to auxiliary (a peg other than the initial and target peg) peg (B).
2. Move the largest disc from initial peg (A) to target peg (C).
3. Move the discs which is now in auxiliary peg (B) to target peg (C).

Obviously we cannot move more than 1 disc at once, so step 1 and step 3 can only be done using multiple steps. So how to do step 1 and 3? Just use this algorithm! But instead of setting A as the initial peg and C as the target peg, set A as the initial peg and B as the target peg because we want to move n-1 discs from peg A to peg B, if you want to do step 1. Similarly, set B as the initial peg and C as the final peg if you want to execute step 3 above. The point is, use this algorithm whenever you want to move a set of discs by adjusting the initial peg, auxiliary peg, and the target peg accordingly.
                   
So where does the 2n-1 come from? Well, let’s have a look at our algorithm. Let Hn be the number of moves needed to move n discs from an initial peg to target peg. Since there are n-1pegs to be moved in step 1, thus step 1 needs Hn-1 moves. It is obvious that step 2 needs only 1 move. How about step 3? For the same reason as step 1, it needs Hn-1 moves. So, we can conclude that Hn = Hn-1 + Hn-1 + 1 = 2Hn-1 + 1. By solving this recurrence relation, you can find that Hn = 2n - 1, by setting H1 = 1. This result can also be proved using induction.


## Source
* Liu, D. The Tower of Hanoi. Retrieved from http://www2.mtsd.k12.wi.us/homestead/users/ordinans/Tower%20of%20Hanoi.html
* MG's Tower of Hanoi For Python.\nRetrieved from https://www.pygame.org/project/3191
