# PDF.js Express - Blazor sample

[PDF.js Express](https://pdfjs.express/) is a powerful JavaScript-based PDF Library that leverages PDF.js and adds additional features such as annotations, form support, and digitial signatures. It provides a slick out-of-the-box responsive UI that interacts with the core library to view, annotate and manipulate PDFs that can be embedded into any web project.

This repo is specifically designed for any users interested in integrating WebViewer into a Blazor project. This project was integrated using the [Blazor server-sided application template](https://docs.microsoft.com/en-us/aspnet/core/blazor/get-started?view=aspnetcore-3.0&tabs=visual-studio).

## Initial setup

Before you begin, make sure your development environment includes [.NET Core 3.0 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.0) and [Node.js](https://nodejs.org/en/).

## Install

```
git clone https://github.com/pdfjs-express/pdfjs-express-blazor-sample.git
cd pdfjs-express-blazor-sample
npm install
```

## Run

```
npm start
```

Navigate to `https://localhost:5001/webviewer`

## WebViewer APIs

See [API documentation](https://pdfjs.express/documentation).

## Enabling full API

PDFNetJS Full is a complete browser side PDF SDK, unlocking viewing, parsing and editing of PDF files. To enable full API, you can modify constructor in `wwwroot/js/webviewerScripts.js`:

```diff
initWebViewer: function () {
    const viewerElement = document.getElementById('viewer');
    WebViewer({
        path: 'lib',
        initialDoc: 'https://pdftron.s3.amazonaws.com/downloads/pl/demo-annotated.pdf', // replace with your own PDF file
+        fullAPI: true
    }, viewerElement).then((instance) => {
        // call APIs here
    })
}
```

You can refer to this [guide for more information](https://pdfjs.express/documentation/get-started)

## License

See [license](./LICENSE).
