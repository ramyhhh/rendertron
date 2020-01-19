## Rendertron [fork]
This fork (rami branch) enables PDF generation from web page request (Original Rendertron decided not to add this feature), the URLs goes like:

```
GET 'rendertron-host/pdf/:url(.*)'
POST 'rendertron-host/pdf/:url(.*)'
```

The POST request can include options, as a url-encoded form, and the default options looks like:
```
defaults = {
  displayHeaderFooter: false,
  headerTemplate: '',
  footerTemplate: '',
  printBackground: true,
  format: 'A4'
}
```

### How it works
Rendertron depends on Puppeteer which utilizes headless chrome, so PDF generation process is the same when you use Chrome to print a web page and save it as PDF.
