---
layout: tailwind
permalink: /profile
#menu: nav/home.html
search_exclude: true
show_reading_time: false
---

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html {
        font-family: 'Roboto', sans-serif;
        background-color: #1a1a1a;
        color: #ffffff;
    }

    .container {
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
        padding-top: 2rem;
    }

    .page-header {
        text-align: center;
        margin-bottom: 2rem;
        padding: 2rem 0;
        border-bottom: 2px solid #007cff;
    }

    .page-header h1 {
        font-size: 2.5rem;
        font-weight: bold;
        color: #007cff;
        margin-bottom: 0.5rem;
    }

    .page-header p {
        color: #a0aec0;
        font-size: 1.1rem;
    }

    .profile {
        display: flex;
        align-items: center;
        margin-bottom: 24px;
        background-color: #2d3748;
        padding: 2rem;
        border-radius: 8px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .profile img {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        border: 4px solid #007cff;
        margin-right: 2rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    }

    .profile div h2 {
        font-size: 2rem;
        font-weight: bold;
        color: #ffffff;
        margin-bottom: 0.5rem;
    }

    .card {
        background-color: #2d3748;
        padding: 1.5rem;
        border-radius: 8px;
        margin-bottom: 1.5rem;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .card h3 {
        font-size: 1.5rem;
        font-weight: 600;
        color: #007cff;
        margin-bottom: 1.5rem;
        border-bottom: 2px solid #007cff;
        padding-bottom: 0.5rem;
    }

    form div {
        margin-bottom: 1rem;
    }

    label {
        display: block;
        margin-bottom: 0.5rem;
        color: #a0aec0;
    }

    input[type="text"],
    input[type="password"] {
        width: 100%;
        padding: 0.75rem;
        border-radius: 4px;
        border: 1px solid #4a5568;
        background-color: #1a202c;
        color: #ffffff;
        margin-bottom: 1rem;
    }

    input[type="text"]:focus,
    input[type="password"]:focus {
        outline: none;
        border-color: #007cff;
        box-shadow: 0 0 0 2px rgba(229, 62, 62, 0.2);
    }

    .file-icon {
        display: inline-block;
        padding: 0.75rem 1.5rem;
        background-color: #007cff;
        color: white;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.2s;
    }

    .file-icon:hover {
        background-color: #c53030;
    }

    #profile-message {
        margin-top: 1rem;
        padding: 0.75rem;
        border-radius: 4px;
        font-weight: 500;
    }

    .grid {
        display: grid;
        gap: 16px;
        margin-bottom: 24px;
    }

    .grid-cols-2 {
        grid-template-columns: repeat(2, 1fr);
    }

    .card img {
        width: 100%;
        border-radius: 8px;
        transition: transform 0.3s ease-in-out;
    }

    .card img:hover {
        transform: scale(1.05);
    }

    .card p {
        margin-top: 8px;
    }

    ul {
        list-style: none;
    }

    ul li {
        margin: 8px 0;
    }

    .input-field {
        width: 100%;
        padding: 0.75rem;
        margin-bottom: 1rem;
        border: 2px solid #007cff;
        border-radius: 6px;
        background-color: #1a1a1a;
        color: #ffffff;
        font-size: 1rem;
        transition: border-color 0.3s ease;
    }

    .input-field:focus {
        outline: none;
        border-color: #fc8181;
        box-shadow: 0 0 0 2px rgba(229, 62, 62, 0.2);
    }

    textarea.input-field {
        resize: vertical;
        min-height: 100px;
    }

    .btn-primary {
        background-color: #007cff;
        color: white;
        padding: 0.75rem 1.5rem;
        border: none;
        border-radius: 6px;
        font-size: 1rem;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    .btn-primary:hover {
        background-color: #c53030;
    }

    #newPostForm {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    #newPostForm label {
        color: #a0aec0;
        font-size: 1rem;
        margin-bottom: 0.5rem;
        display: block;
    }

    .posts-container {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        max-height: 500px;
        overflow-y: auto;
    }

    .message-bubble {
        background-color: #2d3748;
        padding: 1rem;
        border-radius: 8px;
        margin: 0;
        border-left: 3px solid #007cff;
    }

    .post-title {
        font-weight: bold;
        color: #007cff;
        margin-bottom: 0.5rem;
    }

    .post-comment {
        color: #ffffff;
    }
</style>

<header class="heading">
    <h1>GeneScope</h1>
    <p>You can control your settings from here!</p>
</header>

<div class="container">
    <section class="profile">
        <img src="https://placehold.co/150x150" alt="Profile Picture" id="profilePicture">
        <div>
            <h2 id="username">User Name</h2>
        </div>
    </section>
    <section class="card">
        <h3>Profile Settings</h3>
        <form>
            <div>
                <label for="newUid">Enter New UID:</label>
                <input type="text" id="newUid" placeholder="New UID">
            </div>
            <div>
                <label for="newName">Enter New Name:</label>
                <input type="text" id="newName" placeholder="New Name">
            </div>
            <div>
                <label for="newPassword">Enter New Password:</label>
                <input type="password" id="newPassword" placeholder="New Password">
            </div>
            <br>
            <label for="profilePictureUpload" class="file-icon">
                Upload Profile Picture <i class="fas fa-upload"></i>
            </label>
            <input type="file" id="profilePictureUpload" accept="image/*" style="display: none;">
            <p id="profile-message" style="color: blue;"></p>
        </form>
    </section>
    <section class="grid grid-cols-2">
        <div class="card">
            <h3>User Stats</h3>
            <p>Followers: 120</p>
            <p>Following: 75</p>
            <p>Posts: 34</p>
        </div>
        <div class="card">
            <h3>Recent Activity</h3>
            <ul>
                <li>Liked a post about climate change</li>
                <li>Started following @naturelover</li>
                <li>Commented on "Tech Innovations 2025"</li>
            </ul>
        </div>
    </section>
    <section class="card">
        <h3>Create New Post</h3>
        <form id="newPostForm">
            <label for="postTitle">Title:</label>
            <input type="text" id="postTitle" class="input-field" placeholder="Enter post title" required>
            <label for="postComment">Comment:</label>
            <textarea id="postComment" class="input-field" placeholder="Write your comment here..." required></textarea>
            <button type="submit" class="btn-primary">Submit Post</button>
        </form>
        <div class="posts-container" id="postsContainer"></div>
    </section>
    <div class="web-container"></div>
</div>

<script>
    // Handle profile picture upload
    const profilePictureUpload = document.getElementById('profilePictureUpload');
    const profilePicture = document.getElementById('profilePicture');
    const profileMessage = document.getElementById('profile-message');

    profilePictureUpload.addEventListener('change', function () {
        const file = this.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = function (e) {
                profilePicture.src = e.target.result;
                profileMessage.textContent = 'Profile picture updated successfully!';
                profileMessage.style.color = 'green';
            }
            reader.readAsDataURL(file);
        } else {
            profileMessage.textContent = 'No file selected.';
            profileMessage.style.color = 'red';
        }
    });

    // Handle new post creation
    const newPostForm = document.getElementById('newPostForm');
    const postsContainer = document.getElementById('postsContainer');

    newPostForm.addEventListener('submit', function (e) {
        e.preventDefault();

        const title = document.getElementById('postTitle').value.trim();
        const comment = document.getElementById('postComment').value.trim();

        if (!title || !comment) {
            alert('Please fill out both title and comment.');
            return;
        }

        const postDiv = document.createElement('div');
        postDiv.classList.add('message-bubble');

        const postTitle = document.createElement('div');
        postTitle.classList.add('post-title');
        postTitle.textContent = title;

        const postComment = document.createElement('div');
        postComment.classList.add('post-comment');
        postComment.textContent = comment;

        postDiv.appendChild(postTitle);
        postDiv.appendChild(postComment);

        postsContainer.prepend(postDiv);

        newPostForm.reset();
    });

    // Load logged-in user data from localStorage
    const userData = JSON.parse(localStorage.getItem('user'));
    if (userData) {
        if (userData.name) {
            document.getElementById('username').textContent = userData.name;
        }
        if (userData.profilePicture) {
            document.getElementById('profilePicture').src = userData.profilePicture;
        }
    }
</script>