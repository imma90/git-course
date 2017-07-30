######################################
Lesson 1: navigating a commit history
######################################

``diff`` laat het verschil zien tussen twee bestanden.

***********
Reflections
***********


 How did viewing a diff between two versions of a file help you see the bug that was introduced?

Je ziet het verschil meteen, want de diff output is kort dus je heb een veel kleiner stuk tekst om door te nemen.

 How could having easy access to the entire history of a file make you a more efficient programmer in the long term?

Als je een fout hebt gemaakt en daar pas later achter komt, kun je terugkeren naar de versie waar de fout nog niet in zat.

Als je wilt weten wanneer een bepaalde feature is toegevoegd, kom je daar snel achter.


************
Concept map
************

 .. TODO: add concept map

 .. figure:: concept_map.jpg

********************************
One commit per logical change
********************************

`One commit per logical change <https://classroom.udacity.com/courses/ud775/lessons/2980038599/concepts/24198785820923>`_

Two small bugs in different functions? Commit separately!

*********************************************
Using Git to View History
*********************************************

 How can you use the commands git log and git diff to view the history of files?

Eerst met ``git log`` een overzicht vna de commit met de bijbehorende ID inzien en dan ``git diff <ID nieuw> <ID oud>``

***********************
Git Errors and Warnings
***********************

***********************************
Checking out older versions of code
***********************************

``git checkout <ID>``


.. note:: Let op dat de output van ``git log`` in omgekeerde chronologische volgorde staat!

########################
Lesson 2: Problem Set 1
########################


#############################################
Lesson 3: Creating and modifying a repository
#############################################

``git init``
  initializes a repository, creates directory .git

the repository is initially empty

``git add``
  adds files to the staging area.

  Er is een staging area, dat is handig om ervoor te zorgen dat één logische verandering in één commit hebt. Als je meerdere logische veranderingen in je working directory hebt, en je wilt maar één hen committen, dan kun je die naar de staging area brengen en de andere nog niet. Bij de commit gaan de veranderingen die je niet naar de staging area gebracht hebt, niet mee.

`A styleguide for commit messages<http://udacity.github.io/git-styleguide/>`_


Viewing your changes
====================

.. image:: git_diff.png

``git diff`` difference between working directory and staging area
``git diff --staged`` difference between staging area and repository

********
branches
********

e.g. experimental feature, Italian version,

- master

Create a new branch:
#. ``git branch mynewbranch`` create a new branch
#. ``git checkout mynewbranch`` checkout to the new branch (so that any changes you make are in the new branch)

 What are some situations when branches would be helpful in keeping your history organized? How would branches help?

If you add an experimental feature where you don't know whether it works, you can mess up your code with the new feature without affecting the main (master) line of development. In the mean time, you can work on your master branch without the experimental feature.

You can merge branches later.

``git log --graph --oneline branch1 branch2``

reachability
 commits have parents, back to the initial commit. Commits from two branches cannot reach each othter.

 Detached HEAD warning: je ben in een eerdere commit. Als je veranderingen maakt, moet je een nieuwe branch maken de verandering te committen.

*********
 Merging
*********

A merge is a commit

Merge the coins branch into the master branch.

.. image:: git_merge.png

``git log`` shows the commit history of both branches.
The commits in the coins branch will still be reachable.


Commit history will be chronological. dus de commits van 2 branches staan door elkaar.

``git diff`` vs ``git show``:

- git show shows the difference with the parent commit
- git diff shows the difference between two commits (that might originate from two different branches)

merge conflict
 similar changes in two branches

#######################################
Lesson 4: Using github to collaborate3
#######################################

``git clone``
