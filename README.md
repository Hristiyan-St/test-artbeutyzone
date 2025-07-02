# Art Beauty Zone — Jinja2 Template

Този проект е преработен от React/Next.js към Jinja2 шаблони, подходящи за Flask или Django приложения.

## 📁 Структура

- `templates/` — всички Jinja2 HTML шаблони
  - `base.html` — основен шаблон, съдържа header/footer
  - `index.html` — начална страница
  - `sections/` — включваеми части като Hero, Gallery, FAQ и други
  - `admin/` — шаблони за админ панела (график, служители, и т.н.)
  - `macros.html` — повторяеми UI компоненти (бутон, карта, alert и др.)

- `static/`
  - `css/globals.css` — Tailwind базирани стилове
  - `img/` — икони, изображения (ако има)

## 🚀 Стартиране с Flask (пример)

1. Инсталирай Flask:

    ```bash
    pip install flask
    ```

2. Създай файл `app.py`:

    ```python
    from flask import Flask, render_template

    app = Flask(__name__)

    @app.route("/")
    def home():
        return render_template("index.html")

    if __name__ == "__main__":
        app.run(debug=True)
    ```

3. Стартирай:

    ```bash
    python app.py
    ```

4. Отвори браузър: [http://localhost:5000](http://localhost:5000)

## 🛠 TODO

- Свързване с база данни или бекенд
- Динамика за форми, резервации, календар и потребители
