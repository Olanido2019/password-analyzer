# Password Strength Analyzer 

**Author:** Olanido (Razzyerasmus2019)  
**Project Type:** Cybersecurity Tool  
**Language:** Python  
**Environment:** Kali Linux / Linux  

---

##  Project Overview

The **Password Strength Analyzer** is a Python-based cybersecurity tool that evaluates the strength of a password and provides feedback on how secure it is.

The tool uses the **zxcvbn password strength estimation algorithm** along with entropy calculations to determine how resistant a password is against brute-force and dictionary attacks.

This project helps demonstrate core cybersecurity concepts such as:

- Password entropy
- Password cracking resistance
- Secure password design
- Defensive security practices

---

##  Features

- Password strength scoring using **zxcvbn**
- Entropy calculation
- Color-coded feedback in the terminal
- Weak / Moderate / Strong password classification
- Simple command-line interface

---

##  Technologies Used

- Python 3
- zxcvbn-python
- colorama
- Linux / Kali Linux
- Git & GitHub

---

##  Project Structure

```
password-analyzer/
│
├── analyzer.py
├── requirements.txt
└── README.md
```

---

##  Installation

Clone the repository:

```
git clone https://github.com/Olanido2019/password-analyzer.git
```

Move into the project directory:

```
cd password-analyzer
```

Create a virtual environment:

```
python3 -m venv .venv
```

Activate the virtual environment:

```
source .venv/bin/activate
```

Install dependencies:

```
pip install -r requirements.txt
```

---

##  Running the Tool

Run the analyzer:

```
python3 analyzer.py
```

Example:

```
Enter password to analyze: password123

Analyzing password...

zxcvbn score: 1/4
Entropy estimate: 35 bits
Feedback: Add symbols and uppercase letters

Weak password!
```

---

##  Cybersecurity Concepts Demonstrated

This project demonstrates several security concepts:

- Password entropy calculation
- Password strength estimation
- Defense against brute-force attacks
- Secure password recommendations

These concepts are widely used in authentication systems and password policy enforcement.

---

##  Future Improvements

Possible improvements include:

- Password dictionary attack simulator
- Password hash cracking demonstration
- Password policy enforcement module
- GUI interface for easier usability
- Logging and reporting features

---

##  Learning Outcome

This project was built as part of a cybersecurity lab to better understand:

- How password strength is evaluated
- How attackers attempt to crack passwords
- How developers can build tools to improve security

---

##  License

This project is for **educational and cybersecurity learning purposes**.
