# 🔐 File Permissions & `chmod` Task

This project demonstrates how to understand file permissions in Unix/Linux systems, how to visualize them using a flowchart, and how to apply permission changes using both the **Linux terminal** and a **Python script**.

---

## 📘 Understanding File Permissions

In Unix-like systems, file permissions determine who can:
- **Read** a file (`r`)
- **Write** to a file (`w`)
- **Execute** a file (`x`)

Permissions are grouped into three categories:
- **Owner** (User)
- **Group**
- **Others**

Example permission: `rwxrwxr-x`

| Section | Permissions | Meaning              |
|---------|-------------|----------------------|
| Owner   | rwx         | Read, Write, Execute |
| Group   | rwx         | Read, Write, Execute |
| Others  | r-x         | Read, Execute        |

---

## 🔄 Flowchart for File Permissions

           +-----------------------+
           | Start with a file     |
           +-----------------------+
                     |
                     v
         +--------------------------+
         | Who needs access?        |
         | (Owner, Group, Others)   |
         +--------------------------+
                     |
          +----------+----------+
          |                     |
      Owner               Group / Others
          |                     |
          v                     v
  +---------------+     +-----------------+
  | Read? Write?  |     | Read? Execute?  |
  | Execute?      |     +-----------------+
  +---------------+              |
          |                      v
          +---------------> Apply permissions
                                (e.g., chmod)

---

## 🖥️ Method 1: Using Linux Terminal (Ubuntu)

### Step-by-Step

1. **Open Terminal**:
   ```bash
   Ctrl + Alt + T
   ```
2. **Navigate to your file:**
   ```bash
   cd /path/to/your/file
   ```
3. **Check current permissions:**
   ```bash
   ls -l example.py
   ```
4. **Change permissions to rwxrwxr-x (775):**
   ```bash
   chmod 775 example.py
   ```
5. **Verify change:**
   ```bash
   ls -l example.py
   ```
###Expected output:###
-rwxrwxr-x 1 aleen aleen 1234 Aug 5 14:33 example.py
