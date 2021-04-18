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
# <a name="load-a-certificate-from-a-file"></a><span data-ttu-id="95086-103">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="95086-103">Load a Certificate from a File</span></span>

<span data-ttu-id="95086-104">In questo argomento viene descritto come caricare un certificato da un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="95086-104">This topic describes how to load a certificate from a certificate file.</span></span>

<span data-ttu-id="95086-105">Per caricare un certificato da un file di certificato</span><span class="sxs-lookup"><span data-stu-id="95086-105">To load a certificate from a certificate file</span></span>

1.  <span data-ttu-id="95086-106">Aprire il file del certificato per l'accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="95086-106">Open the certificate file for read access.</span></span>
2.  <span data-ttu-id="95086-107">Leggere il contenuto del file del certificato nel buffer del certificato.</span><span class="sxs-lookup"><span data-stu-id="95086-107">Read the contents of the certificate file into the certificate buffer.</span></span>
3.  <span data-ttu-id="95086-108">Creare un certificato utilizzando il contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="95086-108">Create a certificate using the contents of the buffer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95086-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95086-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95086-110">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="95086-110">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="95086-111">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="95086-111">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="95086-112">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="95086-112">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="95086-113">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="95086-113">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="95086-114">**Usato in questo esempio**</span><span class="sxs-lookup"><span data-stu-id="95086-114">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="95086-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="95086-115">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="95086-116">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="95086-116">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="95086-117">**CertCreateCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="95086-117">**CertCreateCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
</dt> <dt>

<span data-ttu-id="95086-118">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="95086-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="95086-119">API di crittografia</span><span class="sxs-lookup"><span data-stu-id="95086-119">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="95086-120">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="95086-120">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="95086-121">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="95086-121">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="95086-122">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="95086-122">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="95086-123">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="95086-123">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
