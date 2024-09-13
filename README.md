# 08-indonesia-complete-blog-app
Membuat A COMPLETE BLOG APP Menggunakan Django 5
Github: https://github.com/gurnitha/08-indonesia-complete-blog-app


## 1. SETUP

#### 1. Lokasi proyek 

#### 2. Membuat remote repositori di Github 

#### 3. Mengklon repositori dari Github

#### 4. Git commit 

#### 5. Restrukturisasi file proyek dan membuat root direktori

        modified:   README.md

#### 6. Mendorong file proyek ke remote repositori di Github

#### 7. Membuat lingkungan virtual 

#### 8. Aktivasi dan deaktivasi lingkungan virtual

#### 9. Menginstal Django 

#### 10. Meng-upgrade pip 

#### 11. Contoh teknik pembuatan proyek Django


## 2. PROYEK DJANGO

#### 1. Memeriksa sub-perintah yang tersedia pada django-admin

        C:\Users\ING\Desktop\workspace\08-indonesia-complete-blog-app\src(main -> origin)
        (venv312511) λ django-admin

        Type 'django-admin help <subcommand>' for help on a specific subcommand.

        Available subcommands:

        [django]
            check
            compilemessages
            createcachetable
            dbshell
            diffsettings
            dumpdata
            flush
            inspectdb
            loaddata
            makemessages
            makemigrations
            migrate
            optimizemigration
            runserver
            sendtestemail
            shell
            showmigrations
            sqlflush
            sqlmigrate
            sqlsequencereset
            squashmigrations
            startapp
            startproject
            test
            testserver
        Note that only Django core commands are listed as settings are not properly configured (error: Requested setting INSTALLED_APPS, but settings are not configured. You must either define the environment variable DJANGO_SETTINGS_MODULE or call settings.configure() before accessing settings.).

#### 2. Memeriksa sub-perintah yang tersedia pada python-manage.py

        (venv312511) λ python manage.py

        Type 'manage.py help <subcommand>' for help on a specific subcommand.

        Available subcommands:

        [auth]
            changepassword
            createsuperuser

        [contenttypes]
            remove_stale_contenttypes

        [django]
            check
            compilemessages
            createcachetable
            dbshell
            diffsettings
            dumpdata
            flush
            inspectdb
            loaddata
            makemessages
            makemigrations
            migrate
            optimizemigration
            sendtestemail
            shell
            showmigrations
            sqlflush
            sqlmigrate
            sqlsequencereset
            squashmigrations
            startapp
            startproject
            test
            testserver

        [sessions]
            clearsessions

        [staticfiles]
            collectstatic
            findstatic
            runserver

#### 3. Menginisiasi Django proyek dengan nama config

        (venv312511) λ django-admin startproject config .

        modified:   README.md
        new file:   config/__init__.py
        new file:   config/asgi.py
        new file:   config/settings.py
        new file:   config/urls.py
        new file:   config/wsgi.py
        new file:   manage.py

        src
        ├── README.md
        ├── config
        │   ├── __init__.py
        │   ├── asgi.py
        │   ├── settings.py
        │   ├── urls.py
        │   └── wsgi.py
        └── manage.py

#### 4. Menjalankan development server

        (venv312511) λ ls
        config/  manage.py*  README.md

        C:\Users\ING\Desktop\workspace\08-indonesia-complete-blog-app\src(main -> origin)
        (venv312511) λ python manage.py runserver
        Watching for file changes with StatReloader
        Performing system checks...

        System check identified no issues (0 silenced).

        You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
        Run 'python manage.py migrate' to apply them.
        September 13, 2024 - 12:02:33
        Django version 5.1.1, using settings 'config.settings'
        Starting development server at http://127.0.0.1:8000/
        Quit the server with CTRL-BREAK.

        Note:

        1. Saat menjalankan server pada kali pertama, Django
        secara otomatis menghasilkan db.sqlite3 sebagai default database.

        2. Kita dapat menggunakannya tanpa melakukan apa pun.

#### 5. Mengaktifkan aplikasi bawaan Django

        (venv312511) λ python manage.py migrate
        Operations to perform:
          Apply all migrations: admin, auth, contenttypes, sessions
        Running migrations:
          Applying contenttypes.0001_initial... OK
          Applying auth.0001_initial... OK
          Applying admin.0001_initial... OK
          Applying admin.0002_logentry_remove_auto_add... OK
          Applying admin.0003_logentry_add_action_flag_choices... OK
          Applying contenttypes.0002_remove_content_type_name... OK
          Applying auth.0002_alter_permission_name_max_length... OK
          Applying auth.0003_alter_user_email_max_length... OK
          Applying auth.0004_alter_user_username_opts... OK
          Applying auth.0005_alter_user_last_login_null... OK
          Applying auth.0006_require_contenttypes_0002... OK
          Applying auth.0007_alter_validators_add_error_messages... OK
          Applying auth.0008_alter_user_username_max_length... OK
          Applying auth.0009_alter_user_last_name_max_length... OK
          Applying auth.0010_alter_group_name_max_length... OK
          Applying auth.0011_update_proxy_permissions... OK
          Applying auth.0012_alter_user_first_name_max_length... OK
          Applying sessions.0001_initial... OK

          Note:

          Perintah python manage.py migrate menghasilkan:

          1. Tabel-tabel di dalam database db.sqlite3
          2. Kita akan memeriksa tabel-tabel tersebut setelah
             mensetup postgres database yang akan kita gunakan 
             pada proyek ini. 
          3. Karena tabel-tabel telah dibuat, satu diantara mereka adalah tabel auth_user, maka kita bisa menggunakannya dengan membuat superuser.

#### 6. Membuat superuser

        (venv312511) λ python manage.py createsuperuser
        Username (leave blank to use 'ing'): superuser
        Email address: superuser@mail.com
        Password:
        Password (again):
        The password is too similar to the email address.
        Bypass password validation and create user anyway? [y/N]: y
        Superuser created successfully.

#### 7. Login superuser

#### 8. Meng-update superuser


## 3. PENGATURAN

#### 1. Pengaturan bahasa dari Bahasa Inggris ke Bahasa Indonesia

        modified:   README.md
        modified:   config/settings.py

#### 2. Pengaturan waktu dari UTC ke waktu Asia/Jakarta

        modified:   README.md
        modified:   config/settings.py

#### 3. Membuat path untuk static files

        modified:   README.md
        modified:   config/settings.py
        modified:   config/urls.py

#### 4. Membuat path untuk media files

        modified:   README.md
        modified:   config/settings.py
        modified:   config/urls.py


## 4. DATABASE

#### 1. Membuat database menggunakan postgresql


        λ psql -U postgres
        psql (16.2)
        WARNING: Console code page (437) differs from Windows code page (1252)
                 8-bit characters might not work correctly. See psql reference
                 page "Notes for Windows users" for details.
        Type "help" for help.

        postgres=# 

        postgres=# CREATE DATABASE 80_indonesia_dj5_manajemen_rumah_sakit;
        ERROR:  trailing junk after numeric literal at or near "80_"
        LINE 1: CREATE DATABASE 80_indonesia_complete_blog_app
                                ^
        postgres=# CREATE DATABASE indonesia_80_complete_blog_app;
        CREATE DATABASE

        postgres=# SELECT datname FROM pg_database;
                        datname
        ----------------------------------------
         ...
         indonesia_80_complete_blog_app
        (8 rows)

#### 2. Menghubungkan proyek dengan database

        # PostgreSQL DB
        DATABASES = {
            'default': {
                'ENGINE': 'django.db.backends.postgresql_psycopg2',
                'NAME': 'indonesia_80_complete_blog_app',
                'USER': 'postgres',
                'PASSWORD': 'postgres',
                'HOST': 'localhost',
                'PORT': '5432'
            }
        }

        Note:

        Terjadi error karena driver atau modul psycopg2 atau psycopg belum
        di instal.

        raise ImproperlyConfigured("Error loading psycopg2 or psycopg module")
        django.core.exceptions.ImproperlyConfigured: Error loading psycopg2 or psycopg module

        Next:

        Menginstal psycopg2

        modified:   README.md
        modified:   config/settings.py

#### 3. Menginstal driver atau module psycopg2

        (venv312511) λ pip install psycopg2
        Collecting psycopg2
          Using cached psycopg2-2.9.9-cp312-cp312-win_amd64.whl.metadata (4.5 kB)
        Using cached psycopg2-2.9.9-cp312-cp312-win_amd64.whl (1.2 MB)
        Installing collected packages: psycopg2
        Successfully installed psycopg2-2.9.9

        (venv312511) λ python manage.py check
        System check identified no issues (0 silenced).


## 5. MELINDUNGI FILE PENTING

#### 1. Membuat file .env, .env.example dan melengkapinya dengan environ variabel

        SECRET_KEY=django-insecure-kdk&^0&-uj(nmy!*6%x@(-i(gj5p#h%5kn93ya+$qp+0qkj1gz
        DATABASE_NAME=indonesia_80_dj5_manajemen_rumah_sakit
        DATABASE_USER=postgres
        DATABASE_PASSWORD=postgres
        DATABASE_HOST=localhost
        DATABASE_PORT=5432

        new file:   .env.example
        modified:   README.md