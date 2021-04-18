---
description: In questo argomento viene descritto come caricare un certificato da un file di certificato.
ms.assetid: 60cced55-9fcc-4fce-a462-7abf3f4466f0
title: Caricare un certificato da un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c708fb042ccdf4acd43986de1404f9ccb266148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318365"
---
# <a name="load-a-certificate-from-a-file"></a>Caricare un certificato da un file

In questo argomento viene descritto come caricare un certificato da un file di certificato.

Per caricare un certificato da un file di certificato

1.  Aprire il file del certificato per l'accesso in lettura.
2.  Leggere il contenuto del file del certificato nel buffer del certificato.
3.  Creare un certificato utilizzando il contenuto del buffer.


```C++
// In the interest of simplicity, this example
//  uses a fixed-length buffer to hold the certificate. 
// A more robust solution would be to query the size
//  of the certificate file and dynamically
//  allocate a buffer of that size or greater.
#define CERTIFICATE_BUFFER_SIZE 1024

HRESULT  hr                  = S_OK;
BYTE     certEncoded[CERTIFICATE_BUFFER_SIZE] = {0};
DWORD    certEncodedSize     = 0L;
HANDLE   certFileHandle      = NULL;
BOOL     result              = FALSE;

// open the certificate file
certFileHandle = CreateFile(certFile, 
    GENERIC_READ, 
    0, 
    NULL, 
    OPEN_EXISTING, 
    FILE_ATTRIBUTE_NORMAL, 
    NULL);
if (INVALID_HANDLE_VALUE == certFileHandle) {
    hr = HRESULT_FROM_WIN32(GetLastError());
}

if (SUCCEEDED(hr)) {
    // if the buffer is large enough
    //  read the certificate file into the buffer
    if (GetFileSize (certFileHandle, NULL) <= CERTIFICATE_BUFFER_SIZE) {
        result = ReadFile(certFileHandle, 
            certEncoded, 
            CERTIFICATE_BUFFER_SIZE, 
            &certEncodedSize, 
            NULL);
        if (!result) {
            // the read failed, return the error as an HRESULT
            hr = HRESULT_FROM_WIN32(GetLastError());
        } else {
            hr = S_OK;
        }
    } else {
        // The certificate file is larger than the allocated buffer.
        //  To handle this error, you could dynamically allocate
        //  the certificate buffer based on the file size returned or 
        //  use a larger static buffer.
        hr = HRESULT_FROM_WIN32(ERROR_MORE_DATA);
    }    
}
if (SUCCEEDED(hr))
{
    // create a certificate from the contents of the buffer
    *cert = CertCreateCertificateContext(X509_ASN_ENCODING, 
        certEncoded, 
        certEncodedSize);
    if (!(*cert)) {
        hr = HRESULT_FROM_WIN32(GetLastError());
        CloseHandle(certFileHandle);
        hr = E_FAIL;
    } else {
        hr = S_OK;
    }
}
// close the certificate file
if (NULL != certFileHandle) CloseHandle(certFileHandle);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Usato in questo esempio**
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[**CertCreateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[API di crittografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Errori dell'API firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori del documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
