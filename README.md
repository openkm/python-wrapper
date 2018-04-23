# PyOKM
Python wrapper of the OpenKM RESTful API.

---
## Install
Go to the downloaded folder and execute on command line:

```sudo python setup.py install```

## Use 
To use the package, you can import it with:

```python
from OKMObjects.okmDocument import OkmDocument
```

Now, you only have to create a new OkmDocument and call the methods that you need.

```python
mDocumentAPI = OkmDocument('username', 'password', 'http://<localhost>:8080/OpenKM')

mDocumentAPI.getDocument('<document-route>', '<destination-name>')
mDocumentAPI.deleteDocument('<document-route>')
```

## Methods
The methods that are available to use in this package are

### deleteDocument(srcPath)
@srcPath could be the UUID or the route of the file in the OKM Server.

This method deletes a concrete document.

### getDocument(srcPath, dstName)
@srcPath could be the UUID or the route of the file in the OKM Server.
@dstName is the name that the file will have in our computer.

This method downloads a concrete document.

### getDocumentProperties(srcPath)
@srcPath could be the UUID or the route of the file in the OKM Server.

This method downloads the properties of a concrete document into a JSON file.

### getDocumentVersionHistory(srcPath)
@srcPath could be the UUID or the route of the file in the OKM Server.

This method downloads the versions history of a concrete document into a JSON file.

### copyDocument(srcPath, dstPath)
@srcPath could be the UUID or the route of the file in the OKM Server.
@dstPath is the route of the file in the OKM Server.

This method duplicates the document into the destination path.

### moveDocument(srcPath, dstPath)
@srcPath could be the UUID or the route of the file in the OKM Server.
@dstPath is the route of the file in the OKM Server.

This method moves the document into the destination path.

### uploadDocument(srcPatch, dstName)
@srcPath is the local route of the file in our computer.
@dstName is the name that the file will have in the OKM Server

This method uploads a document to our server.
