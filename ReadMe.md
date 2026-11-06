# 🏋️‍♀️ R.I.S.E. Fitness

**Own your journey.** One place for the workout, the meal plan, and the reason you showed up today.

R.I.S.E. Fitness is a personal health dashboard. Sign up, set a goal, and the app keeps the week in front of you: meals you actually plan to eat, workouts matched to your level and the time you have, progress you can see, and a wellness blog for the days motivation is thin.

It is built for consistency, not extremes. Fifteen minutes counts. A saved meal plan counts. Checking off Tuesday counts.

## What a week looks like

1. **Join.** Create an account and tell the app who you are: height, weight, fitness goal, experience, and how you like to eat.
2. **Train.** Browse workout videos filtered to your goal, level, and available time — 15 minutes, 30 minutes, or longer. Mark a session done when you finish it.
3. **Eat.** Build a meal plan for the week, then come back to view, edit, or clone it when next week looks a lot like this one.
4. **Read.** Open the wellness blog for nutrition, mindset, and the occasional reminder that progress is slower than a highlight reel.
5. **Check the dashboard.** Today’s meal, today’s workout, recent articles, and how much of the week you have already completed — all on one screen.

## What you can do

| | |
|---|---|
| 🔐 **Account** | Sign up, sign in, reset your password, or delete your account. |
| 👤 **Profile** | Save goals, experience, diet, measurements, date of birth, and a profile photo. |
| 📊 **Dashboard** | See today’s meal, today’s workout, weekly progress, and the latest blog posts. |
| 🏃 **Workouts** | Watch sessions matched to your goal and mark them complete. |
| 🥗 **Meal plans** | Log a week of meals, then view, edit, or clone a plan. |
| 📖 **Blog** | Read fitness and wellness articles, and subscribe for updates. |

## Built with

A multi-page [Flask](https://flask.palletsprojects.com/) app: routes, a data-access layer, and [Jinja2](https://jinja.palletsprojects.com/) templates, with [MySQL](https://www.mysql.com/) underneath and Bootstrap plus custom CSS on the page.

- Python 3.12
- Flask
- Jinja2
- MySQL
- HTML, CSS (Bootstrap), and JavaScript

## Run it locally

You need **Python 3.12** and a running **MySQL** server. The app connects as `root` on `localhost` to a database named `rise_db`. On macOS and Linux the password is empty. On Windows it is `password`.

From the project folder:

```bash
python3.12 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

On Windows, activate the virtual environment with `.venv\Scripts\activate` instead of `source`.

Load the schema and sample content. This script drops `rise_db` if it already exists, then recreates it:

```bash
mysql -u root < application/rise_db.sql
```

On Windows, add the password:

```bash
mysql -u root -ppassword < application/rise_db.sql
```

Start the app:

```bash
python app.py
```

Open [http://127.0.0.1:5001](http://127.0.0.1:5001), create an account, and set your profile. The dashboard fills in from there.
