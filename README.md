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
    <h1>Welcome to RondusTech Blog</h1>
  </header>
  <main>
    <article>
      <h2>Title: Step-by-Step Guide to Launching a Static Website on AWS S3 Bucket</h2>
      <p>In today's digital age, having an online presence is essential for individuals and businesses alike. Whether you're showcasing your portfolio, promoting your business, or sharing your thoughts through a blog, launching a website is the first step towards reaching a global audience. In this blog post, we'll walk you through the process of launching a static website on an AWS S3 bucket, a simple and cost-effective solution for hosting static content.</p>

<h2>What is a Static Website?<h2>
<p>A static website consists of web pages with fixed content that does not change dynamically. These websites are typically built using HTML, CSS, and JavaScript and are suitable for content that doesn't require frequent updates or user interactions.</p>

<h2>Why AWS S3 Bucket?<h2>
<p>Amazon S3 (Simple Storage Service) is a highly scalable, reliable, and cost-effective cloud storage service provided by Amazon Web Services (AWS). It is commonly used for storing and serving static content, making it an ideal choice for hosting static websites. With S3, you can benefit from high availability, durability, and low latency, ensuring a seamless experience for your website visitors.</p>

<h2>Step 1: Create an AWS Account<h2>
<p>If you don't already have an AWS account, you'll need to sign up for one. Visit the AWS website and follow the instructions to create a new account. You may need to provide payment information, but AWS offers a free tier with certain usage limits, which should be sufficient for hosting a small static website.</p>

<h2>Step 2: Set Up an S3 Bucket<h2>
<p>Once you've logged in to your AWS Management Console, navigate to the Amazon S3 service. Click on the "Create bucket" button to create a new bucket. Choose a unique name for your bucket, select the region where you want to host your website, and leave the remaining settings as default. Click "Create" to create the bucket.</p>

<h2>Step 3: Configure Bucket for Static Website Hosting<h2>
<p>Select the bucket you just created and go to the "Properties" tab. Scroll down to the "Static website hosting" section and click on "Edit." Choose the option to "Use this bucket to host a website" and enter the name of your index document (e.g., index.html). You can also specify an optional error document if desired. Click "Save changes" to save your settings.</p>

<h2>Step 4: Upload Website Files<h2>
<p>Upload your website files to the S3 bucket. This typically includes HTML, CSS, JavaScript, and any other assets such as images or videos. You can upload files individually or use the AWS CLI or SDK for batch uploads.</p>

<h2>Step 5: Set Bucket Policy for Public Access<h2>
<p>To make your website accessible to the public, you'll need to set a bucket policy that allows read access to everyone. Go to the "Permissions" tab of your bucket, click on "Bucket Policy," and enter a policy similar to the following:</p>

<p>
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```
</p>
<p>Replace "your-bucket-name" with the name of your bucket. Click "Save" to apply the policy.</p>

<h2>Step 6: Access Your Website<h2>
<p>Once you've configured your bucket for static website hosting and set the appropriate permissions, your website should be accessible via the provided endpoint URL. You can find the endpoint URL in the "Static website hosting" section of your bucket properties. You can also set up a custom domain using Amazon Route 53 or a third-party domain registrar and point it to your S3 bucket endpoint for a more professional look.</p>

<h2>Conclusion<h2>
<p>Launching a static website on an AWS S3 bucket is a quick and easy way to get your website up and running with minimal effort and cost. By following the steps outlined in this guide, you can create a scalable and reliable website that is accessible to users around the world. Whether you're a developer, blogger, or small business owner, AWS S3 provides the tools you need to showcase your content and engage with your audience online. So why wait? Get started today and take your first step towards establishing your online presence!</p>
      <img src="https://1drv.ms/i/s!Ag0LJquTdwyThI9s11OovU-OprjmCw?e=4yiVzT" alt="Blog Post Image">
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
