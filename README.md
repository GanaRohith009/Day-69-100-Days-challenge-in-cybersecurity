# Day-69-100-Days-challenge-in-cybersecurity
## Day 69: Command Injection Exploration 🛡️

### 📝 Overview
Today's study focused on **Command Injection** vulnerabilities, where improper input handling allows attackers to execute system-level commands on the host server.

### 🔍 Key Concepts
* **Vulnerability Origin:** Occurs when applications pass untrusted user input directly to OS shell commands (e.g., `system()`, `exec()`).
* **Command Chaining:** Explored how attackers use special characters to execute multiple commands:
    * `;` (Semicolon) - Sequential execution.
    * `&&` (Logical AND) - Executes if the previous command succeeds.
    * `|` (Pipe) - Passes output to another command.
* **Payload Examples:**
    * `8.8.8.8; cat /etc/passwd`
    * `127.0.0.1 && whoami`

### 🛡️ Prevention Strategies
1.  **Input Validation & Whitelisting:** Strictly define allowed input formats (e.g., regex for IPs).
2.  **Avoid System Calls:** Use built-in language APIs (e.g., `os.mkdir()` instead of `system("mkdir ...")`) to bypass the shell entirely.
3.  **Principle of Least Privilege:** Run the web server as a non-privileged user (e.g., `www-data`) to limit the impact of a successful breach.

### 🖼️ Visual Breakdown
![Command Injection Infographic](path/to/your/image.png)

---
*Part of my #100DaysOfCode journey into Cyber Security.*
