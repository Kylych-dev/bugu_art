## API Endpoints

### Аутентификация/Авторизация

| HTTP Method | Endpoint               | Description                    |
|-------------|------------------------|--------------------------------|
| POST        | `/register/`           | Register a new user            |
| POST        | `/login/`              | User login                     |
| POST        | `/logout/`             | User logout                    |

### Статьи

| HTTP Method | Endpoint                   | Description                        |
|-------------|----------------------------|------------------------------------|
| GET, POST   | `/articles/`               | List all articles / Create article |
| GET, PUT, DELETE | `/articles/<int:pk>/` | Retrieve, update, delete article   |

### Пользователи

| HTTP Method | Endpoint                   | Description                        |
|-------------|----------------------------|------------------------------------|
| GET         | `/users/`                  | List all users                     |
| GET         | `/users/profile/`          | Retrieve user profile              |




## Features

- Аутентификация пользователей: Регистрация, вход и выход пользователей. <br>
- Управление статьями: Создание, отображение, обновление и удаление статей. <br>



## Contributing

telegram: **`@mirbekov0909`** <br>

email: **`tteest624@gmail.com`** <br>

email: **`mirbekov1kylych@gmail.com`**







## Тестирование с помощью Postman

Рекомендуется тестировать конечные точки API с помощью Postman для более интерактивного и комплексного тестирования. Вот несколько рекомендаций по тестированию:

### Authentication

1. **Register a New User:**
   - **Endpoint:** `POST /register/`
   - **Description:** Создайте новую учетную запись пользователя, предоставив email, имя пользователя и пароль.
   - **Payload Example:**
     ```json
     {
       "email": "user@example.com",
       "username": "newuser",
       "password": "password123",
       "password2": "password123",
       "role": "subscriber"  // or "author"
     }
     ```

2. **Login:**
   - **Endpoint:** `POST /login/`
   - **Description:** Authenticate a user and obtain a token.
   - **Payload Example:**
     ```json
     {
       "username": "newuser",
       "password": "password123"
     }
     ```

3. **Logout:**
   - **Endpoint:** `POST /logout/`
   - **Description:** Log out the authenticated user.
   - **Payload Example:**
     ```json
     {
       "refresh_token": "your_refresh_token"
     }
     ```

### Articles

1. **Create an Article:**
   - **Endpoint:** `POST /articles/`
   - **Description:** Create a new article.
   - **Payload Example:**
     ```json
     {
       "title": "Article Title",
       "content": "Article content here."
     }
     ```

2. **List Articles:**
   - **Endpoint:** `GET /articles/`
   - **Description:** Retrieve a list of articles.

3. **Retrieve an Article:**
   - **Endpoint:** `GET /articles/{id}/`
   - **Description:** Retrieve details of a specific article.

4. **Update an Article:**
   - **Endpoint:** `PUT /articles/{id}/`
   - **Description:** Update details of a specific article.
   - **Payload Example:**
     ```json
     {
       "title": "Updated Title",
       "content": "Updated content here."
     }
     ```

5. **Delete an Article:**
   - **Endpoint:** `DELETE /articles/{id}/`
   - **Description:** Delete a specific article.