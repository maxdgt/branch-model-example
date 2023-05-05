** DOCUMENTATION **

- https://semver.org/
- https://github.com/symfony/symfony

[master] (production)

[dev] (testing/qa)

[release/**] (release branches)

** new feature or bugfix ** 

IB-2023 from master
Ib-2024 from master

** remote testing on dev ** 

merge into dev

** local testing **

IB-2023 (local branch)
git fetch 
git merge IB-2024

** deploy to production **

[release/1.0] new branch from master
 merge IB-2023 finished
 merge IB-2024 fisished

merge into master

===========================================================================


git clone git@github.com:maxdgt/new-modelbranch.git

touch README.md
git add README.md
git commit -m "Initial commit"
git push -u origin main

git checkout -b dev
git push origin dev

git checkout main
git pull
git checkout -b IB-2023

touch index.html
git add index.hmtl
git commit -m "adding index.html file"
git push origin IB-2023

git checkout main
git checkout -b IB-2024

touch main.js
git add main.js
git commit -m "adding scripting"
git push origin IB-2024

git checkout main
git pull

## Release to dev

git checkout dev
 > git merge IB-2023 (PR)
 > git merge IB-2024 (PR)

## Release to staging

git checkout -b 1.0
git push origin 1.0
 > git merge IB-2023 (PR)
 > git merge IB-2024 (PR)


git checkout main
 > git merge 1.0 (PR)

generate tag/release v1.0

## Relese to production

- Manually from main

**A Release is created from an existing tag and exposes release notes and links to download the software or source code from GitHub.**

