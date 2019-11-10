## Roll back changes

1. Go to a folder with cloned repo (or clone repo like it was described in step2). Make some changes in `hello_world.py`.
To de sure changes were made you can look at them with
```
git diff
diff --git a/hello_world.py b/hello_world.py
index 03e6b7a..6da49ac 100644
--- a/hello_world.py
+++ b/hello_world.py
@@ -1,6 +1,9 @@
def hello_world():
    print('Hello!')

+def hello_world2():
+    print('Hello to you to')

if __name__ == '__main__':
    hello_world()
+    hello_world2()
```
The command shows difference only in not-staged files, if you want to compare already staged files try:
```
git diff --staged
```
2. If you want to remove file from stage you have to run:
```
git reset hello_world.py
```
3. Commit changes. (like it was described in step3)
You can check, that commit is ok with:
```
git log
```
Output should look like
```
commit dad1040af5e6096aefa1667e3566b9d9a7fbeecf (HEAD -> add-text-file)
Author: Olga <tomasmor42@gmail.com>
Date:   Sun Nov 10 20:38:18 2019 +0100

    Some changes

commit 41ca8c685082cae1f681992ad2c9bcff93838edb (origin/add-text-file)
Author: Olga <tomasmor42@gmail.com>
Date:   Sun Nov 10 13:20:22 2019 +0100

    Add hello_world file

commit 09b8cbf8c194d5d592c34fdf06165c777234b9fc (origin/master, origin/HEAD, master)
Author: tomasmor42 <42064734+tomasmor42@users.noreply.github.com>
Date:   Sun Nov 10 10:45:05 2019 +0100

    Initial commit
```
4. You can revert the last commit with command:
```
git revert dad1040af5e6096aefa1667e3566b9d9a7fbeecf
```
where long string is a hash of last commit (you can see it in `git log` output)
This log creates an additional commit that reverts repo to the state before the last commit. You can see it in a `git log`
