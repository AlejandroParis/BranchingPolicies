# Branching Policies

“I am [Alejandro París](https://www.linkedin.com/in/alejandro-par%C3%ADs-g%C3%B3mez-05a675129/), student of the
[Bachelor’s Degree in Video Games by UPC at CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). 
This content is generated for the second year’s
subject Project 2, under supervision of lecturer [Ricard Pillosu](https://es.linkedin.com/in/ricardpillosu).”

# The concept 

Branching policies are followed by rules that are established to maintain control over the project. They help to organize, to work in parallel and to solve any problem related to the structure of the project in a simpler way.
Good branching policies together with a good team will do a better job.

To see the advantages of branch policies we will see two ways of working one with a light branch policy and another with a branch policy that is currently used by most companies in the industry.

The Trunk-Based Development in which the entire team works in the same branch and only has the branch of releases separate, therefore when someone checks-in with wrong code everyone must wait for it to fix it in order to continue working. This is a policy that used to be used but that has been outdated by the Feature Branching Development

![trunk](https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/trunk-based.png)

On the other hand we have the Feature Branching Development in which all the features are made external to the main branch and are integrated at the time they are completed. Therefore, the problem presented by the trunk-based is avoided.
In spite of avoiding this problem other inconveniences arise as they are when lengthening a long time a feature branch if it does not stay updated with the main branch can end up giving problems when trying to join them.
An example of this branch policy is Gitflow.

![trunk](https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/gitflow-present.png)

The need for this kind of ruling arises from the fact that organising a group of people to work together, for the same standards, and make it all work is almost impossible with no clear instructions on how to act in every situation that may come up. Having this kind of instructions and rules prevents repository damage, since the main branches are protected and can only be manipulated by the administrator.

The administrator is the only user with permission to allow modifications to the main branches such as pull requests and merges. There might be more than one administrator and even be more that one kind of administrator (for example, the Lead Programmer should only manage develop and hotfixes while the QA Lead manages releases and master). You can control all these settings on the Github website.

The way regular workers interact with these main branches is by branching off from develop and creating their own fature branches, in which they can develop their fature and merge it back with the main develop branch (by creating a pull request) after it is finished and has passed all needed verifications. By using this method, we avoid any danger to the project while still keeping all flexibility that a worker may need in his local codebase since he can still make modifications to the original code while not affecting the rest of the development team.

# Gitflow Structure

<img src="https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/gitflow.png" width="490" height="575">

## Master and Develop

The Gitflow structure has two parallel and infinite branches: the master branch that will be updated with the main stable versions of the project and the develop branch in which the development will progress and we will always be able to find the latest version of the project in which we are working.

<img src="https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/main-branches.png" width="450" height="575">

These two branches are the only ones that remain from the beginning of development until the end.

## Feature

May branch off from:
develop
Must merge back into:
develop

<img src="https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/feature-branches.png" width="300" height="575">

The feature branches are essentially the branches in which the developers work in their respective fields to develop the different parts of the release in which they are working at that moment. To avoid problems when doing the merge the feature branches must be kept updated with the information of the develop branch.

## Release

May branch off from:               							
develop											
Must merge back into:									
develop and master

![trunk](https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/release-branch.png)

Release branches support preparation of a new production release.En el momento en que todo lo que debe contener la release está en la rama develop se genera esta nueva rama para acabar de arreglar los últimos bugs y preparar toda la metadata de la release (version number, build dates,...). De esta manera en la rama develop se puede continuar trabajando para la siguiente release.

## Hotfix 
May branch off from:
master
Must merge back into:
develop and master 

<img src="https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/hotfix-branches.png" width="508" height="575">

Hotfix branches are very much like release branches in that they are also meant to prepare for a new production release, albeit unplanned. They arise from the necessity to act immediately upon an undesired state of a live production version. When a critical bug in a production version must be resolved immediately, a hotfix branch may be branched off from the corresponding tag on the master branch that marks the production version.
The essence is that work of team members (on the develop branch) can continue, while another person is preparing a quick production fix.

# AppVeyor

By connecting Appveyor with your Github account and giving it access to the project, it will generate a build for each commit that is made in the repository.

As this is not what we are looking for, we can configure Appveyor to do the builds only when a commit is made in some specific branches such as develop, releases, master and hotfix, making the QA team easier to work with.

![trunk](https://raw.githubusercontent.com/AlejandroParis/BranchingPoliciesResearch/master/images/appveyor.png)

# Sources

- [Azure Branching Policies](https://docs.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops)
- [Azure Pull Request](https://docs.microsoft.com/en-us/azure/devops/repos/git/pull-requests?view=azure-devops&tabs=new-nav#complete-the-pull-request)
- [GitHub Branches](https://help.github.com/en/articles/about-protected-branches)
- [DevOpsNet](https://devopsnet.com/2012/11/01/exciting-branching/)
- [Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)
- [IT Hare](http://ithare.com/version-control-branching-for-gamedev/)
- [Git Branching](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows)
- [AppVeyor](https://www.appveyor.com/docs/branches/)

# Contact

paris.alejandro1@gmail.com
