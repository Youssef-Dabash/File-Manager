📁 File Management API

A robust, scalable, and highly efficient RESTful API built with ASP.NET Core for seamless file and media management. 
This system provides a complete solution for handling file uploads, bulk processing, secure downloads, and high-performance media streaming.

✨ Key Features

🚀 Single & Bulk Uploads: Efficiently handle individual file uploads or process multiple files simultaneously.

🖼️ Dedicated Image Handling: Specialized endpoint optimized for image uploads.

⬇️ Secure Downloads: Fast and reliable file retrieval using unique identifiers (GUIDs).

🎥 Advanced Media Streaming: Built-in support for media streaming (Audio/Video) with Range processing enabled, 
   allowing clients to buffer and skip through media smoothly without downloading the entire file.

⚡ Asynchronous & Scalable: Fully async operations using CancellationToken to ensure optimal resource utilization and prevent thread starvation under heavy loads.

🛠️ Tech Stack & Architecture
Framework: .NET 10 (ASP.NET Core Web API)

Pattern: Service Pattern (IFileService, FileService)

Constructor Injection: Modern C# Primary Constructors for cleaner Dependency Injection.

Streaming Protocol: Native ASP.NET Core FileStreamResult with partial request support.
