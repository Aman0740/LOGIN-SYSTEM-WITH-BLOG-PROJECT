# LOGIN-SYSTEM-WITH-BLOG-PROJECT

This project aims to develop a "Blog Management System" using modern web technologies. It will consist of a **frontend** built with **React.js** and a **backend** powered by **Node.js**, **Express**, and **MongoDB**. The application will allow users to manage blog posts and implement user authentication with role-based access (admin and regular users).

### Key Features:

#### Frontend (React.js):
1. **User Interface**:
   - Users will have dedicated pages to **sign up** and **log in**.
   - After logging in, users will get a **JWT token** for authentication, stored securely in cookies.
   
2. **User Roles**:
   - There are two roles: **Admin** and **User**.
   - **Admin**: Can perform all actions, including creating, updating, deleting, and viewing any blog post.
   - **User**: Can create posts, view all posts, and update or delete only their own posts.
   
3. **Blog Management**:
   - Users can **create**, **view**, **update**, and **delete** blog posts.
   - Blog posts will display key details like the title, author, content, and tags.
   - The interface will be responsive and styled using **CSS** or **Bootstrap**.

#### Backend (Node.js, Express, MongoDB):
1. **Authentication**:
   - Users can **sign up** with a username, email, and password. Passwords will be encrypted using **bcrypt**.
   - **Login** generates a **JWT token** for users, which will be used for secure authentication.
   
2. **Role-Based Access**:
   - Middleware will verify users’ JWT tokens and enforce role-based permissions.
   - Users can perform actions based on their role: admins can manage all posts, while regular users can only manage their own posts.

3. **CRUD Operations for Blog Posts**:
   - **Create**: Authenticated users can add new posts.
   - **Read**: All users can view any post.
   - **Update**: Users can update their own posts; admins can update any post.
   - **Delete**: Users can delete their own posts; admins can delete any post.

4. **Security**:
   - **JWT tokens** will be stored in **HTTP-only cookies** to prevent unauthorized access.
   - **Passwords** will be encrypted with **bcrypt** to enhance security.
   - **Mongoose** will be used to define data models for blog posts and users.

#### Database (MongoDB):
1. **BlogPost Model**:
   - Includes fields for title, author, content, tags, and the date it was published.
   
2. **User Model**:
   - Contains user information like username, email, hashed password, and the user’s role (admin or user).

#### Routing and Communication:
- The frontend will use **Axios** or **Fetch API** to handle API calls to the backend for actions like signing in, signing up, and managing blog posts.
- **React Router** will manage page navigation.
- **JWT tokens** stored in cookies will be used to manage user sessions, ensuring that actions like creating or deleting posts are protected.

### Folder Structure:
The project will follow a clear folder structure for both the frontend and backend:
- **Backend**: Controllers for managing authentication and blog posts, routes for handling requests, and middleware for authentication and role-based access.
- **Frontend**: Components for user authentication (sign up, login) and blog management (listing, creating, viewing, updating blog posts).
