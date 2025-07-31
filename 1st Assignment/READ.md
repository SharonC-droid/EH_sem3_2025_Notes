# Assignment 5: File Creation and Permission

## 🎯 Objective
To create a file, set specific permissions using octal notation `751`, and understand how Linux file permission management works using `chmod` and `ls -l`.

---

## 🧪 Methodology

1. Created a file using the `touch` command.
2. Changed its permissions using the `chmod` command with octal notation `751`.
3. Verified the updated permissions using the `ls -l` command.
4. Analyzed and explained what each digit in `751` represents.
5. Captured terminal screenshots as evidence of the steps.

---

## 💻 Commands Used

```bash
# Step 1: Create an empty file
touch samplefile.txt

# Step 2: Change permissions to 751
chmod 751 samplefile.txt

# Step 3: View file permissions
ls -l samplefile.txt

