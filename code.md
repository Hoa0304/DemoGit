
ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git log --oneline
29dbd3b (HEAD -> test, origin/test) Merge pull request #1 from Hoa0304/master
87dc54e fix issure
5e736d2 Hot fix issure 1
7d931b2 Hot fix issue
3bc996b (origin/testing, testing) demo

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git commit -m "Hoa commit"
On branch test
Your branch is up to date with 'origin/test'.

nothing to commit, working tree clean

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git push origin
Everything up-to-date

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git log --oneline
29dbd3b (HEAD -> test, origin/test) Merge pull request #1 from Hoa0304/master
87dc54e fix issure
5e736d2 Hot fix issure 1
7d931b2 Hot fix issue
3bc996b (origin/testing, testing) demo

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git rebase -i 7d931b2
[detached HEAD 5fe19b9] Hot fix issure 1
 Date: Thu Mar 16 12:33:15 2023 +0700
 1 file changed, 1 insertion(+)
 create mode 100644 index.txt
Successfully rebased and updated refs/heads/test.

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git log --oneline
5fe19b9 (HEAD -> test) Hot fix issure 1
7d931b2 Hot fix issue
3bc996b (origin/testing, testing) demo

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git push origin
To https://github.com/Hoa0304/DemoGit.git
 ! [rejected]        test -> test (non-fast-forward)
error: failed to push some refs to 'https://github.com/Hoa0304/DemoGit.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git push --force
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 308 bytes | 308.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Hoa0304/DemoGit.git
 + 29dbd3b...5fe19b9 test -> test (forced update)

ADMIN@MSI MINGW64 /d/GitHubb/DemoGit (test)
$ git log --oneline
5fe19b9 (HEAD -> test, origin/test) Hot fix issure 1
7d931b2 Hot fix issue
3bc996b (origin/testing, testing) demo
