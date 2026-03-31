📁 File Management API

A robust, scalable, and highly efficient RESTful API built with ASP.NET Core for seamless file and media management. This system provides a complete solution for handling file uploads, bulk processing, secure downloads, and high-performance media streaming.

✨ Key Features
🚀 Single & Bulk Uploads: Efficiently handle individual file uploads or process multiple files simultaneously.

🖼️ Dedicated Image Handling: Specialized endpoint optimized for image uploads.

⬇️ Secure Downloads: Fast and reliable file retrieval using unique identifiers (GUIDs).

🎥 Advanced Media Streaming: Built-in support for media streaming (Audio/Video) with Range processing enabled, allowing clients to buffer and skip through media smoothly without downloading the entire file.

⚡ Asynchronous & Scalable: Fully async operations using CancellationToken to ensure optimal resource utilization and prevent thread starvation under heavy loads.

🛣️ API Endpoints
Here is the list of available endpoints in the FilesController:

Method	Endpoint	Description	Content-Type
POST	/api/files/upload	Uploads a single file and returns its location.	multipart/form-data
POST	/api/files/upload-many	Uploads multiple files in a single request and returns their IDs.	multipart/form-data
POST	/api/files/upload-image	Uploads a specific image file.	multipart/form-data
GET	/api/files/download/{id}	Downloads a specific file by its unique ID.	application/octet-stream
GET	/api/files/stream/{id}	Streams media files with HTTP Range support for video/audio players.	*/*

🛠️ Tech Stack & Architecture
Framework: .NET 10 (ASP.NET Core Web API)

Pattern: Service Pattern (IFileService, FileService)

Constructor Injection: Modern C# Primary Constructors for cleaner Dependency Injection.

Streaming Protocol: Native ASP.NET Core FileStreamResult with partial request support.

💻 Usage Example (Streaming)
The /api/files/stream/{id} endpoint is specifically configured with enableRangeProcessing: true. This makes it perfect for plugging directly into HTML5