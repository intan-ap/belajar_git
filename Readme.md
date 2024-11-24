# STEPS

# Awal
1. git init
2. git status (masih master)
3. git branch
4. git config user.name <username-github>
5. git config user.email <email-github>
6. git status (sudah main)
7. git branch

# Create New File
1. create new file
2. git status
3. git branch
4. git add . >>> buat mengambil semua file. Tapi apabila cuma file tertentu, tambahkan nama filenya
5. git commit -m <"adding new file (commit message)">
6. git branch -M main
7. git log
8. git status
9. git branch
10. git checkout -b add/file
11. git status (di branch add/file)
12. git branch

# Add New File
1. create new file
2. git status
3. git branch
4. git add <nama file>
5. git commit -m <"adding new file (commit message)">
6. git log
7. git status
8. git branch
9. git checkout main (di branch main)
10. git checkout add/file (di branch add/file)

# Modify File dan membuat branch manual tanpa -b
1. modify file content
2. git checkout main (di branch main)
3. git status
4. git branch fix/parameter (membuat branch baru)
5. git branch (masih di branch main)
6. git status
7. git checkout fix/parameter
8. git status (sudah di branch fix/parameter)
9. git add .
10. git status
11. git log

# Karena main tertinggal dengan branch add/file, kita perlu merge main dengan branch add/file
1. git checkout main
2. git merge add/file
3. git checkout -b add/file (akan eror karena udah di merge ke main)

# Terjadi Konflik
1. git checkout -b feat/parameter_c
2. git status
3. File di modif
4. git status
5. git add .
6. git status
7. git commit -m "adding parameter c to div func"
8. git log --oneline
9. git status
10. git checkout main
11. git checkout -b feat/parameter_d
12. git status
13. File di modif
14. git status
15. git stash
16. git status
17. git merge add/file feat/parameter_c
18. git stash pop
19. Ke file nya lalu pilih current change
20. git status
21. git add .
22. git status (udah solved)

# Remote
1. Create new repository in github
2. git remote add origin https://github.com/intan-ap/belajar_git.git
3. git remote -v
4. git push -u origin main

# Push ke Remote Repository
1. git status
2. git checkout main
3. Lakukan perubahan di file sub
4. git status
5. git diff <nama file> (untuk melihat perubahannya)
6. git status
7. git stash
8. git status (kalau di stash, yang kesimpen cuma yang di modify)
9. git checkout -b feat/parameter_sub
10. git stash pop >>> balikin saved index ke working directory
11. git add .
12. git status
13. git commit -m "Adding parameter c and readme"
14. git log
15. git push origin feat/parameter_sub
16. Klik compare & request di github
17. Create pull request di github
18. Merge pull request di github
19.