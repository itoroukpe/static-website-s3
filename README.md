# static-website-s3

Below is a simple example of HTML, CSS, and JavaScript code for a static website to publish blogs, along with an image:

**HTML (index.html):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Blog</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to My Blog</h1>
  </header>
  <main>
    <article>
      <h2>Blog Post Title</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <img src="image.jpg" alt="Blog Post Image">
    </article>
  </main>
  <footer>
    <p>&copy; 2024 My Blog</p>
  </footer>
  <script src="script.js"></script>
</body>
</html>
```

**CSS (styles.css):**
```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

main {
  padding: 20px;
}

article {
  margin-bottom: 30px;
}

footer {
  background-color: #333;
  color: #fff;
  padding: 10px;
  text-align: center;
}
```

**JavaScript (script.js):**
```javascript
// JavaScript code can be added here if needed
```

**Image (image.jpg):**
You would need to have an actual image file named "image.jpg" in the same directory as your HTML file.

To publish this static website using an AWS S3 bucket, follow these steps:

1. **Create an S3 Bucket:**
   - Log in to your AWS Management Console.
   - Navigate to the Amazon S3 service.
   - Click on the "Create bucket" button.
   - Enter a unique bucket name and choose the region where you want to host your website.
   - Click "Create" to create the bucket.

2. **Upload Files to the Bucket:**
   - Upload your HTML, CSS, JavaScript, and image files to the S3 bucket. You can do this by clicking the "Upload" button in the S3 console and selecting the files from your computer.

3. **Configure Bucket for Static Website Hosting:**
   - Select the bucket you created.
   - Go to the "Properties" tab and click on "Static website hosting."
   - Choose "Use this bucket to host a website" and enter the name of your HTML file (e.g., "index.html") as the index document.
   - Click "Save changes."

4. **Set Bucket Policy for Public Access:**
   - Go to the "Permissions" tab of your bucket.
   - Click on "Bucket Policy" and enter a policy that allows public read access to your files. You can use the same bucket policy as mentioned in the previous answer.
   - Replace "your-bucket-name" with the name of your bucket.

5. **Access Your Website:**
   - Once you've configured the bucket for static website hosting and set the appropriate permissions, your website should be accessible via the provided endpoint URL.
   - You can find the endpoint URL for your website in the "Static website hosting" section of your bucket properties.

That's it! Your static website is now published and accessible to the public via the AWS S3 bucket. You can continue to update and manage your website by uploading new files to the bucket as needed.
