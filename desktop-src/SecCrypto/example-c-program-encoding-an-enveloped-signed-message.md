---
description: Crea, firma e busta un messaggio.
ms.assetid: 1d9d8a7a-0088-41a7-98fe-4f0e9cb21f31
title: 'Esempio di programma C: codifica di un messaggio firmato in busta'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5ae8008794dc7f8fa32f39543cf2ddc61827bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758348"
---
# <a name="example-c-program-encoding-an-enveloped-signed-message"></a><span data-ttu-id="16caa-103">Esempio di programma C: codifica di un messaggio firmato in busta</span><span class="sxs-lookup"><span data-stu-id="16caa-103">Example C Program: Encoding an Enveloped, Signed Message</span></span>

<span data-ttu-id="16caa-104">Nell'esempio seguente vengono creati, firmati e busti un messaggio e vengono illustrate le attività e le funzioni [*CryptoAPI*](../secgloss/c-gly.md) seguenti:</span><span class="sxs-lookup"><span data-stu-id="16caa-104">The following example creates, signs, and envelopes a message, and it illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="16caa-105">Acquisizione dell'handle di un CSP con [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="16caa-105">Acquiring the handle of a CSP using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="16caa-106">Apertura di un archivio di sistema tramite [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="16caa-106">Opening a system store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="16caa-107">Trovare un firmatario e i certificati del destinatario usando [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span><span class="sxs-lookup"><span data-stu-id="16caa-107">Finding a signer and recipient certificates using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="16caa-108">Inizializzazione delle strutture di dati appropriate per la firma di un messaggio in busta.</span><span class="sxs-lookup"><span data-stu-id="16caa-108">Initializing appropriate data structures for signing an enveloped message.</span></span>
-   <span data-ttu-id="16caa-109">Ricerca della lunghezza del messaggio in busta con [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).</span><span class="sxs-lookup"><span data-stu-id="16caa-109">Finding the length of the enveloped message using [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).</span></span>
-   <span data-ttu-id="16caa-110">Creazione e firma del messaggio tramite [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)e [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="16caa-110">Creating and signs the message using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), and [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>
-   <span data-ttu-id="16caa-111">Inviluppo del messaggio firmato e codificato per un ricevitore usando [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)e [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="16caa-111">Enveloping the signed and encoded message for a receiver using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), and [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>

<span data-ttu-id="16caa-112">Questo esempio avrà esito negativo se non esiste una chiave privata utilizzabile nel [*contenitore di chiavi*](../secgloss/k-gly.md)predefinito.</span><span class="sxs-lookup"><span data-stu-id="16caa-112">This example will fail if a usable private key does not exist in the default [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="16caa-113">Se la chiave privata necessaria non è disponibile, è possibile usare il codice che usa [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey), come illustrato nell'esempio di codice [C programma: invio e ricezione di un messaggio firmato e crittografato](example-c-program-sending-and-receiving-a-signed-and-encrypted-message.md).</span><span class="sxs-lookup"><span data-stu-id="16caa-113">If the needed private key is not available, code using [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey), as demonstrated in the code sample [Example C Program: Sending and Receiving a Signed and Encrypted Message](example-c-program-sending-and-receiving-a-signed-and-encrypted-message.md), can be used.</span></span>

<span data-ttu-id="16caa-114">In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="16caa-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="16caa-115">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="16caa-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="16caa-116">Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="16caa-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

BYTE* pbContent = (BYTE*) "Security is our only business.";
                                    // a byte pointer
DWORD cbContent = strlen((char *) pbContent)+1;
                                    // the size of the message
HCERTSTORE hStoreHandle;
HCRYPTPROV hCryptProv;
PCCERT_CONTEXT pSignerCert;         // signer's certificate
PCCERT_CONTEXT pRecipCert;          // receiver's certificate
LPWSTR pswzRecipientName = L"Hortense";
LPWSTR pswzCertSubject = L"Full Test Cert";
PCERT_INFO RecipCertArray[1];
DWORD ContentEncryptAlgSize;
CRYPT_ALGORITHM_IDENTIFIER ContentEncryptAlgorithm;
CMSG_ENVELOPED_ENCODE_INFO EnvelopedEncodeInfo;
DWORD cbEncodedBlob;
BYTE *pbEncodedBlob;
DWORD cbSignedBlob;
BYTE *pbSignedBlob;
HCRYPTMSG hMsg;
DWORD HashAlgSize;
CRYPT_ALGORITHM_IDENTIFIER HashAlgorithm;
CMSG_SIGNER_ENCODE_INFO SignerEncodeInfo;
CERT_BLOB SignerCertBlob;
CERT_BLOB SignerCertBlobArray[1];
CMSG_SIGNER_ENCODE_INFO SignerEncodeInfoArray[1];
CMSG_SIGNED_ENCODE_INFO SignedMsgEncodeInfo;

//-------------------------------------------------------------------
// Begin processing. Display the original message.

printf("The original message => %s\n",pbContent);  

//-------------------------------------------------------------------
// Acquire a cryptographic provider. 

if(CryptAcquireContext(
        &hCryptProv,      // address for handle to be returned
        NULL,             // use the current user's logon name
        NULL,             // use the default provider
        PROV_RSA_FULL,    // provider type
        0))               // zero allows access to private keys
{
    printf("Context CSP acquired. \n");
}
else
{
   if ( GetLastError() == NTE_BAD_KEYSET)
   {
        printf("A Usable private key was not found \n");
        printf("in the default key container. Either a \n");
        printf("private key must be generated in that container \n");
        printf("or CryptAquireCertificatePrivateKey can be used \n");
        printf("to gain access to the needed private key.");
   }
    MyHandleError("CryptAcquireContext failed.");
}
//-------------------------------------------------------------------
// Open the My system certificate store.

if(hStoreHandle = CertOpenStore(
       CERT_STORE_PROV_SYSTEM,
       0,
       NULL,
       CERT_SYSTEM_STORE_CURRENT_USER,
       L"MY"))
{
    printf("The MY system store is open. \n");
}
else
{
    MyHandleError( "Error getting store handle.");
}
//-------------------------------------------------------------------
// Get the signer's certificate. This certificate must be in the
// My store, and its private key must be available.

if(pSignerCert = CertFindCertificateInStore(
   hStoreHandle,
   MY_ENCODING_TYPE,
   0,
   CERT_FIND_SUBJECT_STR,
   pswzCertSubject,
   NULL))
{
    printf("Found certificate for %S.\n",pswzCertSubject);
}
else
{
    MyHandleError("Signer certificate not found.");
}
//-------------------------------------------------------------------
// Initialize the algorithm identifier structure.

HashAlgSize = sizeof(HashAlgorithm);
memset(&HashAlgorithm, 0, HashAlgSize);    // initialize to zero
HashAlgorithm.pszObjId = szOID_RSA_MD5;    // initialize the 
                                           // necessary member
//-------------------------------------------------------------------
// Initialize the CMSG_SIGNER_ENCODE_INFO structure.

memset(&SignerEncodeInfo, 0, sizeof(CMSG_SIGNER_ENCODE_INFO));
SignerEncodeInfo.cbSize = sizeof(CMSG_SIGNER_ENCODE_INFO);
SignerEncodeInfo.pCertInfo = pSignerCert->pCertInfo;
SignerEncodeInfo.hCryptProv = hCryptProv;
SignerEncodeInfo.dwKeySpec = AT_KEYEXCHANGE;
SignerEncodeInfo.HashAlgorithm = HashAlgorithm;
SignerEncodeInfo.pvHashAuxInfo = NULL;

//-------------------------------------------------------------------
// Create an array of one. 
// Note: The current program is set up for only a single signer.

SignerEncodeInfoArray[0] = SignerEncodeInfo;

//-------------------------------------------------------------------
// Initialize the CMSG_SIGNED_ENCODE_INFO structure.

SignerCertBlob.cbData = pSignerCert->cbCertEncoded;
SignerCertBlob.pbData = pSignerCert->pbCertEncoded;

//-------------------------------------------------------------------
// Initialize the array of one CertBlob.

SignerCertBlobArray[0] = SignerCertBlob;
memset(&SignedMsgEncodeInfo, 0, sizeof(CMSG_SIGNED_ENCODE_INFO));
SignedMsgEncodeInfo.cbSize = sizeof(CMSG_SIGNED_ENCODE_INFO);
SignedMsgEncodeInfo.cSigners = 1;
SignedMsgEncodeInfo.rgSigners = SignerEncodeInfoArray;
SignedMsgEncodeInfo.cCertEncoded = 1;
SignedMsgEncodeInfo.rgCertEncoded = SignerCertBlobArray;
SignedMsgEncodeInfo.rgCrlEncoded = NULL;

//-------------------------------------------------------------------
// Get the size of the encoded, signed message BLOB.

if(cbSignedBlob = CryptMsgCalculateEncodedLength(
    MY_ENCODING_TYPE,       // message encoding type
    0,                      // flags
    CMSG_SIGNED,            // message type
    &SignedMsgEncodeInfo,   // pointer to structure
    NULL,                   // inner content OID
    cbContent))             // size of content
{
    printf("%d, the length of data calculated. \n",cbSignedBlob);
}
else
{
   if ( GetLastError() == NTE_BAD_KEYSET)
   {
        printf("A Usable private key was not found \n");
        printf("in the default key container. Either a \n");
        printf("private key must be generated in that container \n");
        printf("or CryptAquireCertificatePRivateKey can be used \n");
        printf("to gain access to the needed private key.");
    }
    MyHandleError("Getting cbSignedBlob length failed.");
}
//-------------------------------------------------------------------
// Allocate memory for the encoded BLOB.

if(pbSignedBlob = (BYTE *) malloc(cbSignedBlob))
{
   printf("Memory has been allocated for the signed message. \n");
}
else
{
   MyHandleError("Memory allocation failed.");
}
//-------------------------------------------------------------------
// Open a message to encode.

if(hMsg = CryptMsgOpenToEncode(
    MY_ENCODING_TYPE,        // encoding type
    0,                       // flags
    CMSG_SIGNED,             // message type
    &SignedMsgEncodeInfo,    // pointer to structure
    NULL,                    // inner content OID
    NULL))                   // stream information (not used)
{
    printf("The message to be encoded has been opened. \n");
}
else
{
    MyHandleError("OpenToEncode failed.");
}
//-------------------------------------------------------------------
// Update the message with the data.

if(CryptMsgUpdate(
     hMsg,         // handle to the message
     pbContent,    // pointer to the content
     cbContent,    // size of the content
     TRUE))        // last call
{
    printf("Content has been added to the encoded message. \n");
}
else
{
    MyHandleError("MsgUpdate failed.");
}
//-------------------------------------------------------------------
// Get the resulting message.

if(CryptMsgGetParam(
    hMsg,                      // handle to the message
    CMSG_CONTENT_PARAM,        // parameter type
    0,                         // index
    pbSignedBlob,              // pointer to the BLOB
    &cbSignedBlob))            // size of the BLOB
{
    printf("Message encoded successfully. \n");
}
else
{
    MyHandleError("MsgGetParam failed.");
}
//-------------------------------------------------------------------
// pbSignedBlob now points to the encoded, signed content.

//-------------------------------------------------------------------
// Get a pointer to the recipient certificate.
// For this program, the recipient's certificate must also be in the
// My store. At this point, only the recipient's public key is needed.
// To open the enveloped message, however, the recipient's 
// private key must also be available.

if(pRecipCert=CertFindCertificateInStore(      
      hStoreHandle,
      MY_ENCODING_TYPE,            // use X509_ASN_ENCODING
      0,                           // no dwFlags needed
      CERT_FIND_SUBJECT_STR,       // find a certificate with a
                                   // subject that matches the 
                                   // string in the next parameter
      pswzRecipientName,           // the Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // in all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
     printf("Certificate for %S found. \n", pswzRecipientName);
}
else
{
     MyHandleError("Could not find the countersigner's "
         "certificate.");
}
//-------------------------------------------------------------------
// Initialize the first element of the array of CERT_INFOs. 
// In this example, there is only a single recipient.

RecipCertArray[0] = pRecipCert->pCertInfo;

//-------------------------------------------------------------------
// Initialize the symmetric-encryption algorithm identifier
// structure.

ContentEncryptAlgSize = sizeof(ContentEncryptAlgorithm);
memset(&ContentEncryptAlgorithm, 
       0,
       ContentEncryptAlgSize);               // initialize to zero

//-------------------------------------------------------------------
// Initialize the necessary members. This particular OID does not
// need any parameters. Some OIDs, however, will require that
// the other members be initialized.

ContentEncryptAlgorithm.pszObjId = szOID_RSA_RC4;

//-------------------------------------------------------------------
// Initialize the CMSG_ENVELOPED_ENCODE_INFO structure.

memset(&EnvelopedEncodeInfo, 
       0,
       sizeof(CMSG_ENVELOPED_ENCODE_INFO));
EnvelopedEncodeInfo.cbSize = sizeof(CMSG_ENVELOPED_ENCODE_INFO);
EnvelopedEncodeInfo.hCryptProv = hCryptProv;
EnvelopedEncodeInfo.ContentEncryptionAlgorithm = 
                                        ContentEncryptAlgorithm;
EnvelopedEncodeInfo.pvEncryptionAuxInfo = NULL;
EnvelopedEncodeInfo.cRecipients = 1;
EnvelopedEncodeInfo.rgpRecipients = RecipCertArray;

//-------------------------------------------------------------------
// Get the size of the encoded message BLOB.

if(cbEncodedBlob = CryptMsgCalculateEncodedLength(
     MY_ENCODING_TYPE,        // message encoding type
     0,                       // flags
     CMSG_ENVELOPED,          // message type
     &EnvelopedEncodeInfo,    // pointer to structure
     szOID_RSA_signedData,    // inner content OID
     cbSignedBlob))           // size of content
{
    printf("Length of the encoded BLOB will be %d.\n",cbEncodedBlob);
}
else
{
    MyHandleError("Getting enveloped cbEncodedBlob length failed.");
}
//--------------------------------------------------------------------
// Allocate memory for the encoded BLOB.

if(pbEncodedBlob = (BYTE *) malloc(cbEncodedBlob))
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Enveloped malloc operation failed.");
}
//-------------------------------------------------------------------
// Open a message to encode.

if(hMsg = CryptMsgOpenToEncode(
     MY_ENCODING_TYPE,        // encoding type
     0,                       // flags
     CMSG_ENVELOPED,          // message type
     &EnvelopedEncodeInfo,    // pointer to structure
     szOID_RSA_signedData,    // inner content OID
     NULL))                   // stream information (not used)
{
    printf("The message to encode is open. \n");
}
else
{
    MyHandleError("Enveloped OpenToEncode failed.");
}
//-------------------------------------------------------------------
// Update the message with the data.

if(CryptMsgUpdate(
     hMsg,              // handle to the message
     pbSignedBlob,      // pointer to the signed data BLOB
     cbSignedBlob,      // size of the data BLOB
     TRUE))             // last call
{
    printf("The signed BLOB has been added to the message. \n");
}
else
{
    MyHandleError("Enveloped MsgUpdate failed.");
}
//-------------------------------------------------------------------
// Get the resulting message.

if(CryptMsgGetParam(
     hMsg,                  // handle to the message
     CMSG_CONTENT_PARAM,    // parameter type
     0,                     // index
     pbEncodedBlob,         // pointer to the enveloped,
                            // signed data BLOB
     &cbEncodedBlob))       // size of the BLOB
{
    printf("Enveloped message encoded successfully. \n");
}
else
{
    MyHandleError("Enveloped MsgGetParam failed.");
}
//-------------------------------------------------------------------
// Clean up.

CertFreeCertificateContext(pRecipCert);
if(CertCloseStore(
     hStoreHandle,
     CERT_CLOSE_STORE_CHECK_FLAG))
{
  printf("The certificate store closed without a certificate "
      "left open. \n");
}
else
{
  printf("The store closed but a certificate was still open. \n");
}
if(hMsg)
   CryptMsgClose(hMsg);
if(hCryptProv) 
   CryptReleaseContext(hCryptProv,0);
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
