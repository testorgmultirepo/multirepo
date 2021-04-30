# multirepo/monorepo

git version 2.31.1(Please check your Git version. It should be > 2.20(Q2 2020)


```javascript
git clone https://github.com/testorgmultirepo/multirepo.git multirepo
cd multirepo
git remote add origin https://github.com/testorgmultirepo/multirepo.git
git branch -M main
git push -u origin main
```

```javascript
mkdir repo1 && mkdir repo2
git push

git config core.sparsecheckout true
echo repo1/ >> .git/info/sparse-checkout
echo repo2/ >> .git/info/sparse-checkout

git push

mkdir test_multirepo && cd test_multirepo/
```

`git clone \\n  --depth 1 \\n  --filter=blob:none \\n  --no-checkout \\n  https://github.com/testorgmultirepo/multirepo.git \\n;`

`cd multirepo`

`git checkout main -- repo1` // pull only repo1

**WE GET THE HISTORY ONLY FOR REPO1:**

COMMIT 4D31ED0B1734F24CDB6F529176F00F5EFBA72A85 (GRAFTED, HEAD -> MAIN, ORIGIN/MAIN, ORIGIN/HEAD)
AUTHOR: PULPIKS <PULPIKS@YANDEX.RU>
DATE:   FRI APR 30 15:41:06 2021 +0200

SDFDSF
(END)

**Full History Of Commits in the multirepo In Github:**

SDFDSF --->>> ONLY THIS COMMIT WILL BE PICKED UP IN THE HISTORY WHILE PULLING REPO1

@PULPIKS
PULPIKS COMMITTED 15 MINUTES AGO
 
SDFDF

@PULPIKS
PULPIKS COMMITTED 38 MINUTES AGO
 
WIP

@PULPIKS
PULPIKS COMMITTED 1 HOUR AGO
 

