echo "main" > conflict_test.txt
$ git add conflict_test.txt
$ git commit -m "main branch commit"
$ git checkout -b feature
$ echo "feature branch" > conflict_test.txt
$ git add conflict_test.txt
$ git commit -m "feature branch commit"
$ git checkout main
$ git checkout master
$ echo "master branch" > conflict_test.txt
$ git add conflict_test.txt
$ git commit -m "master conflict commit"
$ git checkout feature
$ git rebase master
$ echo "해결 하기" > conflict_test.txt
$ git add conflict_test.txt
$ git rebase --continue

