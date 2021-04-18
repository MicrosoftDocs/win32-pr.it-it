---
description: hashing e codifica un messaggio di testo, quindi decodifica e verifica il messaggio.
ms.assetid: effe4080-63c1-4f35-a5e3-e7e60754b28f
title: 'Esempio di programma C: codifica e decodifica di un messaggio con hash'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5904a684d02a81acba1502162c779b9f124d3dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316173"
---
# <a name="example-c-program-encoding-and-decoding-a-hashed-message"></a>Esempio di programma C: codifica e decodifica di un messaggio con hash

Nell'esempio seguente viene eseguito l' [*hashing*](../secgloss/h-gly.md) e viene codificato un messaggio di testo, quindi viene decodificato e verificato il messaggio.

Sebbene, per semplicità, le due funzioni diverse siano state combinate in questo esempio, in un'impostazione più realistica le due parti verrebbero utilizzate separatamente.

In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:

-   Chiamata di [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per acquisire un provider CSP.
-   Utilizzo di [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per calcolare la lunghezza del messaggio codificato.
-   Allocazione della memoria per un buffer per memorizzare i dati codificati.
-   Apertura di un messaggio da codificare tramite [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).
-   Aggiunta di contenuto al messaggio da codificare tramite [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).
-   Utilizzo di [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per copiare il messaggio codificato nel buffer allocato.
-   Apertura di un messaggio da decodificare con [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).
-   Aggiunta del messaggio codificato al messaggio da decodificare con [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).
-   Creazione di un puntatore duplicato al messaggio mediante [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate).
-   Verifica del tipo di messaggio con [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).
-   Utilizzo di [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per decodificare il messaggio.
-   Verifica dell'hash con [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).
-   Utilizzo di [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per rilasciare l'handle del messaggio.
-   Uso di [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) per rilasciare il CSP.

In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md). Il codice per questa funzione è incluso nell'esempio.

Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).


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
//  Copyright (C) Microsoft.  All rights reserved.
//  Declare and initialize variables. This includes creating a 
//  pointer to the message content. In real situations, 
//  the message content will usually exist somewhere and a pointer
//  to it will get passed to the application. 

BYTE* pbContent = (BYTE*) "A razzle-dazzle hashed message \n"
       "Hashing is better than trashing. \n";    // The message
DWORD cbContent = strlen((char *)pbContent)+1;  // Size of message
                                                // including the  
                                                // final NULL.
HCRYPTPROV hCryptProv;                          // CSP handle
DWORD HashAlgSize;
CRYPT_ALGORITHM_IDENTIFIER HashAlgorithm;
CMSG_HASHED_ENCODE_INFO HashedEncodeInfo;
DWORD cbEncodedBlob;
BYTE *pbEncodedBlob;
HCRYPTMSG hMsg;
HCRYPTMSG hDupMsg;
//-------------------------------------------------------------------
//  Variables to be used in decoding.
DWORD cbData = sizeof(DWORD);
DWORD dwMsgType;
DWORD cbDecoded;
BYTE  *pbDecoded;

//-------------------------------------------------------------------
//  Begin processing.

printf("Begin processing. \n");
printf("The message to be hashed and encoded is: \n");
printf("%s\n",pbContent);    // Display original message.
printf("The starting message length is %d\n",cbContent);

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
               &hCryptProv,     // Address for the handle. 
               NULL,            // Use the current user's logon name.
               NULL,            // Use the default provider.
               PROV_RSA_FULL,   // Provider type.
               0))              // Zero allows access to
                                // private keys.
{
    printf("A CSP context has been acquired. \n");
}
else
{
    MyHandleError("CryptAcquireContext failed.");
}
//-------------------------------------------------------------------
// The function succeeded; hCryptProv is the CSP handle.

//-------------------------------------------------------------------
// Initialize the algorithm identifier structure.

HashAlgSize = sizeof(HashAlgorithm);
memset(&HashAlgorithm, 0, HashAlgSize);   // Initialize to zero.
HashAlgorithm.pszObjId = szOID_RSA_MD5;   // Then set the 
                                          //   necessary member.

//-------------------------------------------------------------------
// Initialize the CMSG_HASHED_ENCODE_INFO structure.

memset(&HashedEncodeInfo, 0, sizeof(CMSG_HASHED_ENCODE_INFO));
HashedEncodeInfo.cbSize = sizeof(CMSG_HASHED_ENCODE_INFO);
HashedEncodeInfo.hCryptProv = hCryptProv;
HashedEncodeInfo.HashAlgorithm = HashAlgorithm;
HashedEncodeInfo.pvHashAuxInfo = NULL;

//-------------------------------------------------------------------
// Get the size of the encoded message BLOB.

if(cbEncodedBlob = CryptMsgCalculateEncodedLength(
                     MY_ENCODING_TYPE,     // Message encoding type
                     0,                    // Flags
                     CMSG_HASHED,          // Message type
                     &HashedEncodeInfo,    // Pointer to structure
                     NULL,                 // Inner content object ID
                     cbContent))           // Size of content
{
    printf("The length to be allocated is %d bytes.\n",
        cbEncodedBlob);
}
else
{
    MyHandleError("Getting cbEncodedBlob length failed");
}
//-------------------------------------------------------------------
// Allocate memory for the encoded BLOB.
if(pbEncodedBlob = (BYTE *) malloc(cbEncodedBlob))
{
    printf("%d bytes of memory have been allocated.\n",
        cbEncodedBlob);
}
else
{
    MyHandleError("Malloc operation failed.");
}
//-------------------------------------------------------------------
// Open a message to encode.

if(hMsg = CryptMsgOpenToEncode(
            MY_ENCODING_TYPE,        // Encoding type
            0,                       // Flags
            CMSG_HASHED,             // Message type
            &HashedEncodeInfo,       // Pointer to structure
            NULL,                    // Inner content object ID
            NULL))                   // Stream information (not used)
{
    printf("The message to encode has been opened. \n");
}
else
{
    MyHandleError("OpenToEncode failed");
}
//-------------------------------------------------------------------
// Update the message with the data.

if(CryptMsgUpdate(
            hMsg,          // Handle to the message
            pbContent,     // Pointer to the content
            cbContent,     // Size of the content
            TRUE))         // Last call
{
    printf("Data has been added to the message to encode. \n");
}
else
{
    MyHandleError("MsgUpdate failed");
}
//-------------------------------------------------------------------
// Create a duplicate of the message.

if(hDupMsg = CryptMsgDuplicate(hMsg))
{
     printf("The message has been duplicated.\n");
}
else
{
     MyHandleError("Duplication of the message failed.");
}

//-------------------------------------------------------------------
// Get the resulting message from the duplicate of the message.

if(CryptMsgGetParam(
               hDupMsg,                  // Handle to the message
               CMSG_CONTENT_PARAM,       // Parameter type
               0,                        // Index
               pbEncodedBlob,            // Pointer to the BLOB
               &cbEncodedBlob))          // Size of the BLOB
{
     printf("Message encoded successfully. \n");
}
else    
{
    MyHandleError("MsgGetParam failed");
}
//-------------------------------------------------------------------
// Close both messages to prepare for decoding.

CryptMsgClose(hMsg);
CryptMsgClose(hDupMsg);

// The following code decodes the hashed message.
// Usually, this would be in a separate program and the encoded,
// hashed data would be input from a file, from an email message, 
// or from some other source.
//
// The variables used in this code have already been
// declared and initialized.

//-------------------------------------------------------------------
// Open the  message for decoding.

if(hMsg = CryptMsgOpenToDecode(
            MY_ENCODING_TYPE,       // Encoding type
            0,                      // Flags
            0,                      // Message type 
                                    // (get from message)
            hCryptProv,             // Cryptographic provider
            NULL,                   // Recipient information
            NULL))                  // Stream information
{
     printf("The message has been opened for decoding. \n");
}
else
{
     MyHandleError("OpenToDecode failed");
}
//-------------------------------------------------------------------
// Update the message with the encoded BLOB. 

if(CryptMsgUpdate(
            hMsg,             // Handle to the message
            pbEncodedBlob,    // Pointer to the encoded BLOB
            cbEncodedBlob,    // Size of the encoded BLOB
            TRUE))            // Last call
{
     printf("The encoded data is added to the message "
         "to decode. \n");
}
else
{
    MyHandleError("Decode MsgUpdate failed");
}
//-------------------------------------------------------------------
// Get the message type.

if(CryptMsgGetParam(
       hMsg,               // Handle to the message
       CMSG_TYPE_PARAM,    // Parameter type
       0,                  // Index
       &dwMsgType,         // Address for returned information
       &cbData))           // Size of the returned information
{
    printf("The message type has been obtained. \n");
}
else
{
    MyHandleError("Decode CMSG_TYPE_PARAM failed");
}
//-------------------------------------------------------------------
// Some applications may need to use a switch statement here
// and process the message differently, depending on the
// message type.

if(dwMsgType == CMSG_HASHED)
{
     printf("The message is a hashed message. Proceed. \n");
}
else
{
    MyHandleError("Wrong message type");
}
//-------------------------------------------------------------------
// Get the size of the content.

if(CryptMsgGetParam(
               hMsg,                   // Handle to the message
               CMSG_CONTENT_PARAM,     // Parameter type
               0,                      // Index
               NULL,                   // Address for returned 
                                       // information
               &cbDecoded))            // Size of the returned 
                                       // information
{
    printf("The length %d of the message obtained. \n", cbDecoded);
}
else
{
    MyHandleError("Decode CMSG_CONTENT_PARAM failed");
}
//-------------------------------------------------------------------
// Allocate memory.

if(pbDecoded = (BYTE *) malloc(cbDecoded))
{
     printf("Memory for the decoded message has been allocated.\n");
}
else
{
    MyHandleError("Decoding memory allocation failed");
}
//-------------------------------------------------------------------
// Copy the decoded message into the buffer just allocated.

if(CryptMsgGetParam(
            hMsg,                    // Handle to the message
            CMSG_CONTENT_PARAM,      // Parameter type
            0,                       // Index
            pbDecoded,               // Address for returned 
                                     // information
            &cbDecoded))             // Size of the returned 
                                     // information
{
    printf("Message decoded successfully \n");
    printf("The decoded message is \n%s\n", (LPSTR)pbDecoded);
}
else
{
    MyHandleError("Decoding CMSG_CONTENT_PARAM #2 failed");
}
//-------------------------------------------------------------------
// Verify the hash.

if(CryptMsgControl(
              hMsg,                        // Handle to the message
              0,                           // Flags
              CMSG_CTRL_VERIFY_HASH,       // Control type
              NULL))                       // Pointer not used
{
    printf("Verification of hash succeeded. \n");
    printf("The data has not been tampered with.\n");
}
else
{
     printf("Verification of hash failed. Something changed "
         "this message .\n");
}

printf("Test program completed without error. \n");

//-------------------------------------------------------------------
// Clean up

if(pbEncodedBlob)
    free(pbEncodedBlob);
if(pbDecoded)
    free(pbDecoded);

CryptMsgClose(hMsg); 

// Release the CSP.

if(hCryptProv) 
   CryptReleaseContext(hCryptProv,0);
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
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



 

 
