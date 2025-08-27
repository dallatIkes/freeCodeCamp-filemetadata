# File Metadata Microservice

This project is a **File Metadata Analyzer** API that allows users to upload a file and receive metadata about it such as the file name, type, and size.

## Project Structure

- `index.js` – main Node.js application
- `/public` – contains static assets like CSS
- `views/index.html` – frontend interface for uploading files

## Technologies Used

- Node.js
- Express
- Multer (for handling file uploads)
- CORS

## Features

- Upload a file via a form
- Display metadata including:
  - `name` – file name
  - `type` – MIME type
  - `size` – file size in bytes
- Modern and responsive frontend interface
- JSON output displayed directly on the page after upload

## Usage

1. Clone the repository:

```bash
git clone https://github.com/dallatIkes/freeCodeCamp-filemetadata.git
cd freeCodeCamp-filemetadata
```

2. Install dependencies:

```bash
npm install
```

3. Start the server:

```bash
npm run start
```

4. Open your browser and navigate to:

```
http://localhost:3000
```

## API Endpoints

### POST `/api/fileanalyse`

- Accepts a `multipart/form-data` POST request with a single file field named `upfile`
- Returns a JSON object with metadata about the uploaded file

Example request using `curl`:

```bash
curl -X POST -F "upfile=@example.png" http://localhost:3000/api/fileanalyse
```

Example response:

```json
{
  "name": "example.png",
  "type": "image/png",
  "size": 1024
}
```

## Frontend

- The frontend allows users to select a file and see the resulting JSON directly on the page
- It uses JavaScript `fetch` or a normal form submission to display the response without refreshing the page
- Responsive design with modern dark-themed style

## Notes

- Ensure the server is running before uploading files
- Only one file can be uploaded at a time
- Works with all file types

## License

This project is open source and available under the MIT License
