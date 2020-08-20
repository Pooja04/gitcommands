commit m1 11:00
commit f1 11:01
commit m2 11:02

git log master
commit m2 11:02
commit m1 11:00

git log feature
commit f1 11:01
commit m1 11:00


git merge master (in feature branch)

git log feature
merge branch
commit m2 11:02
commit f1 11:01
commit m1 11:00


commit m3 11:03 from UI

git merge master (in feature branch) - no updates of commit m3 since changes not present in local

git log feature (same as above no changes)
merge branch
commit m2 11:02
commit f1 11:01
commit m1 11:00

git pull origin master (in feature branch)

git log feature (commit taken form UI, see m3 is displayed below)
merge branch
commit m3 11:03
merge branch
commit m2 11:02
commit f1 11:01
commit m1 11:00

git pull origin master (in master branch, just to update master)

git log master
commit m3 11:03
commit m2 11:02
commit m1 11:00


commit m4 11:04 (not pushed)

commit m5 11:05 (added from UI)

// scenario 1
git pull origin master (in feature branch)

git log feature (commit taken form UI only, not the local one which is not pushed, see below m4 is missing)
merge branch
commit m5 11:05
merge branch
commit m3 11:03
merge branch
commit m2 11:02
commit f1 11:01
commit m1 11:00

// scenario 2
git merge master (in feature branch)

git log feature (commit not taken form UI, taken from the local one which is not pushed, see below m5 is missing)
merge branch
commit m4 11:04
merge branch
commit m3 11:03
merge branch
commit m2 11:02
commit f1 11:01
commit m1 11:00
