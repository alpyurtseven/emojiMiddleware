# Emoticon to Emoji Middleware

This project is a simple ASP.NET application that demonstrates the usage of middleware in the ASP.NET pipeline. The middleware implemented here converts emoticons found in the response body to emojis.

## How it Works

The application consists of custom middleware (`EmojiMiddleware.cs`) that intercepts the response before it is sent to the client. It scans the response body for emoticons and replaces them with corresponding emojis.

## Installation and Usage

1. Clone this repository to your local machine.
2. Open the solution in Visual Studio or your preferred IDE.
3. Build and run the application.
4. Send a request to the application, and it will return a response with the text containing emoticons converted to emojis.

## Middleware Implementation

The middleware is added to the ASP.NET pipeline in the `Program.cs` file. Here's how it's configured:

```csharp

  // Other middleware configurations...

  // Add EmoticonToEmojiMiddleware to the pipeline
  app.UseEmojiMiddleware(); //There is an extension method for this in EmojiMiddlewareExtensions class.

  // Other middleware configurations...

