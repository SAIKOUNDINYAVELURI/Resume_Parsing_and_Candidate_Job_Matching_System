# Resume_Parsing_and_Candidate_Job_Matching_System

🚀 A powerful NLP-based tool that parses resumes, recommends improvements, matches candidates to relevant job roles, and provides admin-level analytics. Ideal for job seekers, colleges, and organizations aiming to streamline recruitment and gain actionable insights.

---

## 🎯 Scope

i. 🔍 Extract structured resume data into **tabular and CSV format** for analytical use by organizations.

ii. 🤖 Provide **personalized recommendations**, **predicted job roles**, and an **overall resume score** to help users improve and re-test resumes.

iii. 🌐 Attract more users through the **interactive client section** with resume tips and improvement suggestions.

iv. 🎓 Empower colleges to **analyze students’ resumes before placements**, identifying gaps and trends.

v. 📊 Gain **insights into most-searched job roles** and user preferences through analytics.

vi. 💬 Gather **user feedback** to continually enhance the tool's features and experience.

---

## 🛠️ Tech Stack

### Frontend
- **Streamlit** (for interactive UI)

### Backend
- **Python** (NLP logic, resume parsing)
- **PyMySQL** (for DB connection)

### Database
- **MySQL**

### Libraries & Modules
- **spaCy**
- **PyMuPDF / PDFMiner**
- **pymysql**
- **pyresparser** (customized)
- **geopy**, **nltk**, **re**, etc.

---

## ✨ Features

### 👤 Client-Side
- Upload and parse resume
- Extract:
  - Name, Email, Phone, Location
  - Skills
  - Keywords
- Recommendations:
  - Skills to add
  - Courses and certifications
  - Resume tips
  - Predicted job role
  - Overall resume score
  - Interview prep videos
- Feedback form with rating and comment history

### 🔐 Admin-Side
- View all uploaded resumes
- Download user data as CSV
- Dashboard with:
  - Pie charts for user demographics & analytics
  - Resume score distribution
  - Popular job roles
  - User ratings & feedback
- Manage uploaded files and resume reports

---

## 📋 Requirements

Make sure the following are installed on your machine:

- [Python (3.9.12)](https://www.python.org/downloads/release/python-3912/)
- [MySQL](https://www.mysql.com/downloads/)
- [Visual Studio Code](https://code.visualstudio.com/Download)
- [Visual Studio Build Tools](https://aka.ms/vs/17/release/vs_BuildTools.exe)

---

## ⚙️ Setup & Installation

Follow the steps to set up the project locally:

1. **Clone the repo**  
   ```
 [  git clone https://github.com/your-username/Resume-Parsing-and-Matching-System.git](https://github.com/SAIKOUNDINYAVELURI/Resume_Parsing_and_Candidate_Job_Matching_System.git)
   ```

2. **Create virtual environment**
   ```
   python -m venv venvapp
   cd venvapp/Scripts
   activate
   ```

3. **Install dependencies**
   ```
   cd ../../App
   pip install -r requirements.txt
   python -m spacy download en_core_web_sm
   ```

4. **Setup MySQL Database**
   - Create a new database named: `cv`
   - Update DB credentials in `App.py` (Line 95):
     ```python
     connection = pymysql.connect(host='localhost', user='root', password='yourpassword', db='cv')
     ```

5. **Replace `resume_parser.py`**
   - Go to: `venvapp/Lib/site-packages/pyresparser`
   - Replace the file `resume_parser.py` with the **custom one provided**

6. **Run the App**
   ```
   streamlit run App.py
   ```

---

## ⚠️ Known Issues

- **GeocoderUnavailable**: Caused by poor internet. Check connection if location data fails to load.

---

## 🧪 Usage

- Upload any resume (PDF format) via the UI.
- Test with the sample resume in `Uploaded_Resumes/`
- Login to admin using:
  ```
  username: admin
  password: admin123
  ```

---


