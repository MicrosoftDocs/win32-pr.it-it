---
description: Nell'esempio seguente viene eseguito l'hashing di alcuni dati e viene firmato tale hash. In una seconda fase, l'hash e la relativa firma vengono verificati. L'hash è firmato con la chiave privata dell'utente e la chiave pubblica del firmatario viene esportata in modo da poter verificare la firma.
ms.assetid: 72f5d30a-efd5-4bf5-8057-cb73e5aa0514
title: 'Esempio di programma C: firma di un hash e verifica della firma hash'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000db2504b6a7046d040f6519f78de55e5b98c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401573"
---
# <a name="example-c-program-signing-a-hash-and-verifying-the-hash-signature"></a><span data-ttu-id="1aca2-105">Esempio di programma C: firma di un hash e verifica della firma hash</span><span class="sxs-lookup"><span data-stu-id="1aca2-105">Example C Program: Signing a Hash and Verifying the Hash Signature</span></span>

<span data-ttu-id="1aca2-106">Nell'esempio seguente viene eseguito l' [*hashing*](../secgloss/h-gly.md) di alcuni dati e viene firmato tale hash.</span><span class="sxs-lookup"><span data-stu-id="1aca2-106">The following example [*hashes*](../secgloss/h-gly.md) some data and signs that hash.</span></span> <span data-ttu-id="1aca2-107">In una seconda fase, l'hash e la relativa firma vengono verificati.</span><span class="sxs-lookup"><span data-stu-id="1aca2-107">In a second phase, the hash and its signature are verified.</span></span> <span data-ttu-id="1aca2-108">L'hash è firmato con la [*chiave privata*](../secgloss/p-gly.md)dell'utente e la [*chiave pubblica*](../secgloss/p-gly.md) del firmatario viene esportata in modo da poter verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="1aca2-108">The hash is signed with the user's [*private key*](../secgloss/p-gly.md), and the signer's [*public key*](../secgloss/p-gly.md) is exported so that the signature can be verified.</span></span>

<span data-ttu-id="1aca2-109">In questo esempio vengono illustrate le attività e le funzioni [*CryptoAPI*](../secgloss/c-gly.md) seguenti:</span><span class="sxs-lookup"><span data-stu-id="1aca2-109">This example illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="1aca2-110">Acquisizione di un CSP con [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="1aca2-110">Acquiring a CSP using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="1aca2-111">Recupero della coppia di chiavi di firma dell'utente \_ tramite [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).</span><span class="sxs-lookup"><span data-stu-id="1aca2-111">Getting the user's AT\_SIGNATURE key pair using [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).</span></span>
-   <span data-ttu-id="1aca2-112">Creazione di un PUBLICKEYBLOB con la chiave pubblica del firmatario da usare nel processo di verifica della firma usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="1aca2-112">Creating a PUBLICKEYBLOB with the signer's public key to be used in the signature verification process using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>
-   <span data-ttu-id="1aca2-113">Creazione di un oggetto hash con [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="1aca2-113">Creating a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span>
-   <span data-ttu-id="1aca2-114">Hashing dei dati con [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span><span class="sxs-lookup"><span data-stu-id="1aca2-114">Hashing the data using [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span></span>
-   <span data-ttu-id="1aca2-115">Firma dell'hash con [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha).</span><span class="sxs-lookup"><span data-stu-id="1aca2-115">Signing the hash using [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha).</span></span>
-   <span data-ttu-id="1aca2-116">Eliminazione definitiva dell'oggetto hash originale utilizzando [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash).</span><span class="sxs-lookup"><span data-stu-id="1aca2-116">Destroying the original hash object using [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash).</span></span>
-   <span data-ttu-id="1aca2-117">Rendere la chiave pubblica necessaria per verificare l'hash disponibile tramite [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="1aca2-117">Making the public key needed to verify the hash available using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>
-   <span data-ttu-id="1aca2-118">Ricreare l'oggetto hash usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) e [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span><span class="sxs-lookup"><span data-stu-id="1aca2-118">Re-creating the hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) and [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span></span>
-   <span data-ttu-id="1aca2-119">Verifica della firma sull'hash con [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea).</span><span class="sxs-lookup"><span data-stu-id="1aca2-119">Verifying the signature on the hash using [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea).</span></span>
-   <span data-ttu-id="1aca2-120">Esecuzione della pulizia normale.</span><span class="sxs-lookup"><span data-stu-id="1aca2-120">Performing normal cleanup.</span></span>


```C++
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example of signing a hash and 
// verifying the hash signature.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hProv;
BYTE *pbBuffer= (BYTE *)"The data that is to be hashed and signed.";
DWORD dwBufferLen = strlen((char *)pbBuffer)+1;
HCRYPTHASH hHash;
HCRYPTKEY hKey;
HCRYPTKEY hPubKey;
BYTE *pbKeyBlob;        
BYTE *pbSignature;
DWORD dwSigLen;
DWORD dwBlobLen;

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
   &hProv, 
   NULL, 
   NULL, 
   PROV_RSA_FULL, 
   0)) 
{
     printf("CSP context acquired.\n");
}
else
{
     MyHandleError("Error during CryptAcquireContext.");
}
//-------------------------------------------------------------------
// Get the public at signature key. This is the public key
// that will be used by the receiver of the hash to verify
// the signature. In situations where the receiver could obtain the
// sender's public key from a certificate, this step would not be
// needed.

if(CryptGetUserKey(   
   hProv,    
   AT_SIGNATURE,    
   &hKey)) 
{
    printf("The signature key has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptGetUserKey for signkey.");
}
//-------------------------------------------------------------------
// Export the public key. Here the public key is exported to a 
// PUBLICKEYBOLB so that the receiver of the signed hash can
// verify the signature. This BLOB could be written to a file and
// sent to another user.

if(CryptExportKey(   
   hKey,    
   NULL,    
   PUBLICKEYBLOB,
   0,    
   NULL, 
   &dwBlobLen)) 
{
     printf("Size of the BLOB for the public key determined. \n");
}
else
{
     MyHandleError("Error computing BLOB length.");
}
//-------------------------------------------------------------------
// Allocate memory for the pbKeyBlob.

if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Out of memory. \n");
}
//-------------------------------------------------------------------
// Do the actual exporting into the key BLOB.

if(CryptExportKey(   
   hKey, 
   NULL,    
   PUBLICKEYBLOB,    
   0,    
   pbKeyBlob,    
   &dwBlobLen))
{
     printf("Contents have been written to the BLOB. \n");
}
else
{
    MyHandleError("Error during CryptExportKey.");
}
//-------------------------------------------------------------------
// Create the hash object.

if(CryptCreateHash(
   hProv, 
   CALG_MD5, 
   0, 
   0, 
   &hHash)) 
{
     printf("Hash object created. \n");
}
else
{
    MyHandleError("Error during CryptCreateHash.");
}
//-------------------------------------------------------------------
// Compute the cryptographic hash of the buffer.

if(CryptHashData(
   hHash, 
   pbBuffer, 
   dwBufferLen, 
   0)) 
{
     printf("The data buffer has been hashed.\n");
}
else
{
     MyHandleError("Error during CryptHashData.");
}
//-------------------------------------------------------------------
// Determine the size of the signature and allocate memory.

dwSigLen= 0;
if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   NULL, 
   0, 
   NULL, 
   &dwSigLen)) 
{
     printf("Signature length %d found.\n",dwSigLen);
}
else
{
     MyHandleError("Error during CryptSignHash.");
}
//-------------------------------------------------------------------
// Allocate memory for the signature buffer.

if(pbSignature = (BYTE *)malloc(dwSigLen))
{
     printf("Memory allocated for the signature.\n");
}
else
{
     MyHandleError("Out of memory.");
}
//-------------------------------------------------------------------
// Sign the hash object.

if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   NULL, 
   0, 
   pbSignature, 
   &dwSigLen)) 
{
     printf("pbSignature is the hash signature.\n");
}
else
{
     MyHandleError("Error during CryptSignHash.");
}
//-------------------------------------------------------------------
// Destroy the hash object.

if(hHash) 
  CryptDestroyHash(hHash);

printf("The hash object has been destroyed.\n");
printf("The signing phase of this program is completed.\n\n");

//-------------------------------------------------------------------
// In the second phase, the hash signature is verified.
// This would most often be done by a different user in a
// separate program. The hash, signature, and the PUBLICKEYBLOB
// would be read from a file, an email message, 
// or some other source.

// Here, the original pbBuffer, pbSignature, szDescription. 
// pbKeyBlob, and their lengths are used.

// The contents of the pbBuffer must be the same data 
// that was originally signed.

//-------------------------------------------------------------------
// Get the public key of the user who created the digital signature 
// and import it into the CSP by using CryptImportKey. This returns
// a handle to the public key in hPubKey.

if(CryptImportKey(
   hProv,
   pbKeyBlob,
   dwBlobLen,
   0,
   0,
   &hPubKey))
{
     printf("The key has been imported.\n");
}
else
{
     MyHandleError("Public key import failed.");
}
//-------------------------------------------------------------------
// Create a new hash object.

if(CryptCreateHash(
   hProv, 
   CALG_MD5, 
   0, 
   0, 
   &hHash)) 
{
     printf("The hash object has been recreated. \n");
}
else
{
     MyHandleError("Error during CryptCreateHash.");
}
//-------------------------------------------------------------------
// Compute the cryptographic hash of the buffer.

if(CryptHashData(
   hHash, 
   pbBuffer, 
   dwBufferLen, 
   0)) 
{
     printf("The new hash has been created.\n");
}
else
{
     MyHandleError("Error during CryptHashData.");
}
//-------------------------------------------------------------------
// Validate the digital signature.

if(CryptVerifySignature(
   hHash, 
   pbSignature, 
   dwSigLen, 
   hPubKey,
   NULL, 
   0)) 
{
     printf("The signature has been verified.\n");
}
else
{
     printf("Signature not validated!\n");
}
//-------------------------------------------------------------------
// Free memory to be used to store signature.

if(pbSignature)
  free(pbSignature);

//-------------------------------------------------------------------
// Destroy the hash object.

if(hHash) 
  CryptDestroyHash(hHash);

//-------------------------------------------------------------------
// Release the provider handle.

if(hProv) 
   CryptReleaseContext(hProv, 0);
} //  End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the  
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
