from flask import render_template
from app import app

@app.route('/')
@app.route('/index')
def index():
    user = {'username': 'Harsh'}
    posts = [
        {
            'author': {'username': 'kushal'},
            'body': 'Beautiful day in Califoria!'
        },
        {
            'author': {'username': 'mahesh'},
            'body': 'Amazing day at australia!'
        }
    ]
    return render_template('index.html', title='Home', user=user, posts=posts)