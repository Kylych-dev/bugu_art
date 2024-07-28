## API Endpoints

### Authentication/Authorization

| HTTP Method | Endpoint               | Description                    |
|-------------|------------------------|--------------------------------|
| POST        | `/register/`           | Register a new user            |
| POST        | `/login/`              | User login                     |
| POST        | `/logout/`             | User logout                    |

### Articles

| HTTP Method | Endpoint                   | Description                        |
|-------------|----------------------------|------------------------------------|
| GET, POST   | `/articles/`               | List all articles / Create article |
| GET, PUT, DELETE | `/articles/<int:pk>/` | Retrieve, update, delete article   |

### Users (Commented out, not active)

| HTTP Method | Endpoint                   | Description                        |
|-------------|----------------------------|------------------------------------|
| GET         | `/users/`                  | List all users                     |
| GET         | `/users/profile/`          | Retrieve user profile              |



**Bugu Article** is a RESTful API project designed for managing articles and user authentication. <br> 
The application provides endpoints for user registration, login, and logout, as well as for creating, <br> retrieving, updating, and deleting articles.

## Features

- **User Authentication:** Register, login, and logout users. <br>
- **Article Management:** Create, list, update, and delete articles. <br>



## Contributing

telegram: **`@mirbekov0909`** <br>

email: **`tteest624@gmail.com`** <br>

email: **`mirbekov1kylych@gmail.com`**







## Testing with Postman

It is recommended to test the API endpoints using Postman for a more interactive and comprehensive testing experience. Here are some suggestions on what to test:

### Authentication

1. **Register a New User:**
   - **Endpoint:** `POST /register/`
   - **Description:** Create a new user account by providing an email, username, and password.
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

### Tips for Testing

- Ensure that you include the necessary headers for authentication (e.g., `Authorization: Bearer your_access_token`).
- Test various scenarios, including valid and invalid data, to verify the robustness of the API.
- Use Postman's environment variables to manage different environments (e.g., development, production) and tokens.

By using Postman, you can interactively test the API and verify that all endpoints work as expected. This will help ensure the correctness and reliability of your application.
