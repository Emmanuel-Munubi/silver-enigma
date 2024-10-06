---

# **My Django Backend Development Journey**

Welcome to my personal Django project, where I’m developing backend features step-by-step, implementing one new feature each day. The purpose of this repository is to track my learning journey and provide a resource for others interested in backend development with Django and MySQL.

## **Project Overview**

This project is structured around learning key backend development concepts using **Django** as the web framework and **MySQL** as the database. The development process follows a feature-based approach, allowing for daily progress, with each feature designed to be implemented within a day.

### **Technologies Used**

- **Django** - Web Framework
- **MySQL** - Relational Database
- **Django REST Framework** - API Development
- **Redis** - Caching & Task Queuing
- **Celery** - Background Jobs
- **AWS S3** - Cloud File Storage
- **Docker** - Containerization (optional)

---

## **Getting Started**

### **Prerequisites**

Ensure you have the following installed on your local machine:

- **Python 3.8+**
- **Django 4.x**
- **MySQL** (local instance or cloud-hosted)
- **Pipenv** (optional for virtual environment management)
- **Redis** (for caching and Celery)
- **Docker** (for containerization, if needed)

### **Installation Steps**

1. **Clone the Repository**
    ```bash
    git clone https://github.com/Emmanuel-Munubi/silver-enigma.git
    cd silver-enigma
    ```

2. **Set Up Virtual Environment and Install Dependencies**
   If you’re using **Pipenv**, you can set up the virtual environment as follows:
    ```bash
    pipenv install
    pipenv shell
    ```

    Otherwise, create a virtual environment and install dependencies manually:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3. **Set Up MySQL Database**
    - Install MySQL and create a new database:
      ```bash
      mysql -u root -p
      CREATE DATABASE my_django_project;
      ```
    - Update the `DATABASES` section in `settings.py` to connect to your MySQL instance:
      ```python
      DATABASES = {
          'default': {
              'ENGINE': 'django.db.backends.mysql',
              'NAME': 'my_django_project',
              'USER': 'root',
              'PASSWORD': 'your_password',
              'HOST': 'localhost',
              'PORT': '3306',
          }
      }
      ```

4. **Run Migrations**
    Apply migrations to set up the initial database structure:
    ```bash
    python manage.py migrate
    ```

5. **Create a Superuser**
    To access the Django admin panel, create a superuser:
    ```bash
    python manage.py createsuperuser
    ```

6. **Start the Development Server**
    Run the Django development server:
    ```bash
    python manage.py runserver
    ```

7. **Access the Project**
    - Open your browser and go to `http://127.0.0.1:8000/` to see the homepage.
    - Admin panel: `http://127.0.0.1:8000/admin/`

---

## **Features**

This project follows a structured **daily feature implementation** plan, progressing from foundational to advanced backend development topics.

### **Daily Feature Implementation**

- **Phase 1: Foundational Skills**
    - [ ] Set up Django project
    - [ ] Configure MySQL database
    - [ ] Create custom user model
    - [ ] Implement basic user registration and login
    - [ ] Add basic CRUD operations for a model
    - [ ] Add file upload functionality

- **Phase 2: Intermediate Skills**
    - [ ] Set up Redis caching
    - [ ] Implement token-based authentication
    - [ ] Implement background jobs using Celery
    - [ ] Add email notification on user registration

- **Phase 3: Advanced Skills**
    - [ ] Dockerize the Django app
    - [ ] Implement auto-scaling on AWS

For a detailed breakdown of features and progress, refer to the **Issues** section in this repository.

---

## **Project Structure**

```plaintext
.
├── my_project/           # Main Django project directory
│   ├── settings.py       # Django settings (updated for MySQL)
│   ├── urls.py           # Project URLs
│   └── wsgi.py           # WSGI entry point
├── app/                  # Example Django app directory
│   ├── models.py         # Application models
│   ├── views.py          # Application views
│   ├── urls.py           # Application-specific URLs
│   └── serializers.py    # API serializers (for Django REST Framework)
├── requirements.txt      # List of dependencies
└── README.md             # Project readme (this file)
```

---

## **Contributing**

Contributions are welcome! To contribute to this project:

1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m "Add new feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

---

## **Contact**

If you have any questions or suggestions, feel free to open an issue or contact me at [your-email@example.com](mailto:your-email@example.com).

---

## **License**

This project is licensed under the MIT License.

---

By following this `README.md`, anyone can quickly understand the project's purpose, set up the environment, and get involved in contributing or following along with your development progress.
