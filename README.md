

# Django Social Blog

![1](/README_IMAGES/1.png)
![2](/README_IMAGES/2.png)
![3](/README_IMAGES/3.png)
![4](/README_IMAGES/4.png)
![5](/README_IMAGES/5.png)
![6](/README_IMAGES/6.png)
![7](/README_IMAGES/7.png)
![8](/README_IMAGES/8.png)
![9](/README_IMAGES/9.png)
![10](/README_IMAGES/10.png)
![11](/README_IMAGES/11.png)
![12](/README_IMAGES/12.png)


A blog-centric social media platform developed using Django 4.0.1, where users can create, manage, and share posts, as well as handle user profile management and authentication.

## Project Structure

- Main Directory: `django_project`
  - `urls.py`: Handles HTTP request routing either to other app-specific `urls.py` files or directly to a view.
  - `settings.py`: Houses essential settings like `INSTALLED_APPS` and `MEDIA_ROOT` for development and deployment.
- Apps:
  - `blog`: Manages functionalities and routes related to posts.
  - `users`: Focuses on user-related features such as user authentication and profile management.

### Key Insights

1. **`INSTALLED_APPS`** (in `settings.py`): Ensure to register each new development app here for Django to acknowledge them.
   
2. **`MEDIA_ROOT`** (in `settings.py`): Defines the directory to store media files. 

3. **`urls.py`**: Utilized to map URL patterns which guide user navigation through the app, such as the `blog-home` route in the `blog` app.

### Apps Details

#### 1. Blog App
- **Key Files & Features:**
  - `models.py`: Houses the `Post` model.
  - `views.py`: Contains `PostListView`, fetching all posts (`Post.objects.all()`) and rendering them using the `blog/home.html` template.
  - `urls.py`: Defines routes, e.g., `blog-home`, directing HTTP requests to specific views.
   
#### 2. Users App
- Manages user-related functionalities like user authentication, profile management, etc.
- **Key Files & Features:**
  - **`Profile` Model**: The `Profile` model extends the User model using a one-to-one relationship to manage user profile images.
  - **`signals.py`**: Ensures a `Profile` instance is automatically created for each `User` instance.
  - **Note**: The `users` app does not contain a `urls.py` file as all views from this app are directly imported into the main project directory's `urls.py`.

### Media Storage
- Media files are stored in an Amazon S3 bucket, circumventing Heroku's lack of media file storage.



## Acknowledgments
Gratitude goes to Corey Schafer and his insightful Django course, which significantly aided the construction of this project.

## Contact
Email: tiqbal10a@gmail.com
