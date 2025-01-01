 ## 🌟**Bluestock Fintech IPO Web Application & REST API**  
![company logo](https://github.com/Dahire100/Bluestock-SDE-intern/blob/main/logo.jpeg)

Welcome to the Bluestock IPO Web Application & REST API project! This platform is designed to provide users with comprehensive IPO-related details and robust API integrations for client applications.  

---

## 👥 **Team Members**  
- 🏆 **Vedant Santosh Deshpande** (Team Lead)  
- ⭐ **Aarti** (Co-Team Lead)  
- 💻 **Devendra Ratan Ahire**  
- 🔧 **Ayush Maheshwari**  
- 🖥️ **Divyansh Singh Tomar**
- 🖥️ **Divya**  

---

## 🚀 **How to Run the Project**  

Follow these steps to set up and run the project locally:  

### 1️⃣ Clone the Repository  
```bash  
git clone https://github.com/Vijayvarma115/bluestock-ipo-webapp.git  
```  

### 2️⃣ Navigate to the Project Directory  
```bash  
cd bluestock-ipo-webapp  
```  

### 3️⃣ Install Dependencies  
```bash  
pip3 install -r requirements.txt  
```  

### 4️⃣ Apply Migrations and Create Superuser  
- **Make migrations:**  
  ```bash  
  python3 manage.py makemigrations  
  ```  
- **Migrate the database:**  
  ```bash  
  python3 manage.py migrate  
  ```  
- **Create a superuser:**  
  ```bash  
  python3 manage.py createsuperuser  
  ```  

### 5️⃣ Run the Server  
```bash  
python3 manage.py runserver  
```  

---

## 🔗 **Connecting Django to PostgreSQL**  

### 🛠️ Step 1: Install PostgreSQL  
Download and install PostgreSQL from the [official website](https://www.postgresql.org/).  

### 🗂️ Step 2: Create Database and User  
Run the following commands in the PostgreSQL command-line interface (psql):  
```sql  
CREATE DATABASE bluestock;  
CREATE USER devendra WITH PASSWORD 'dev@123';  
ALTER ROLE devendra SET client_encoding TO 'utf8';  
ALTER ROLE devendra SET default_transaction_isolation TO 'read committed';  
ALTER ROLE devendra SET timezone TO 'UTC';  
GRANT ALL PRIVILEGES ON DATABASE bluestock TO devendra;  
```  

### ⚙️ Step 3: Install PostgreSQL Adapter for Python  
```bash  
pip install psycopg2-binary  
```  

### 📜 Step 4: Update `settings.py` in Django  
Add the following configuration to the `DATABASES` section in your `settings.py` file:  
```python  
DATABASES = {  
    'default': {  
        'ENGINE': 'django.db.backends.postgresql',  
        'NAME': 'bluestock',  
        'USER': 'devendra',  
        'PASSWORD': 'dev@123',  
        'HOST': 'localhost',  
        'PORT': '5432',  
    }  
}  
```  

---

## 📽️ **References**  

🎥 **Video Tutorial:**  
[How to Connect Django with PostgreSQL](https://drive.google.com/file/d/1jUYqTqp_CTMRYu6FKNIT5327IPQh0fYk/view?usp=sharing)  

---

### ✨ **Happy Coding!**  
This project is a production-level platform designed to ensure precision, security, and scalability for Bluestock Fintech's IPO services. If you encounter issues or have suggestions, feel free to contribute or contact the team. 🌐  

