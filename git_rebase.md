commit m1 11:00
commit m2 11:01
commit f1 11:02
commit m3 11:03
commit f2 11:04

git log master
commit m3 11:03
commit m2 11:01
commit m1 11:00

git log feature
commit f2 11:04
commit f1 11:02
commit m2 11:01
commit m1 11:00


git rebase master (in feature branch)

git log feature
commit f2 11:04
commit f1 11:02
commit m3 11:03 (see even if it was created later it had become base to the feature branch)
commit m2 11:01
commit m1 11:00


commit m4 11:05


git rebase feature (in master branch)

git log feature
commit m4 11:05
commit f2 11:04
commit f1 11:02
commit m3 11:03
commit m2 11:01
commit m1 11:00
