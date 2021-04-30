# multirepo
test if multirepo works


git clone https://github.com/testorgmultirepo/multirepo.git multirepo
cd multirepo
git remote add origin https://github.com/testorgmultirepo/multirepo.git
git branch -M main
git push -u origin main

mkdir repo1 && mkdir repo2
git push

git config core.sparsecheckout true
echo repo1/ >> .git/info/sparse-checkout
echo repo2/ >> .git/info/sparse-checkout

git push

mkdir test_multirepo && cd test_multirepo/

git clone \\n  --depth 1 \\n  --filter=blob:none \\n  --no-checkout \\n  https://github.com/testorgmultirepo/multirepo.git \\n;
cd multirepo
git checkout main -- repo1 // pull only repo1

we get the history only for repo1:
commit 4d31ed0b1734f24cdb6f529176f00f5efba72a85 (grafted, HEAD -> main, origin/main, origin/HEAD)
Author: pulpiks <pulpiks@yandex.ru>
Date:   Fri Apr 30 15:41:06 2021 +0200

    sdfdsf
(END)

The full history of commits in Github:

sdfdsf --->>> only this commit will be picked up in the history while pulling repo1

@pulpiks
pulpiks committed 15 minutes ago
 
sdfdf

@pulpiks
pulpiks committed 38 minutes ago
 
wip

@pulpiks
pulpiks committed 1 hour ago
 

