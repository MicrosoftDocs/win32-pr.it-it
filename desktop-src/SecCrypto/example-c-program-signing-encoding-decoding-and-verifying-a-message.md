---
description: Nell'esempio seguente vengono combinate la firma e la codifica di un messaggio e la decodifica di un messaggio firmato e la verifica della firma.
ms.assetid: 2cad11a8-75ad-4726-a7bb-82870b71c721
title: 'Esempio di programma C: firma, codifica, decodifica e verifica di un messaggio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128b4368a75d5f7636394fdf9a3b1b2694f45176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752146"
---
# <a name="example-c-program-signing-encoding-decoding-and-verifying-a-message"></a><span data-ttu-id="dd996-103">Esempio di programma C: firma, codifica, decodifica e verifica di un messaggio</span><span class="sxs-lookup"><span data-stu-id="dd996-103">Example C Program: Signing, Encoding, Decoding, and Verifying a Message</span></span>

<span data-ttu-id="dd996-104">Nell'esempio seguente vengono combinate la firma e la codifica di un messaggio e la decodifica di un messaggio firmato e la verifica della firma.</span><span class="sxs-lookup"><span data-stu-id="dd996-104">The following example combines signing and encoding a message, and decoding a signed message and verifying the signature.</span></span> <span data-ttu-id="dd996-105">Le due operazioni si trovavano in genere in programmi distinti.</span><span class="sxs-lookup"><span data-stu-id="dd996-105">The two operations would usually be in separate programs.</span></span> <span data-ttu-id="dd996-106">L'esempio di codifica crea il messaggio codificato, lo salva in un file su disco o in altro modo lo invia a un altro utente.</span><span class="sxs-lookup"><span data-stu-id="dd996-106">The encoding example would create the encoded message, save it to a disk file or in some other way send it to another user.</span></span> <span data-ttu-id="dd996-107">L'esempio di decodifica riceverà il messaggio codificato, lo decodifica e verificherà la firma.</span><span class="sxs-lookup"><span data-stu-id="dd996-107">The decoding example would receive the encoded message, decode it, and verify the signature.</span></span> <span data-ttu-id="dd996-108">I due processi sono stati combinati per illustrare l'utilizzo di entrambe le procedure.</span><span class="sxs-lookup"><span data-stu-id="dd996-108">The two processes have been combined here to show both procedures working.</span></span>

<span data-ttu-id="dd996-109">La firma e la codifica di un messaggio non garantiscono la privacy del messaggio.</span><span class="sxs-lookup"><span data-stu-id="dd996-109">Signing and encoding a message does not ensure privacy for that message.</span></span> <span data-ttu-id="dd996-110">Ma garantisce l'autenticità del messaggio.</span><span class="sxs-lookup"><span data-stu-id="dd996-110">Rather it ensures the authenticity of the message.</span></span> <span data-ttu-id="dd996-111">Poiché il messaggio viene firmato con la chiave privata del mittente, quando il ricevitore del messaggio decrittografa la firma con la [*chiave pubblica*](../secgloss/p-gly.md) del mittente (disponibile dal certificato inviato insieme al messaggio), il destinatario può essere sicuro che il messaggio sia stato inviato dalla persona o dall'entità associata al certificato e che il messaggio non sia stato modificato dopo la firma.</span><span class="sxs-lookup"><span data-stu-id="dd996-111">Because the message is signed with the sender's private key, when the receiver of the message decrypts the signature with the sender's [*public key*](../secgloss/p-gly.md) (available from the certificate that is sent along with the message), the receiver can be sure that the message was sent by the person or entity associated with the certificate and that the message was not changed after it was signed.</span></span>

<span data-ttu-id="dd996-112">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti per la codifica di un messaggio:</span><span class="sxs-lookup"><span data-stu-id="dd996-112">This example illustrates the following tasks and CryptoAPI functions for encoding a message:</span></span>

-   <span data-ttu-id="dd996-113">Apertura di un archivio certificati utilizzando [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="dd996-113">Opening a certificate store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="dd996-114">Recupero di un certificato con un nome soggetto specifico utilizzando [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span><span class="sxs-lookup"><span data-stu-id="dd996-114">Retrieving a certificate with a specific subject name using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="dd996-115">Ottenere e stampare il nome del soggetto del certificato usando [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="dd996-115">Getting and printing a certificate's subject name using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="dd996-116">Inizializzazione di una struttura di messaggio di firma di Crypt da utilizzare in una chiamata a [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). [**\_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)</span><span class="sxs-lookup"><span data-stu-id="dd996-116">Initializing a [**CRYPT\_SIGN\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) structure to be used in a call to [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span>
-   <span data-ttu-id="dd996-117">Firma e codifica di un messaggio con [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="dd996-117">Signing and encoding a message with [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span>

<span data-ttu-id="dd996-118">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti per la decodifica di un messaggio e la verifica della firma:</span><span class="sxs-lookup"><span data-stu-id="dd996-118">This example illustrates the following tasks and CryptoAPI functions for decoding a message and verifying the signature:</span></span>

-   <span data-ttu-id="dd996-119">Apertura di un messaggio per la decodifica con [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span><span class="sxs-lookup"><span data-stu-id="dd996-119">Opening a message for decoding with [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="dd996-120">Aggiunta del [*BLOB*](../secgloss/b-gly.md) codificato al messaggio da decodificare tramite [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="dd996-120">Adding the encoded [*BLOB*](../secgloss/b-gly.md) to the message to be decoded by using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="dd996-121">Decodifica del messaggio con [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="dd996-121">Decoding the message using [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>
-   <span data-ttu-id="dd996-122">Apertura di un archivio certificati in memoria con [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) utilizzando il messaggio ricevuto e decodificato.</span><span class="sxs-lookup"><span data-stu-id="dd996-122">Opening a certificate store in memory with [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) using the message received and decoded.</span></span>
-   <span data-ttu-id="dd996-123">Utilizzo di [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) per ottenere il certificato del firmatario del messaggio.</span><span class="sxs-lookup"><span data-stu-id="dd996-123">Using [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the certificate of the message's signer.</span></span>
-   <span data-ttu-id="dd996-124">Verifica della firma di un messaggio con [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span><span class="sxs-lookup"><span data-stu-id="dd996-124">Verifying a message's signature using [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span></span>
-   <span data-ttu-id="dd996-125">Liberare memoria, chiudere gli [*archivi certificati*](../secgloss/c-gly.md)e liberare il [*contesto del certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dd996-125">Freeing memory, closing [*certificate stores*](../secgloss/c-gly.md), and freeing [*certificate context*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="dd996-126">Per un esempio di come eseguire queste operazioni simili usando un callback di flusso, vedere [esempio C Program: codifica e decodifica di un messaggio con un flusso](example-c-program--encoding-and-decoding-a-message-using-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="dd996-126">For an example of how to perform these similar operations using a stream callback, see [Example C Program: Encoding and Decoding a Message Using a Stream](example-c-program--encoding-and-decoding-a-message-using-a-stream.md).</span></span>

<span data-ttu-id="dd996-127">In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="dd996-127">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="dd996-128">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="dd996-128">Code for this function is included with the sample.</span></span> <span data-ttu-id="dd996-129">Il codice per questa e altre funzioni ausiliarie è elencato anche in [ \_ \_ funzioni di utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="dd996-129">Code for this and other auxiliary functions is also listed under [General\_Purpose\_Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example of encoding and decoding a signed message.

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

#define MAX_NAME 256

#define CERTIFICATE_STORE_NAME L"MY"

//-------------------------------------------------------------------
//    Declare local functions.

//-------------------------------------------------------------------
BOOL EncodeMessage(PCRYPT_DATA_BLOB pEncodedData,
                   LPWSTR pwszSignerName);
void DecodeMessage(PCRYPT_DATA_BLOB pEncodedData,
                   LPWSTR pwszSignerName);

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void ReportFailure()
{
    switch (GetLastError())
    {
        case CRYPT_E_AUTH_ATTR_MISSING:
            printf("Message does not contain an expected "
                "attribute.\n");
            break;
        case CRYPT_E_BAD_ENCODE:
            printf("An error encountered encoding or decoding.\n");
            break;
        case CRYPT_E_HASH_VALUE:
            printf("The hash value is not correct.\n");
            break;
        case CRYPT_E_INVALID_MSG_TYPE:
            printf("The message type is not valid.\n");
            break;
        case CRYPT_E_OSS_ERROR:
            printf("OSS error.\n");
            break;
        case CRYPT_E_SIGNER_NOT_FOUND:
            printf("Signer not found.\n");
            break;
        case CRYPT_E_UNEXPECTED_ENCODING:
            printf("Unexpected encoding. \n");
            break;
        case CRYPT_E_UNKNOWN_ALGO:
            printf("Unknown algorithm.\n");
            break;
        case E_OUTOFMEMORY:
            printf("Out of memory.\n");
            break;
        case ERROR_INVALID_HANDLE:
            printf("The handle from verify signature is not valid." \
                "function.\n");
            break;
        case ERROR_INVALID_PARAMETER:
            printf("The parameter from verify signature "
                "is not valid.\n");
            break;
        case NTE_BAD_FLAGS:
            printf("Bad Flags from verify signature function.\n");
            break;
        case NTE_BAD_HASH:
            printf("Bad Hash from verify signature function.\n");
            break;
        case NTE_BAD_KEY:
            printf("Bad Key from verify signature function.\n");
            break;
        case NTE_BAD_SIGNATURE:
            printf("Bad signature from verify signature " \
                "function.\n");
            break;
        case NTE_BAD_UID:
            printf("Bad UID from verify signature function.\n");
            break;
    }  // End switch.
}  // End ReportFailure.

void EncodeAndDecodeMessage(LPWSTR pwszSignerName)
{
    CRYPT_DATA_BLOB EncodedBlob;

    if(EncodeMessage(&EncodedBlob, pwszSignerName))
    {
        DecodeMessage(&EncodedBlob, pwszSignerName);
    }
}

BOOL EncodeMessage(PCRYPT_DATA_BLOB pEncodedBlob,
                   LPWSTR pwszSignerName)
{
    /*---------------------------------------------------------------
        Declare and initialize variables. This includes getting a 
        pointer to the message content. This sample creates 
        the message content and gets a pointer to it. In most 
        situations, the content will exist somewhere, and a 
        pointer to it will get passed to the application. 
    ---------------------------------------------------------------*/

    HCERTSTORE hSystemStoreHandle;
    CRYPT_SIGN_MESSAGE_PARA SignMessagePara;

    //---------------------------------------------------------------
    //   The message to be signed and encoded.

    BYTE* pbContent = (BYTE*) "The quick brown fox jumped over " \
        "the lazy dog.";

    /*---------------------------------------------------------------
        The length of the message. This must be one more than the 
        value returned by strlen() to include the terminal NULL 
        character.
    ---------------------------------------------------------------*/
    DWORD cbContent = lstrlenA((char *) pbContent) + 1;

    //---------------------------------------------------------------
    //    Arrays to hold the message to be signed and its length.

    const BYTE *rgpbToBeSigned[1] ;
    DWORD rgcbToBeSigned[1];

    //---------------------------------------------------------------
    //    The signer's certificate.

    PCCERT_CONTEXT pSignerCert; 

    //---------------------------------------------------------------
    //    Buffer to hold the name of the subject of a certificate.

    char pszNameString[MAX_NAME];

    //---------------------------------------------------------------
    //  The following variables are used only in the decoding phase.

    DWORD cbData = sizeof(DWORD);

    //---------------------------------------------------------------
    //  Begin processing. Display the original message.

    rgpbToBeSigned[0] = pbContent;
    rgcbToBeSigned[0] = cbContent;

    printf("The original message = \n%s\n\n",
        rgpbToBeSigned[0]);

    //---------------------------------------------------------------
    // Open a certificate store.

    if(hSystemStoreHandle = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        CERTIFICATE_STORE_NAME))
    {
        printf("The certificate store is open. \n");
    }
    else
    {
        MyHandleError( "Error Getting Store Handle");
    }

    /*---------------------------------------------------------------
        Find a certificate in the store. This certificate will be 
        used to sign the message. To sign the message, the 
        certificate must have a private key accessible.
    ---------------------------------------------------------------*/

    if(pSignerCert = CertFindCertificateInStore(
        hSystemStoreHandle,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        pwszSignerName,
        NULL))
    {
        //-----------------------------------------------------------
        //  Get and print the name of the subject of the certificate.

        if(CertGetNameString(
            pSignerCert,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError("Getting the name of the signer " \
                "failed.\n");
        }
    }
    else
    {
        MyHandleError("Signer certificate not found.");
    }

    /*---------------------------------------------------------------
    Initialize the CRYPT_SIGN_MESSAGE_PARA structure. First, use 
    memset to set all members to zero or NULL. Then set the values of
    all members that must be nonzero.
    ---------------------------------------------------------------*/

    memset(&SignMessagePara, 0, sizeof(CRYPT_SIGN_MESSAGE_PARA));
    SignMessagePara.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SignMessagePara.HashAlgorithm.pszObjId = szOID_RSA_MD2;
    SignMessagePara.pSigningCert = pSignerCert;
    SignMessagePara.dwMsgEncodingType = MY_ENCODING_TYPE;
    SignMessagePara.cMsgCert = 1;
    SignMessagePara.rgpMsgCert = &pSignerCert;

    /*---------------------------------------------------------------
        In two steps, sign and encode the message. First, get the 
        number of bytes required for the buffer to hold the signed 
        and encoded message.
    ---------------------------------------------------------------*/

    if( CryptSignMessage(
            &SignMessagePara,
            FALSE,
            1,
            rgpbToBeSigned,
            rgcbToBeSigned,
            NULL,
            &pEncodedBlob->cbData))
    {
        printf("The needed length is %d \n", pEncodedBlob->cbData);
    }
    else
    {
        MyHandleError("Getting the length failed.\n");
    }

    //---------------------------------------------------------------
    //   Allocate memory for the required buffer.
    pEncodedBlob->pbData = (BYTE *)malloc(pEncodedBlob->cbData);
    if(!pEncodedBlob->pbData)
    {
        MyHandleError("Memory allocation failed.");
    }

    //---------------------------------------------------------------
    //   Call CryptSignMessage a second time to
    //   copy the signed and encoded message to the buffer.

    if( CryptSignMessage(
        &SignMessagePara,
        FALSE,
        1,
        rgpbToBeSigned,
        rgcbToBeSigned,
        pEncodedBlob->pbData,
        &pEncodedBlob->cbData))
    {
        printf("Signing worked \n");
    }
    else
    {
        MyHandleError("Signing failed.\n");
    }

    //---------------------------------------------------------------
    //  Clean up after signing and encoding.

    if(pSignerCert)
    {
        CertFreeCertificateContext(pSignerCert);
    }
    
    if(hSystemStoreHandle)
    {
        CertCloseStore(hSystemStoreHandle,
            CERT_CLOSE_STORE_FORCE_FLAG);
    }

    return TRUE;
}

void DecodeMessage(PCRYPT_DATA_BLOB pEncodedBlob,
                   LPWSTR pwszSignerName)
{
    //---------------------------------------------------------------
    //    Buffer to hold the name of the subject of a certificate.

    char pszNameString[MAX_NAME];

    //---------------------------------------------------------------
    //  The following variables are used only in the decoding phase.

    HCRYPTMSG hMsg;
    HCERTSTORE hStoreHandle;           // certificate store handle
    DWORD cbData = sizeof(DWORD);
    DWORD cbDecoded;
    BYTE *pbDecoded;
    DWORD cbSignerCertInfo;
    PCERT_INFO pSignerCertInfo;
    PCCERT_CONTEXT pSignerCertContext;

    /*---------------------------------------------------------------
        The following code decodes the message and verifies the 
        message signature.  This code would normally be in a 
        stand-alone program that would read the signed and encoded 
        message and its length from a file from an email message, 
        or from some other source.
    ---------------------------------------------------------------*/

    //---------------------------------------------------------------
    //  Open a message for decoding.

    if(hMsg = CryptMsgOpenToDecode(
        MY_ENCODING_TYPE,      // encoding type
        0,                     // flags
        0,                     // use the default message type
                               // the message type is 
                               // listed in the message header
        NULL,                  // cryptographic provider 
                               // use NULL for the default provider
        NULL,                  // recipient information
        NULL))                 // stream information
    {
        printf("The message to decode is open. \n");
    }
    else
    {
        MyHandleError("OpenToDecode failed");
    }
    //---------------------------------------------------------------
    //  Update the message with an encoded BLOB.

    if(CryptMsgUpdate(
        hMsg,                 // handle to the message
        pEncodedBlob->pbData, // pointer to the encoded BLOB
        pEncodedBlob->cbData, // size of the encoded BLOB
        TRUE))                // last call
    {
        printf("The encoded BLOB has been added to the message. \n");
    }
    else
    {
        MyHandleError("Decode MsgUpdate failed");
    }

    //---------------------------------------------------------------
    //  Get the number of bytes needed for a buffer
    //  to hold the decoded message.

    if(CryptMsgGetParam(
        hMsg,                  // handle to the message
        CMSG_CONTENT_PARAM,    // parameter type
        0,                     // index
        NULL,                  
        &cbDecoded))           // size of the returned information
    {
        printf("The message parameter has been acquired. \n");
    }
    else
    {
        MyHandleError("Decode CMSG_CONTENT_PARAM failed.");
    }
    //---------------------------------------------------------------
    // Allocate memory.

    if(!(pbDecoded = (BYTE *) malloc(cbDecoded)))
    {
        MyHandleError("Decode memory allocation failed.");
    }

    //---------------------------------------------------------------
    // Copy the content to the buffer.

    if(CryptMsgGetParam(
        hMsg,                 // handle to the message
        CMSG_CONTENT_PARAM,   // parameter type
        0,                    // index
        pbDecoded,            // address for returned information
        &cbDecoded))          // size of the returned information
    {
        printf("The decoded message is =>\n%s\n\n",
            (LPSTR)pbDecoded);
    }
    else
    {
        MyHandleError("Decode CMSG_CONTENT_PARAM #2 failed");
    }

    //---------------------------------------------------------------
    // Verify the signature.
    // First, get the signer CERT_INFO from the message.

    //---------------------------------------------------------------
    // Get the size of memory required for the certificate.

    if(CryptMsgGetParam(
        hMsg,                         // handle to the message
        CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
        0,                            // index
        NULL,   
        &cbSignerCertInfo))           // size of the returned 
                                      // information
    {
        printf("%d bytes needed for the buffer.\n", 
            cbSignerCertInfo);
    }
    else
    {
        MyHandleError("Verify SIGNER_CERT_INFO #1 failed.");
    }

    //---------------------------------------------------------------
    // Allocate memory.

    if(!(pSignerCertInfo = (PCERT_INFO) malloc(cbSignerCertInfo)))
    {
        MyHandleError("Verify memory allocation failed.");
    }

    //---------------------------------------------------------------
    // Get the message certificate information (CERT_INFO
    // structure).

    if(!(CryptMsgGetParam(
        hMsg,                         // handle to the message
        CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
        0,                            // index
        pSignerCertInfo,              // address for returned 
                                      // information
        &cbSignerCertInfo)))          // size of the returned 
                                      // information
    {
        MyHandleError("Verify SIGNER_CERT_INFO #2 failed");
    }

    //---------------------------------------------------------------
    // Open a certificate store in memory using CERT_STORE_PROV_MSG,
    // which initializes it with the certificates from the message.

    if(hStoreHandle = CertOpenStore(
        CERT_STORE_PROV_MSG,         // store provider type 
        MY_ENCODING_TYPE,            // encoding type
        NULL,                        // cryptographic provider
                                     // use NULL for the default
        0,                           // flags
        hMsg))                       // handle to the message
    {
        printf("The certificate store to be used for message " \
            "verification has been opened.\n");
    }
    else  
    {
        MyHandleError("Verify open store failed");
    }

    //---------------------------------------------------------------
    // Find the signer's certificate in the store.

    if(pSignerCertContext = CertGetSubjectCertificateFromStore(
        hStoreHandle,       // handle to the store
        MY_ENCODING_TYPE,   // encoding type
        pSignerCertInfo))   // pointer to retrieved CERT_CONTEXT
    {
        if(CertGetNameString(
            pSignerCertContext,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError("Getting the signer's name failed.\n");
        }
    }
    else
    {
        MyHandleError("Verify GetSubjectCert failed");
    }

    //---------------------------------------------------------------
    // Use the CERT_INFO from the signer certificate to verify
    // the signature.

    if(CryptMsgControl(
        hMsg,
        0,
        CMSG_CTRL_VERIFY_SIGNATURE,
        pSignerCertContext->pCertInfo))
    {
        printf("Verify signature succeeded. \n");
    }
    else
    {
        printf("The signature was not verified. \n");
        ReportFailure();
    }
    //---------------------------------------------------------------
    // Clean up.
    if(pEncodedBlob->pbData)
    {
        free(pEncodedBlob->pbData);
        pEncodedBlob->pbData = NULL;
    }
    if(pbDecoded)
    {
        free(pbDecoded);
    }
    if(pSignerCertInfo)
    {
        free(pSignerCertInfo);
    }
    if(pSignerCertContext)
    {
        CertFreeCertificateContext(pSignerCertContext); 
    }
    if(hStoreHandle)
    {
        CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
    }
    if(hMsg)
    {
        CryptMsgClose(hMsg);
    }
}
```



 

 
