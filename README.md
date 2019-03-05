## Branching Policies

“I am [Alejandro París](https://www.linkedin.com/in/alejandro-par%C3%ADs-g%C3%B3mez-05a675129/), student of the
[Bachelor’s Degree in Video Games by UPC at CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). 
This content is generated for the second year’s
subject Project 2, under supervision of lecturer [Ricard Pillosu](https://es.linkedin.com/in/ricardpillosu).”

### The concept 

Branching policies are followed by rules that are established to maintain control over the project. They help to organize, to work in parallel and to solve any problem related to the structure of the project in a simpler way.
Good branching policies together with a good team will do a better job.

To know the advantages of a good branch policy, we will focus on two forms of work.

The Trunk-Based Development in which the entire team works in the same branch and only has the branch of releases separate, therefore when someone checks-in with wrong code everyone must wait for it to fix it in order to continue working.

<img src= "BranchingPoliciesResearch/images/trunk-based.png" width="250" height="250">

On the other hand we have the Feature Branching Development in which all the features are made external to the main branch and are integrated at the time they are completed. Therefore, the problem presented by the trunk-based is avoided.
In spite of avoiding this problem other inconveniences arise as they are when lengthening a long time a feature branch if it does not stay updated with the main branch can end up giving problems when trying to join them.
An example of this branch policy is Gitflow.

<img src= "BranchingPoliciesResearch/images/gitflow-present.png" width="250" height="250">

The need for this kind of ruling arises from the fact that organising a group of people to work together, for the same standards, and make it all work is almost impossible with no clear instructions on how to act in every situation that may come up. Having this kind of instructions and rules prevents repository damage, since the main branches are protected and can only be manipulated by the administrator.

The administrator is the only user with permission to allow modifications to the main branches such as pull requests and merges. There might be more than one administrator and even be more that one kind of administrator (for example, the Lead Programmer should only manage develop and hotfixes while the QA Lead manages releases and master). You can control all these settings on the Github website.

The way regular workers interact with these main branches is by branching off from develop and creating their own fature branches, in which they can develop their fature and merge it back with the main develop branch (by creating a pull request) after it is finished and has passed all needed verifications. By using this method, we avoid any danger to the project while still keeping all flexibility that a worker may need in his 

### Benefits and drawbacks

### Gitflow Structure

<img src= "https://github.com/AlejandroParis/BranchingPoliciesResearch/blob/master/images/gitflow.png" width="250" height="250">

### QA with Gitflow

### Appveyor


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2


- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Sources



### Contact

paris.alejandro1@gmail.com
