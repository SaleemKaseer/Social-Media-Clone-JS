# Social Media Clone (HTML · CSS · JavaScript)

A small social media web app built with plain HTML, CSS and JavaScript, with no frontend framework. It uses the public **Tarmeez Academy REST API** (`https://tarmeezacademy.com/api/v1`) as its backend. Users can sign up, log in, share posts with images, comment on posts and browse other users' profiles.

## ✨ Features

- **Sign-up and log-in**
  - Register with a name, username, password and profile picture
  - Log in and log out; the auth token and user data are kept in `localStorage`
  - The navbar changes depending on whether you're a guest or logged in (shows your avatar and username)

- **Home feed**
  - A paginated feed of the newest posts
  - **Infinite scroll** loads the next page when you reach the bottom
  - Each post shows the author's avatar, image, date, title, body, comment count and tags

- **Posts (CRUD)**
  - Create a post with a title, body and image (sent as `multipart/form-data`)
  - Edit and delete **your own** posts only; the buttons appear only on posts you wrote
  - Delete asks for confirmation in a modal first

- **Post details and comments**
  - Open any post to see it in full along with all its comments
  - Logged-in users can add comments

- **User profiles**
  - Click a username or avatar to open that user's profile
  - Shows name, username, email, profile picture, and post and comment counts
  - Lists all of that user's posts

- **UI and UX**
  - Responsive layout built with **Bootstrap 5** (navbar, cards, modals, alerts)
  - Success and error alerts for every action, with the API's error messages
  - A loading spinner while requests are running
  - Fallback images when a user or post has no picture

## 🛠️ Tech Stack

| Layer        | Tools                               |
|--------------|-------------------------------------|
| Markup/Style | HTML5, CSS3, Bootstrap 5, Bootstrap Icons |
| Logic        | Vanilla JavaScript (ES6+)           |
| HTTP         | Axios                               |
| Backend      | Tarmeez Academy REST API            |

## 📁 Project Structure
├── home.html # Home feed (main entry point)
├── postDetails.html # Single post + comments
├── profile.html # User profile page
├── INDEX.HTML # Early single-file version of the feed
├── mainLogic.js # Shared logic: auth, UI setup, create/edit/delete posts, alerts, loader
├── homeScripts.js # Feed loading, pagination & infinite scroll
├── profileScripts.js # Profile info & user's posts
├── profile-pics/ # Default avatar
├── placeholders/ # Default post image
└── package.json


## 🚀 Getting Started

1. **Clone the repo**
```bash
   git clone https://github.com/SaleemKaseer/Social-Media-Clone-JS.git
   cd Social-Media-Clone-JS
```
2. **Install dependencies** (Bootstrap, Bootstrap Icons, Axios)
```bash
   npm install
```
3. **Run it:** open `home.html` in your browser, or serve the folder with a tool like the VS Code *Live Server* extension.

> The pages load Bootstrap and Axios from `node_modules`, so run `npm install` before opening them.

## 🔌 API Endpoints Used

| Method | Endpoint                    | Purpose                  |
|--------|-----------------------------|--------------------------|
| POST   | `/register`                 | Create a new account     |
| POST   | `/login`                    | Log in                   |
| GET    | `/posts?limit=&page=`       | Get the paginated feed   |
| GET    | `/posts/{id}`               | Get a post with its comments |
| POST   | `/posts`                    | Create a post            |
| POST   | `/posts/{id}` (`_method=put`) | Update a post          |
| DELETE | `/posts/{id}`               | Delete a post            |
| POST   | `/posts/{id}/comments`      | Add a comment            |
| GET    | `/users/{id}`               | Get a user's profile     |
| GET    | `/users/{id}/posts`         | Get a user's posts       |

## 📚 What I Practiced

- Working with a REST API using Axios (GET, POST, PUT via `_method`, DELETE)
- Token-based authentication and sending Bearer tokens in request headers
- Uploading files with `FormData`
- Building and updating the page (DOM) from API data
- Pagination and infinite scroll
- Reading URL query parameters to move between pages (`?postId=`, `?userid=`)
- Splitting shared code into a common script file

## 👤 Author

**Saleem Kaseer**:  · [GitHub](https://github.com/SaleemKaseer) · [LinkedIn](https://www.linkedin.com/in/saleemkaseer)



