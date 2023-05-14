# Example: Creating a Merge Conflict
For purposes of illustration, as we did in an earlier lesson, we're going to intentionally create a merge conflict in order to simulate the situation in which two members of a team have pushed up conflicting changes to a file. Note that, in doing this, we will depart from best practices in a couple of instances.
Say one of our coauthors is working on Chapter 2. They create a new chapter-2 branch and add their draft. At the same time (ignoring best practice), Author 2 also make a few edits to Chapter 1. Let's go ahead and do that:
	1. Create a new branch, chapter-2, and switch to it.
	2. Create a chapter-2.md file and add some content.
	3. Still on the chapter-2 branch, make a few small edits to the first couple of sentences or paragraphs in chapter-1.md. These can be anything you like.
	4. When you're done, commit the changes.
Next, we'll make a few edits to Chapter 1 as Author 1. Normally, we would create a new branch to do this but, to keep things simple, we'll make the edits directly on the main branch:
	1. Switch to the main branch; you should see in VS Code that chapter-2.md is no longer in the file list.
	2. In chapter-1.md, make different changes to one or two of the pieces of text you edited above.
	3. Commit the changes, and push them to GitHub.
Note that the order here is important! To create a merge conflict, we need to make sure that we create the chapter-2 branch before making the edits to Chapter 1 in the main branch. Otherwise the changes we made on main will be in chapter-2 as well, and there will be no conflict.
Finally, switch back to the chapter-2 branch and push it up to GitHub.
We have now created the situation where Author 1 pushed changes up to GitHub after Author 2 created the chapter-2 branch off of main. In other words, there are changes in chapter-1.md on GitHub that aren't reflected in Author 2's chapter-2 branch.
