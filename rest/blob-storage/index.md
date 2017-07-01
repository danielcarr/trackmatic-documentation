# Blob Storage Api

The blob storage api provides a mechanism for callers to store or retrieve arbitrary unstructured data.

## Open Api Documentation
For more information on available calls and messages structure [goto the open api docs](./open-api)

## Storing a file

To store a file you need to perform an HTTP post with the Content-Type header set to "multipart/form-data". The endpoint expects one file per request. The file id must be provided by the caller. The following is required for a successfull upload

```
POST /api/v2/blob-storage/{organisationId}/{fileId}
```

- A uniuque id must be provided in the url. If a file already exists with the supplied if an error will be thrown.
- The Content-Type of the file must be provided and must be part of the supported content types listed below.
- An organisation id which your token grants access to must be provided in the url

### Supported Content types

```
    "application/xml",
    "application/pdf",
    "image/gif",
    "image/png",
    "image/jpeg",
    "image/bmp",
    "image/webp",
    "text/plain",
    "audio/midi",
    "audio/mpeg",
    "audio/webm",
    "audio/ogg",
    "audio/wav",
    "video/webm",
    "video/ogg"
```

## Retrieving a file

A file can be retrieved via an Http GET to the same URL used in the upload. A valid JWT token must be present.

```
GET /api/v2/blob-storage/{organisationId}/{fileId}
```

## Error Codes

|Http Status Code|Error Code|Description|
|----------------|----------|-----------|
|400|1|File already exists|
|400|2|No file supplied|
|400|3|Content type not provided|
|400|4|Content type not supported|

