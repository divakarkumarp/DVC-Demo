# DVC-Demo
Data Version Control is a free, open-source tool for data management, ML pipeline automation, and experiment management. This helps data science and machine learning teams manage large datasets, make projects reproducible, and collaborate better.

### Follow the to test DVC demo code 

```
E:\DVC-Demo>conda create -p venv python==3.12 -y

E:\DVC-Demo>conda activate venv/

(E:\DVC-Demo\venv) E:\DVC-Demo>git init

(E:\DVC-Demo\venv) E:\DVC-Demo>pip install dvc

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc init

(E:\DVC-Demo\venv) E:\DVC-Demo>git commit -m "dvc init"
[main 0f38aab] dvc init
 3 files changed, 6 insertions(+)
 create mode 100644 .dvc/.gitignore
 create mode 100644 .dvc/config
 create mode 100644 .dvcignore

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc add data/data.txt
100% Adding...|███████████████████████████████████████████████████████████████████████████████|1/1 [00:00,  7.48file/s]

To track the changes with git, run:

        git add 'data\.gitignore' 'data\data.txt.dvc'

To enable auto staging, run:

        dvc config core.autostage true

(E:\DVC-Demo\venv) E:\DVC-Demo>git add data/.gitignore

(E:\DVC-Demo\venv) E:\DVC-Demo>git branch
* main

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc add data/data.txt
100% Adding...|███████████████████████████████████████████████████████████████████████████████|1/1 [00:00, 12.45file/s]

To track the changes with git, run:

        git add 'data\data.txt.dvc'

To enable auto staging, run:

        dvc config core.autostage true

(E:\DVC-Demo\venv) E:\DVC-Demo>git add data/data.txt.dvc

(E:\DVC-Demo\venv) E:\DVC-Demo>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   data/.gitignore
        new file:   data/data.txt.dvc

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore


(E:\DVC-Demo\venv) E:\DVC-Demo>git commit -m "DVC"
[main a058ea9] DVC
 2 files changed, 6 insertions(+)
 create mode 100644 data/.gitignore
 create mode 100644 data/data.txt.dvc

(E:\DVC-Demo\venv) E:\DVC-Demo>git log
commit a058ea9249deee545b75a2b15ec9606bf0eb2262 (HEAD -> main)
Author: Divakar Kumar <divakarkumar424@gmail.com>
Date:   Wed May 22 22:02:59 2024 +0530

    DVC

commit 0f38aabc592b8769abf2edb2ba7a9f7254a15545
Author: Divakar Kumar <divakarkumar424@gmail.com>
Date:   Wed May 22 20:06:15 2024 +0530

    dvc init

commit ddef71cbdfe2e35a98464b0669c3a15c799bb102 (origin/main, origin/HEAD)
Author: Divakar Kumar <32620288+divakarkumarp@users.noreply.github.com>
Date:   Wed May 22 16:29:54 2024 +0530

    Initial commit

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc add data/data.txt
100% Adding...|███████████████████████████████████████████████████████████████████████████████|1/1 [00:00, 16.06file/s]

To track the changes with git, run:

        git add 'data\data.txt.dvc'

To enable auto staging, run:

        dvc config core.autostage true

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc add data/data.txt
100% Adding...|███████████████████████████████████████████████████████████████████████████████|1/1 [00:00, 10.08file/s]

To track the changes with git, run:

        git add 'data\data.txt.dvc'

To enable auto staging, run:

        dvc config core.autostage true

(E:\DVC-Demo\venv) E:\DVC-Demo>git add data/data.txt.dvc

(E:\DVC-Demo\venv) E:\DVC-Demo>git commit -m "3rd version"
[main 7ccf636] 3rd version
 1 file changed, 2 insertions(+), 2 deletions(-)

(E:\DVC-Demo\venv) E:\DVC-Demo>git log
commit 7ccf63616be397ecd9cfd397c4028cc4c75dcc7e (HEAD -> main)
Author: Divakar Kumar <divakarkumar424@gmail.com>
Date:   Wed May 22 22:07:34 2024 +0530

    3rd version

commit a058ea9249deee545b75a2b15ec9606bf0eb2262
Author: Divakar Kumar <divakarkumar424@gmail.com>
Date:   Wed May 22 22:02:59 2024 +0530

    DVC

commit 0f38aabc592b8769abf2edb2ba7a9f7254a15545
Author: Divakar Kumar <divakarkumar424@gmail.com>
Date:   Wed May 22 20:06:15 2024 +0530

    dvc init

commit ddef71cbdfe2e35a98464b0669c3a15c799bb102 (origin/main, origin/HEAD)
Author: Divakar Kumar <32620288+divakarkumarp@users.noreply.github.com>
Date:   Wed May 22 16:29:54 2024 +0530

    Initial commit

(E:\DVC-Demo\venv) E:\DVC-Demo>git checkout aadc123b37dc712028ebbe97d1f951a0
error: pathspec 'aadc123b37dc712028ebbe97d1f951a0' did not match any file(s) known to git

(E:\DVC-Demo\venv) E:\DVC-Demo>git checkout a058ea9249deee545b75a2b15ec9606bf0eb2262
Note: switching to 'a058ea9249deee545b75a2b15ec9606bf0eb2262'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at a058ea9 DVC

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc checkout
Building workspace index                                                                     |2.00 [00:00, 71.6entry/s]
Comparing indexes                                                                            |3.00 [00:00,  600entry/s]
Applying changes                                                                             |1.00 [00:00,   303file/s]
M       data\data.txt

(E:\DVC-Demo\venv) E:\DVC-Demo>git checkout main
Previous HEAD position was a058ea9 DVC
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

(E:\DVC-Demo\venv) E:\DVC-Demo>dvc checkout
Building workspace index                                                                     |2.00 [00:00,  117entry/s]
Comparing indexes                                                                            |3.00 [00:00,  601entry/s]
Applying changes                                                                             |1.00 [00:00,   142file/s]
M       data\data.txt

```