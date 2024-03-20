# unfolding-umber-uploader

A robust file uploader with support for chunked uploads, retry logic, and progress tracking.

## Features

- Chunked uploads for handling large files efficiently
- Automatic retries for handling network issues
- Progress tracking for user feedback

## Installation

Install `unfolding-umber-uploader` using npm:

```bash
npm install unfolding-umber-uploader
```

## Usage

Here's how to use `unfolding-umber-uploader` to upload a file:

```javascript
const UmberUploader = require('unfolding-umber-uploader');
const uploader = new UmberUploader({/* options */});

uploader.on('progress', (data) => {
console.log(`Upload progress for ${data.file}: ${data.percentage}%`);
});

uploader.on('complete', (data) => {
console.log(`Upload complete. File URL: ${data.url}`);
});

uploader.upload('path/to/your/file.txt');
```
