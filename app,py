from flask import Flask, render_template, request

app = Flask(__name__)



# Make a homepage
@app.route('/')
def homepage():
    return render_template("base.html")

@app.route('/form' , methods=[ 'GET' , 'POST' ])
def formDemo(name=None):
    if request.method == 'POST':
        name=request.form['name']
    return render_template('form.html', name=name)

@app.route('/hello/<name>')
def hello(name):
    listOfNames = {name, "LLoyd", "Jennifer"}
    return render_template('name.html', Sname=name, nameList=listOfNames)

if __name__ == "__main__":
    app.run(debug=True)