mkdir Peteros_IT120_Act1
cd Peteros_IT120_Act1

touch Profile.txt Education.txt Background.txt Readme.txt Test.py

git init
git checkout -b main   # instead of 'master'
git add .
git commit -m "Initial commit with all files"

git checkout -b LastName_B1
# → Edit only the Profile.txt file
git add Profile.txt
git commit -m "Edited Profile.txt with personal info"

git checkout main
git checkout -b LastName_B2
# → Edit only the Education.txt file
git add Education.txt
git commit -m "Added educational background"

git checkout main
git checkout -b LastName_B3
# → Edit only Background.txt and delete Test.py
rm Test.py
git add Background.txt
git rm Test.py
git commit -m "Edited Background.txt and removed Test.py"

git checkout main
git checkout -b LastName_B4
# → Edit Readme.txt and delete Test.py (if it exists)
rm -f Test.py
git add Readme.txt
git rm -f Test.py 2>/dev/null  # suppress error if already deleted
git commit -m "Added Git commands in Readme.txt and removed Test.py"
