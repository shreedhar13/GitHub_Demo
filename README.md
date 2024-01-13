# GitHub_Demo
My first github demo
<br>
author -> shreedhar jagatap
<br>
NOTE->in our laptop we call folder or directory,,,but when you create folder on github it is called repository(repo) and these are available on github web so we can also call it s REMOTE REPO<br>
1.I first cloned the github repository from my github account ,link->https://github.com/shreedhar13/GitHub_Demo.git<br>
2.and i cloned it in my local folder named GITHUB_DESKTOP using "git clone link"command on vs code terminal<br>
3.now i get like this,,,,C:\Users\shree\Desktop\GITHUB_DESKTOP\GitHub_Demo<br>
4.inside GitHub_Demo there is file named README.MD ,,,(MD->mark down)<br>
5.i created the new file index.html in C:\Users\shree\Desktop\GITHUB_DESKTOP\GitHub_Demo this folder<br>
6.i entered "git status" to check what modification i have done ,,,,<br>
7.if any modification is done then in terminal it is diplayed in red color....<br>
8.untracked ->new files that git doesnt yet track,,modified->changed,,staged->file is ready to be commited,,unmodified->unchanged<br>
9.to replicate these changes in ur github account ,,2 stage process is followed,,1.add,2.commit<br>
10.add->now added file are become staged,,adds new or changed files in your working dir to the Git staging area using "git add 'file name' " command.if there are many modification ->"git add ."<br>
11.after "git add .",,,all modification displayed in green color,,ie;file is at staged state
12.commit-> git commit -m "some message or comments for this modification so that it can help at the time of tracking history of modification"<br>
13.but these changes tracked at local system ie;in "Git" (which is present at local side).....ie;for every github repository there is a .git file,which keep track of each file/folder inside this repository<br>
14.to push it to github ,use -> "git push origin main",,,which push the changes which are done locally(ie;whatever changes u have done in repository it will tracked by .git file which is managed by Git application at local side) to remote(github website/your github account)
'origin'->currently working repo on github is called origin
'main'->is our branch on currently working github repo,,there can be many bracnhes<br>
15.push->upload local repo content to remote repo,,,,local repo managed  by Git application what u installed .<br>
16.after executing this command ,,,if it is first time push then u have to autohorize the github with ur account<br>
17.now visit the github ,refresh the page u see the chnages u have done in locally<br>

18.if u want to create github repo from your local side,,,then use "git init" command<br>
19.i have created "GitHub_Demo" repo on github itself and then i pulled it to my local side,,but if i want to create repo from my side then foloow these step
20..create folders and files at ur local side,,i have created 'localrepo' named folder in GITHUB_DESKTOP folder<br>
21.mkdir localrepo or bu clicking folder icon u can create<br>
22.but this localrepo is normal folder (when u see ls -a,then it is not showing .git file which tracks the changes,,thus),,,,but we have to track the changes and upload on github sooo make this folder as github repository by using "git init" ,which creates .git file using local side Git application(which we installed),now if u see 'ls -a" then u see (. .. .git)hidden files,,where .git is local side git file which tracks the activity and this only is uploaded/pushed on Github website/our github account.....
thus now localrepo folder become git repo bcz it has now .git file in it<br>
23.now u can do anything inside it(create file,folder..etc) and after ur work is complete then u can push it to ur github account<br>
24.but u cant use direct push option  as u did when u cloned the repo..bcz u created repo from ur local side so there is some steps to be followed to push this repo on github account<br>
25.first->create one repo on github account with "any name",,i choose "LocalRepo" to maintain redability...
   second->exec "git remote add origin link_of_created_LocalRepo",,u can give any diff name instead origin,,,then u have to use "git push given_name main" ,,but keep it simple we use orgin itself
   third->change branch name master to main,,bcz github has changed bydefault branch from master to main so....see apna college for more info
   fourth->now use git push origin main,,,,,but if u are working on localrepo for more time in day,,,then u have to write git push origin main every time when u change something,,,,instead we use git push -u origin main   ,thus from next time onwards u can just write "git push" it willautomatically push the changes in origin and in main branch of origin present on ut github account
   DONE....ur index.html and style.css is pushed on origin(ie;current working repo is LocalRepo bcz we placed origin link https://github.com/shreedhar13/LocalRepo.git)
   and inside "main" named branch<br>
26.now i created README.md  inside localrepo from our local side
27.Thats why create repo on Github and clone it in ut local side ,,then u can create any no of files folders i that,,and finally push it,,,which is easy workflow<br>

# want to create more than 1 branches in ur origin(currently working github repo),,,,,,,why origin see video<br>
ie;within main branch there are mainy teams who are worj=king on diff diff task,,like front end developer,back end,ui/ux designer,app designer..etc features,,,in that case u can create branch for each team,,,where each team take a copy of main branch and work on it and finally that team merge there changes into main branch to form complete product<br>

28.i have created 2 features,,,1 branch is bydefault there with name 'main'  if u created repo on github
  else with name 'master' branch is created  when u create repo on ur local side as we discussed above...
  thus total 3 branches main,feature1,feature2  in 'localrepo(local folder)' and reflect changes in 'Localrepo(github repo)'  u can give any name for branches<br>
  'git branch' to check all branches present in origin or current working repo
  'git checkout -b feature1' to create new branch named feature 1 and switched to feature1 from current working branch<br>

  to delete branch 'git branch -d branch_name'
  i hava deleted feature2 'git branch -d feature2' ,,,,note:feature2 is deleted only when ur out of this branch,,,ie;if u are in feature2 branch and u try to delete feature2 itself then error is shown,,so come out of that branch and then delete it....
  git checkout main ->jump to or switched to main branch from current branch<br>

  but this created branch info is not yet reflected at github....<br>

29.i switched in feature1(bcz i have created feature1 branch inside localrepo and localrepo's "main"(bydefault) branch has 3 files(index.html,README.md,style.css),feature1 also has exactly these 3 files ie;1copy of main branch is assigned in feature1 branch,,,,and when i created feature2 brach inside local repo then also 1copy of main branch is assigned to feature2 but we deletd feature2 branch,so copy also deleted.... )<br>
30.now u can change anything inside this "copy of main branch"add and commit it ,,, which not reflect in main branch and what u cahnge in "main" branch will not reflect in feature1 branch ,,(ie;shaloow copy bro..),,ie;any branch ,activity/modification will not reflect in other branches of current working repo/origin.... 
31.now reflect changes in github account use "git push origin feature1",,,,,if u do from main branch(git push origin main)(bydefault ur in main branch)then changes done in main only reflected in github account,,,if u do from feature1 branch then info of only feature1 is reflected in github account...now u see on ur github account feature1 name branch is instantiated
32.now if we want to merge the main branch and feature1 branch ie;whatever changes u have done in featue1 branch should combined with main branch then there are 2 ways....1)git merge branch_name  ,,(from current branch and branch_name)  2)create PR (pull request) from github account<br>
33.to check differences in 2 branches use git diff branch_name  ,,(from current branch and branch_name)
  supoose i am inside feature1 branch and i want to compare it with main branch then from inside feature1 branch we exec command     "git diff main"<br>
  PS C:\Users\shree\Desktop\GITHUB_DESKTOP\localrepo> git diff main<br>
diff --git a/index.html b/index.html<br>
index f10d021..43bf1c4 100644<br>
--- a/index.html<br>
+++ b/index.html<br>
@@ -1 +1,2 @@<br>
-<p>hello this is my local file,created from my side</p> ->main branch index.html<br>
\ No newline at end of file<br>
+<p>hello this is my local file,created from my side</p><br>  
+<h1,style="display:inline;">line 2 of feature2</h1>->feature1 branch index.html<br>
\ No newline at end of file<br>