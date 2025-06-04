# asd
asd
🔁 1. Fork & Clone the Repository
Since this is a public project, the recommended way to contribute is through a fork:

Go to the repository:
👉 https://github.com/ByteOfWaffle/MyGameLists

Click the Fork button (top right) to create your own copy of the repo.

Clone your fork to your local machine:

bash
Copy
Edit
git clone https://github.com/YOUR_USERNAME/MyGameLists.git
cd MyGameLists
(Optional) Add the original repository as an upstream remote (to keep your fork updated):

bash
Copy
Edit
git remote add upstream https://github.com/ByteOfWaffle/MyGameLists.git
📦 2. Install Dependencies
Make sure your environment is ready:

bash
Copy
Edit
pip install -r requirements.txt
🛠 3. Set Up the MariaDB Database
You’ll need a working MariaDB instance. You can host it any way you like — I hosted it on Ubuntu in a virtual machine for this project.

Import the SQL schema:

Use the database.sql file in the project directory to create the required tables.

Listen on all network interfaces:
Open the config file:

bash
Copy
Edit
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
Change:

ini
Copy
Edit
bind-address = 0.0.0.0
Open necessary ports:

bash
Copy
Edit
sudo ufw allow 8080
If using Apache for static hosting:

bash
Copy
Edit
sudo ufw allow 80
Update IP in your app:
In app1.py, change the database host IP to match the IP of your database server.

✍️ 4. Make Your Changes
Create a new branch for your feature or fix:

bash
Copy
Edit
git checkout -b your-feature-name
Make your changes and commit them:

bash
Copy
Edit
git add .
git commit -m "Description of your changes"
Push your branch to your fork:

bash
Copy
Edit
git push origin your-feature-name
📬 5. Open a Pull Request
Go to your fork on GitHub.

Click "Compare & pull request".

Make sure it targets ByteOfWaffle/MyGameLists:main.

Add a clear title and description of your changes.

Submit the pull request.
