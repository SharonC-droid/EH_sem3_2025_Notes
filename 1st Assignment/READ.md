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

![image alt](https://github.com/SharonC-droid/EH_sem3_2025_Notes/blob/ab411092fd2d99eda35fc8536e4149b83458588c/Screenshot%202025-07-31%20224633.png)

# 🔍 Explanation of Octal File Permissions in Linux

In Linux, file permissions determine who can **read**, **write**, or **execute** a file. These permissions are assigned to **three categories** of users:

- **Owner**: The creator or assigned owner of the file.
- **Group**: Other users in the file's group.
- **Others**: All other users on the system.

---

## 🧮 Octal (Numeric) Notation

Permissions are represented using octal (base-8) numbers. Each digit corresponds to a set of permissions for one category:

| Permission Type | Symbol | Binary | Octal |
|-----------------|--------|--------|-------|
| Read            | `r`    | 100    | 4     |
| Write           | `w`    | 010    | 2     |
| Execute         | `x`    | 001    | 1     |

The digits are **added** to get full permission:

- `rwx` → 4 + 2 + 1 = **7**
- `r-x` → 4 + 0 + 1 = **5**
- `--x` → 0 + 0 + 1 = **1**

---

## 🔢 Example: `751` Permission Breakdown

| User Type | Octal Value | Binary | Permissions | Symbol |
|-----------|-------------|--------|-------------|--------|
| Owner     | 7           | 111    | rwx         | ✅ Full access |
| Group     | 5           | 101    | r-x         | ✅ Read and execute |
| Others    | 1           | 001    | --x         | ✅ Execute only |

The permission string shown by `ls -l` for a file with `751` would look like:

```bash
-rwxr-x--x

