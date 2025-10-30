# S3 Image Upload Solutions

This folder contains several solutions for uploading images to S3. Choose the one that works best for you.

## Option 1: Minimal Direct Upload (Recommended for Testing)

The simplest solution with minimal code:

1. Open `minimal-upload.html` in your browser
2. Select an image and click "Upload"
3. The image will be uploaded directly to S3

This uses the AWS SDK directly in the browser and is the simplest approach.

## Option 2: Node.js Server (Recommended for Production)

A more robust solution using a Node.js server:

1. Install dependencies:
   ```
   npm install
   ```

2. Start the server:
   ```
   node node-upload-server.js
   ```

3. Open `node-uploader.html` in your browser
4. Select an image and click "Upload"

This approach avoids CORS issues and provides better error handling.

## Option 3: Python Server

A Python-based solution:

1. Start the server:
   ```
   python upload-server.py
   ```

2. Open `server-uploader.html` in your browser
3. Select an image and click "Upload"

## Troubleshooting

If you encounter issues:

1. **CORS Errors**: These occur when your browser tries to make cross-origin requests. The Node.js server solution handles this automatically.

2. **Network Errors**: Make sure your AWS credentials are correct and that your bucket exists.

3. **Permission Errors**: Ensure your bucket policy allows the necessary operations.

4. **JSON Parsing Errors**: This usually means the server returned HTML instead of JSON, often due to a server error.

## Bucket Configuration

Make sure your S3 bucket is properly configured:

1. CORS configuration should allow uploads from your domain
2. Bucket policy should allow the necessary operations
3. Public access settings should be appropriate for your use case