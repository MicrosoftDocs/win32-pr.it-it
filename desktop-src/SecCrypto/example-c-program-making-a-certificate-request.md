---
description: Nell'esempio seguente viene illustrata la procedura descritta nella sezione precedente. In questo esempio viene creata una semplice richiesta di certificato con un solo firmatario, un singolo attributo relativo del nome distinto relativo (RDN) e nessun attributo generale.
ms.assetid: bd3d0259-f0e8-460e-9f18-95d2492da3d8
title: 'Esempio di programma C: creazione di una richiesta di certificato'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e02d9faa51d405f02bb46729621f65d43c7ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529574"
---
# <a name="example-c-program-making-a-certificate-request"></a><span data-ttu-id="03e6b-104">Esempio di programma C: creazione di una richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="03e6b-104">Example C Program: Making a Certificate Request</span></span>

<span data-ttu-id="03e6b-105">Nell'esempio seguente viene illustrata la procedura descritta nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="03e6b-105">The following example demonstrates the procedure outlined in the previous section.</span></span> <span data-ttu-id="03e6b-106">In questo esempio viene creata una semplice [*richiesta di certificato*](../secgloss/c-gly.md) con un solo firmatario, un singolo attributo [*relativo del nome distinto relativo*](../secgloss/r-gly.md) (RDN) e nessun [*attributo*](../secgloss/a-gly.md)generale.</span><span class="sxs-lookup"><span data-stu-id="03e6b-106">This example creates a simple [*certificate request*](../secgloss/c-gly.md) with one signer, a single [*relative distinguished name*](../secgloss/r-gly.md) (RDN) [*attribute*](../secgloss/a-gly.md), and no general attributes.</span></span>

<span data-ttu-id="03e6b-107">In questo esempio vengono illustrate le funzioni [*CryptoAPI*](../secgloss/c-gly.md) seguenti:</span><span class="sxs-lookup"><span data-stu-id="03e6b-107">This example illustrates the following [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   [<span data-ttu-id="03e6b-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="03e6b-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [<span data-ttu-id="03e6b-109">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="03e6b-109">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [<span data-ttu-id="03e6b-110">**CryptExportPublicKeyInfo**</span><span class="sxs-lookup"><span data-stu-id="03e6b-110">**CryptExportPublicKeyInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo)
-   [<span data-ttu-id="03e6b-111">**CryptSignAndEncodeCertificate**</span><span class="sxs-lookup"><span data-stu-id="03e6b-111">**CryptSignAndEncodeCertificate**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate)

<span data-ttu-id="03e6b-112">Questo esempio usa anche le funzioni [**ByteToStr**](bytetostr.md) e [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="03e6b-112">This example also uses the functions [**ByteToStr**](bytetostr.md) and [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="03e6b-113">Il codice per queste funzioni è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="03e6b-113">Code for these functions is included with the sample.</span></span> <span data-ttu-id="03e6b-114">[Per utilizzo generico Functions](general-purpose-functions.md) elenca il codice per queste e altre funzioni ausiliarie.</span><span class="sxs-lookup"><span data-stu-id="03e6b-114">[General Purpose Functions](general-purpose-functions.md) lists code for these and other auxiliary functions.</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This example demonstrates how to create and encode a 
// certificate request. 
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
//   This program use this additional #define statement. 

#define CERT_SUBJECT_NAME "This certificate user"

//-------------------------------------------------------------------
// This program uses the function ByteToStr to convert an array
// of BYTEs to a char string. 

void ByteToStr(
     DWORD cb, 
     void* pv, 
     LPSTR sz)
//-------------------------------------------------------------------
// Parameters passed are:
//    pv is the array of BYTEs to be converted.
//    cb is the number of BYTEs in the array.
//    sz is a pointer to the string to be returned.

{
//-------------------------------------------------------------------
//  Declare and initialize local variables.

BYTE* pb = (BYTE*) pv; // local pointer to a BYTE in the BYTE array
DWORD i;               // local loop counter
int b;                 // local variable

//-------------------------------------------------------------------
//  Begin processing loop.

for (i = 0; i<cb; i++)
{
   b = (*pb & 0xF0) >> 4;
   *sz++ = (b <= 9) ? b + '0' : (b - 10) + 'A';
   b = *pb & 0x0F;
   *sz++ = (b <= 9) ? b + '0' : (b - 10) + 'A';
   pb++;
}
*sz++ = 0;
}

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables 

// Declare and initialize a CERT_RDN_ATTR array.
// In this code, only one array element is used.

CERT_RDN_ATTR rgNameAttr[] = {
        "2.5.4.3",                             // pszObjId 
        CERT_RDN_PRINTABLE_STRING,             // dwValueType
        strlen(CERT_SUBJECT_NAME),             // value.cbData
        (BYTE*)CERT_SUBJECT_NAME};             // value.pbData

//-------------------------------------------------------------------
// Declare and initialize a CERT_RDN array.
// In this code, only one array element is used.

CERT_RDN rgRDN[] = {
         1,                 // rgRDN[0].cRDNAttr
         &rgNameAttr[0]};   // rgRDN[0].rgRDNAttr

//-------------------------------------------------------------------
// Declare and initialize a CERT_NAME_INFO structure.

CERT_NAME_INFO Name = {
           1,                  // Name.cRDN
           rgRDN};             // Name.rgRDN

//-------------------------------------------------------------------
// Declare and initialize all other variables and structures.

CERT_REQUEST_INFO  CertReqInfo;
CERT_NAME_BLOB  SubjNameBlob;
DWORD  cbNameEncoded;
BYTE*  pbNameEncoded;
HCRYPTPROV  hCryptProv;
DWORD  cbPublicKeyInfo;
CERT_PUBLIC_KEY_INFO*  pbPublicKeyInfo;
DWORD  cbEncodedCertReqSize;
CRYPT_OBJID_BLOB  Parameters;
CRYPT_ALGORITHM_IDENTIFIER  SigAlg;
BYTE*  pbSignedEncodedCertReq;
char*  pSignedEncodedCertReqBlob;

//-------------------------------------------------------------------
//    Begin processing.

if(CryptEncodeObject(
    MY_ENCODING_TYPE,     // Encoding type
    X509_NAME,            // Structure type
    &Name,                // Address of CERT_NAME_INFO structure
    NULL,                 // pbEncoded
    &cbNameEncoded))      // pbEncoded size
{
    printf("The first call to CryptEncodeObject succeeded. \n");
}
else
{
    MyHandleError("The first call to CryptEncodeObject failed. \n" 
        "A public/private key pair may not exit in the container. \n");
}
//-------------------------------------------------------------------
//     Allocate memory for the encoded name.

if(!(pbNameEncoded = (BYTE*)malloc(cbNameEncoded)))
    MyHandleError("The pbNamencoded malloc operation failed. \n");

//-------------------------------------------------------------------
//  Call CryptEncodeObject to do the actual encoding of the name.

if(CryptEncodeObject(
        MY_ENCODING_TYPE,    // Encoding type
        X509_NAME,           // Structure type
        &Name,               // Address of CERT_NAME_INFO structure
        pbNameEncoded,       // pbEncoded
        &cbNameEncoded))     // pbEncoded size
{
    printf("The object is encoded. \n");
}
else
{
    free(pbNameEncoded);
    MyHandleError("The second call to CryptEncodeObject failed. \n");
}
//-------------------------------------------------------------------
// Set the subject member of CertReqInfo to point to 
// a CERT_NAME_INFO structure that 
// has been initialized with the data from cbNameEncoded
// and pbNameEncoded.

SubjNameBlob.cbData = cbNameEncoded;
SubjNameBlob.pbData = pbNameEncoded;
CertReqInfo.Subject = SubjNameBlob;

//-------------------------------------------------------------------
// Generate custom information. This step is not
// implemented in this code.

CertReqInfo.cAttribute = 0;
CertReqInfo.rgAttribute = NULL;
CertReqInfo.dwVersion = CERT_REQUEST_V1;

//-------------------------------------------------------------------
//    Call CryptExportPublicKeyInfo to return an initialized
//    CERT_PUBLIC_KEY_INFO structure.
//    First, get a cryptographic provider.

if(CryptAcquireContext(
    &hCryptProv,        // Address for handle to be returned.
    NULL,               // Use the current user's logon name.
    NULL,               // Use the default provider.
    PROV_RSA_FULL,      // Need to both encrypt and sign.
    NULL))              // No flags needed.
{
     printf("A cryptographic provider has been acquired. \n");
}
else
{
    free(pbNameEncoded);
    MyHandleError("CryptAcquireContext failed. \n");
}
//-------------------------------------------------------------------
// Call CryptExportPublicKeyInfo to get the size of the returned
// information.

if(CryptExportPublicKeyInfo(
          hCryptProv,            // Provider handle
          AT_SIGNATURE,          // Key spec
          MY_ENCODING_TYPE,      // Encoding type
          NULL,                  // pbPublicKeyInfo
          &cbPublicKeyInfo))     // Size of PublicKeyInfo
{
     printf("The keyinfo structure is %d bytes. \n",cbPublicKeyInfo);
}
else
{
    free(pbNameEncoded);
    MyHandleError("The first call to CryptExportPublickKeyInfo failed. \n"
                  "The probable cause is that \n"
                  "there is no key pair in the key container. \n");
}
//-------------------------------------------------------------------
// Allocate the necessary memory.

if(pbPublicKeyInfo = 
   (CERT_PUBLIC_KEY_INFO*)malloc(cbPublicKeyInfo))
{
    printf("Memory is allocated for the public key structure. \n");
}
else
{
    free(pbNameEncoded);
    MyHandleError("Memory allocation failed. \n");
}
//-------------------------------------------------------------------
// Call CryptExportPublicKeyInfo to get pbPublicKeyInfo.

if(CryptExportPublicKeyInfo(
          hCryptProv,            // Provider handle
          AT_SIGNATURE,          // Key spec
          MY_ENCODING_TYPE,      // Encoding type
          pbPublicKeyInfo,       // pbPublicKeyInfo
          &cbPublicKeyInfo))     // Size of PublicKeyInfo
{
     printf("The key has been exported. \n");
}
else
{
    free(pbNameEncoded);
    free(pbPublicKeyInfo);
    MyHandleError("The second call to CryptExportPublicKeyInfo failed. \n");
}
//-------------------------------------------------------------------
// Set the SubjectPublicKeyInfo member of the 
// CERT_REQUEST_INFO structure to point to the CERT_PUBLIC_KEY_INFO 
// structure created.

CertReqInfo.SubjectPublicKeyInfo = *pbPublicKeyInfo;

memset(&Parameters, 0, sizeof(Parameters));
SigAlg.pszObjId = szOID_OIWSEC_sha1RSASign;
SigAlg.Parameters = Parameters;

//-------------------------------------------------------------------
// Call CryptSignAndEncodeCertificate to get the size of the
// returned BLOB. The dwKeySpec argument should match the KeySpec
// (AT_SIGNATURE or AT_KEYEXCHANGE) used to create the private
// key. Here, AT_KEYEXCHANGE is assumed.

if(CryptSignAndEncodeCertificate(
          hCryptProv,                      // Crypto provider
          AT_KEYEXCHANGE,                  // Key spec
          MY_ENCODING_TYPE,                // Encoding type
          X509_CERT_REQUEST_TO_BE_SIGNED,  // Structure type
          &CertReqInfo,                    // Structure information
          &SigAlg,                         // Signature algorithm
          NULL,                            // Not used
          NULL,                            // pbSignedEncodedCertReq
          &cbEncodedCertReqSize))          // Size of certificate 
                                           // required
{
    printf("The size of the encoded certificate is set. \n");
}
else
{
    free(pbNameEncoded);
    free(pbPublicKeyInfo);
    MyHandleError("First call to CryptSignandEncode failed. \n");
}
//-------------------------------------------------------------------
// Allocate memory for the encoded certificate request.

if(pbSignedEncodedCertReq = (BYTE*)malloc(cbEncodedCertReqSize))
{
    printf("Memory has been allocated.\n");
}
else
{
    free(pbNameEncoded);
    free(pbPublicKeyInfo);
    MyHandleError("The malloc operation failed. \n");
}
//-------------------------------------------------------------------
// Call CryptSignAndEncodeCertificate to get the 
// returned BLOB.

if(CryptSignAndEncodeCertificate(
          hCryptProv,                     // Crypto provider
          AT_KEYEXCHANGE,                 // Key spec
          MY_ENCODING_TYPE,               // Encoding type
          X509_CERT_REQUEST_TO_BE_SIGNED, // Struct type
          &CertReqInfo,                   // Struct info        
          &SigAlg,                        // Signature algorithm
          NULL,                           // Not used
          pbSignedEncodedCertReq,         // Pointer
          &cbEncodedCertReqSize))         // Length of the message
{
     printf("The message is encoded and signed. \n");
}
else
{
    free(pbNameEncoded);
    free(pbPublicKeyInfo);
    free(pbSignedEncodedCertReq);
    MyHandleError("The second call to CryptSignAndEncode failed. \n");
}
//-------------------------------------------------------------------
// View the signed and encoded certificate request BLOB.

pSignedEncodedCertReqBlob = 
                        new char[(cbEncodedCertReqSize *2) +1];

//-------------------------------------------------------------------
// Call ByteToStr, one of the general purpose functions, to convert 
// the byte BLOB to ASCII hexadecimal format. 

ByteToStr(cbEncodedCertReqSize,
          pbSignedEncodedCertReq,
          pSignedEncodedCertReqBlob);

//-------------------------------------------------------------------
// Print the string.
printf("The string created is: \n");
printf("%s\n",pSignedEncodedCertReqBlob);

//-------------------------------------------------------------------
// Free memory.

free(pbNameEncoded);
free(pbPublicKeyInfo);
free(pbSignedEncodedCertReq);
CryptReleaseContext(hCryptProv,0);

printf("\nMemory freed. Program ran without error. \n");
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to  
//  the standard error (stderr) file and exit the program. 
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



 

 
