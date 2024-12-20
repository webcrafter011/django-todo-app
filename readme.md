# Todo List Application

This is a simple Todo List application built with Django. It allows users to add, view, and delete todo items.

## Project Structure

```
TODOLIST/
    manage.py
    TODOLIST/
        __init__.py
        settings.py
        urls.py
        wsgi.py
    todo_list_app/
        __init__.py
        admin.py
        apps.py
        models.py
        tests.py
        views.py
        forms.py
        migrations/
            __init__.py
    templates/
        todo/
            index.html
            404.html
    static/
        todo/
            style.css
```

## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd TODOLIST
    ```

2. **Create a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Apply migrations**:
    ```bash
    python manage.py migrate
    ```

5. **Run the development server**:
    ```bash
    python manage.py runserver
    ```

6. **Access the application**:
    Open your web browser and go to `http://127.0.0.1:8000/`.

## Usage

- **Add a Todo Item**: Use the form on the right side of the page to add a new todo item.
- **View Todo Items**: The main section of the page displays the list of todo items.
- **Delete a Todo Item**: Click the "remove" button next to a todo item to delete it.

## Models

### Todo

- **title**: `CharField` - The title of the todo item.
- **details**: `TextField` - The details of the todo item.
- **date**: `DateField` - The date the todo item was created.

## Views

### index

- **Description**: Displays the list of todo items and the form to add a new item.
- **Template**: `todo/index.html`

### remove

- **Description**: Deletes a todo item based on its ID.
- **Template**: Redirects to the index view.

### handler404

- **Description**: Custom 404 error handler.
- **Template**: `todo/404.html`

## Templates

### index.html

- **Description**: Main template for displaying and managing todo items.
- **Location**: `templates/todo/index.html`

### 404.html

- **Description**: Custom 404 error page.
- **Location**: `templates/todo/404.html`

## Static Files

- **CSS**: Custom styles for the application.
- **Location**: `static/todo/style.css`

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
