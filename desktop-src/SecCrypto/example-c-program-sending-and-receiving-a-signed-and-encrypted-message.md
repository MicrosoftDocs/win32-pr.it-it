---
description: L'esempio seguente firma un messaggio usando la chiave privata di un mittente e crittografa il messaggio firmato usando la chiave pubblica di un ricevitore.
ms.assetid: f2863e4a-d22a-4ff0-91d8-052eeaade14e
title: 'Programma C di esempio: invio e ricezione di un messaggio firmato e crittografato'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7bdfdfd664d278fe72d81743e7116eb64a11099ef37b43200d55378472c383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007539"
---
# <a name="example-c-program-sending-and-receiving-a-signed-and-encrypted-message"></a>Programma C di esempio: invio e ricezione di un messaggio firmato e crittografato

L'esempio seguente firma un messaggio [](../secgloss/p-gly.md) usando la chiave privata di un mittente e crittografa il messaggio firmato usando la [*chiave pubblica di un ricevitore.*](../secgloss/p-gly.md) L'esempio decrittografa quindi il messaggio usando la chiave privata del ricevitore e verifica la firma usando la chiave pubblica del mittente. Il certificato del mittente contenente la chiave pubblica necessaria è incluso nel messaggio crittografato. Questo esempio scrive anche il messaggio firmato e crittografato in un file. Per altre informazioni, vedere [Esempio di programma C: Ricezione di un messaggio firmato e crittografato](example-c-program-receiving-a-signed-and-encrypted-message.md).

Per firmare il messaggio, la chiave privata del firmatario e il certificato del firmatario devono essere disponibili. Per crittografare il messaggio firmato, è necessario che sia disponibile un certificato del ricevitore che include la chiave pubblica del ricevitore.

Per decrittografare il messaggio, la chiave privata del ricevitore deve essere disponibile. Dopo la decrittografia del messaggio, la firma viene verificata usando la chiave pubblica del certificato incluso nel messaggio crittografato.

> [!Note]  
> Non tutti i certificati in un archivio [*certificati*](../secgloss/c-gly.md) forniscono l'accesso alla [*chiave privata*](../secgloss/p-gly.md) associata al certificato. Quando il messaggio viene firmato e crittografato, deve essere usato un certificato appartenente al firmatario con accesso alla chiave privata del firmatario. Inoltre, il destinatario del messaggio deve avere accesso alla chiave privata associata alla chiave pubblica usata per crittografare il messaggio.

 

In questo esempio vengono illustrate le attività seguenti:

-   Apertura e chiusura degli archivi certificati di sistema.
-   Ricerca di certificati per un mittente e un destinatario di messaggi negli archivi certificati aperti.
-   Ricerca e stampa del nome soggetto dai certificati.
-   Inizializzazione delle strutture di dati necessarie per firmare, crittografare, decrittografare e verificare un messaggio.
-   Chiamata di una funzione CryptoAPI per trovare le dimensioni richieste di un buffer, allocando il buffer delle dimensioni richieste e chiamando di nuovo la funzione CryptoAPI per riempire il buffer. Per altre informazioni, vedere [Recupero di dati di lunghezza sconosciuta.](retrieving-data-of-unknown-length.md)
-   Visualizzazione di parte del contenuto crittografato di un buffer. La funzione locale inclusa, **ShowBytes**, visualizza i caratteri nel buffer con valori compresi tra '0' e 'z'. Tutti gli altri caratteri vengono visualizzati come carattere '-'.

In questo esempio vengono utilizzate le funzioni CryptoAPI seguenti:

-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
-   [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)
-   [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey)
-   [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)
-   [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature)
-   [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)
-   [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

In questo esempio vengono utilizzate funzioni separate per mostrare il processo di firma/crittografia e il processo di decrittografia/verifica della firma. Usa anche [**MyHandleError**](myhandleerror.md) per uscire normalmente dal programma in caso di errore. Il codice **MyHandleError** è incluso nell'esempio e può essere trovato insieme ad altre funzioni ausiliarie in [per utilizzo generico Funzioni](general-purpose-functions.md).


```C++
//-------------------------------------------------------------------
// Example C Program: 
// Signs a message by using a sender's private key and encrypts the
// signed message by using a receiver's public key.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MAX_NAME  128

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// SIGNER_NAME is used with the CertFindCertificateInStore  
// function to retrieve the certificate of the message signer.
// Replace the Unicode string below with the certificate subject 
// name of the message signer.

#define SIGNER_NAME L"DUMMY_SIGNER_NAME"

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//-------------------------------------------------------------------
// The local function ShowBytes is declared here and defined after 
// main.

void ShowBytes(BYTE *s, DWORD len);

//-------------------------------------------------------------------
// Declare local functions SignAndEncrypt, DecryptAndVerify, and 
// WriteSignedAndEncryptedBlob.
// These functions are defined after main.

BYTE* SignAndEncrypt(
     const BYTE     *pbToBeSignedAndEncrypted,
     DWORD          cbToBeSignedAndEncrypted,
     DWORD          *pcbSignedAndEncryptedBlob);

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob);

void WriteSignedAndEncryptedBlob(
     DWORD  cbBlob,
     BYTE   *pbBlob);

void main (void)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    //---------------------------------------------------------------
    //  pbToBeSignedAndEncrypted is the message to be 
    //  encrypted and signed.

    const BYTE *pbToBeSignedAndEncrypted =
            (const unsigned char *)"Insert the message to be signed "
            "here";
    //---------------------------------------------------------------
    // This is the length of the message to be
    // encrypted and signed. Note that it is one
    // more that the length returned by strlen()
    // to include the terminating null character.

    DWORD cbToBeSignedAndEncrypted = 
        lstrlenA((const char *)pbToBeSignedAndEncrypted) + 1;

    //---------------------------------------------------------------
    // Pointer to a buffer that will hold the
    // encrypted and signed message.

    BYTE *pbSignedAndEncryptedBlob;

    //---------------------------------------------------------------
    // A DWORD to hold the length of the signed 
    // and encrypted message.

    DWORD cbSignedAndEncryptedBlob;
    BYTE *pReturnMessage;

    //---------------------------------------------------------------
    // Call the local function SignAndEncrypt.
    // This function returns a pointer to the 
    // signed and encrypted BLOB and also returns
    // the length of that BLOB.

    pbSignedAndEncryptedBlob = SignAndEncrypt(
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        &cbSignedAndEncryptedBlob);

    _tprintf(TEXT("The following is the signed and encrypted ")
        TEXT("message.\n"));
    ShowBytes(pbSignedAndEncryptedBlob,cbSignedAndEncryptedBlob/4);

    // Open a file and write the signed and 
    // encrypted message to the file.

    WriteSignedAndEncryptedBlob(
        cbSignedAndEncryptedBlob,
        pbSignedAndEncryptedBlob);

    //---------------------------------------------------------------
    // Call the local function DecryptAndVerify.
    // This function decrypts and displays the 
    // encrypted message and also verifies the 
    // message's signature.
       
    if(pReturnMessage = DecryptAndVerify(
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT(" The returned, verified message is ->\n%s\n"),
            pReturnMessage);
        _tprintf(TEXT(" The program executed without error.\n"));
    }
    else
    {
        _tprintf(TEXT("Verification failed.\n"));
    }

} // End Main.

//-------------------------------------------------------------------
// Begin definition of the SignAndEncrypt function.

BYTE* SignAndEncrypt(
     const BYTE *pbToBeSignedAndEncrypted,
     DWORD cbToBeSignedAndEncrypted,
     DWORD *pcbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    FILE *hToSave;
    HCERTSTORE hCertStore;

    //---------------------------------------------------------------
    // pSignerCertContext will be the certificate of 
    // the message signer.

    PCCERT_CONTEXT pSignerCertContext ;

    //---------------------------------------------------------------
    // pReceiverCertContext will be the certificate of the 
    // message receiver.

    PCCERT_CONTEXT pReceiverCertContext;

    TCHAR pszNameString[256];
    CRYPT_SIGN_MESSAGE_PARA SignPara;
    CRYPT_ENCRYPT_MESSAGE_PARA EncryptPara;
    DWORD cRecipientCert;
    PCCERT_CONTEXT rgpRecipientCert[5];
    BYTE *pbSignedAndEncryptedBlob = NULL;
    CERT_NAME_BLOB Subject_Blob;
    BYTE *pbDataIn;
    DWORD dwKeySpec;
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Open the MY certificate store. 
    // For more information, see the CertOpenStore function 
    // PSDK reference page. 
    // Note: Case is not significant in certificate store names.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Get the certificate for the signer.

    if(!(pSignerCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        SIGNER_NAME,
        NULL)))
    {
        MyHandleError(TEXT("Cert not found.\n"));
    }

    //---------------------------------------------------------------
    // Get and print the name of the message signer.
    // The following two calls to CertGetNameString with different
    // values for the second parameter get two different forms of 
    // the certificate subject's name.

    if(CertGetNameString(
        pSignerCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The SIMPLE_DISPLAY_TYPE message signer's name is ")
            TEXT("%s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(CertGetNameString(
        pSignerCertContext,
        CERT_NAME_RDN_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The RDM_TYPE message signer's name is %s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(!( CryptAcquireCertificatePrivateKey(
        pSignerCertContext,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        MyHandleError(TEXT("CryptAcquireCertificatePrivateKey.\n"));
    }

    //---------------------------------------------------------------
    // Get the certificate for the receiver. In this case,  
    // a BLOB with the name of the receiver is saved in a file.

    // Note: To decrypt the message signed and encrypted here,
    // this program must use the certificate of the intended
    // receiver. The signed and encrypted message can only be
    // decrypted and verified by the owner of the recipient
    // certificate. That user must have access to the private key
    // associated with the public key of the recipient's certificate.

    // To run this sample, the file contains information that allows 
    // the program to find one of the current user's certificates. 
    // The current user should have access to the private key of the
    // certificate and thus can test the verification and decryption. 

    // In normal use, the file would contain information used to find
    // the certificate of an intended receiver of the message. 
    // The signed and encrypted message would be written
    // to a file or otherwise sent to the intended receiver.

    //---------------------------------------------------------------
    // Open a file and read in the receiver name
    // BLOB.


    if( !(hToSave= fopen("s.txt","rb")))
    {
        MyHandleError(TEXT("Source file was not opened.\n"));
    }

    fread(
        &(Subject_Blob.cbData),
        sizeof(DWORD),
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("The size of the BLOB was not read.\n"));
    }

    if(!(pbDataIn = (BYTE *) malloc(Subject_Blob.cbData)))
    {
        MyHandleError(TEXT("Memory allocation error."));
    }

    fread(
        pbDataIn,
        Subject_Blob.cbData,
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("BLOB not read."));
    }

    fclose(hToSave);

    Subject_Blob.pbData = pbDataIn;

    //---------------------------------------------------------------
    // Use the BLOB just read in from the file to find its associated
    // certificate in the MY store.
    // This call to CertFindCertificateInStore uses the
    // CERT_FIND_SUBJECT_NAME dwFindType.

    if(!(pReceiverCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_NAME,
        &Subject_Blob,
        NULL)))
    {
        MyHandleError(TEXT("Receiver certificate not found."));
    }

    //---------------------------------------------------------------
    // Get and print the subject name from the receiver's
    // certificate.

    if(CertGetNameString(
        pReceiverCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(TEXT("The message receiver is  %s \n"), 
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the receiver failed.\n"));
    }

    //---------------------------------------------------------------
    // Initialize variables and data structures
    // for the call to CryptSignAndEncryptMessage.

    SignPara.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SignPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    SignPara.pSigningCert = pSignerCertContext ;
    SignPara.HashAlgorithm.pszObjId = szOID_RSA_MD2;
    SignPara.HashAlgorithm.Parameters.cbData = 0;
    SignPara.pvHashAuxInfo = NULL;
    SignPara.cMsgCert = 1;
    SignPara.rgpMsgCert = &pSignerCertContext ;
    SignPara.cMsgCrl = 0;
    SignPara.rgpMsgCrl = NULL;
    SignPara.cAuthAttr = 0;
    SignPara.rgAuthAttr = NULL;
    SignPara.cUnauthAttr = 0;
    SignPara.rgUnauthAttr = NULL;
    SignPara.dwFlags = 0;
    SignPara.dwInnerContentType = 0;

    EncryptPara.cbSize = sizeof(CRYPT_ENCRYPT_MESSAGE_PARA);
    EncryptPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    EncryptPara.hCryptProv = 0;
    EncryptPara.ContentEncryptionAlgorithm.pszObjId = szOID_RSA_RC4;
    EncryptPara.ContentEncryptionAlgorithm.Parameters.cbData = 0;
    EncryptPara.pvEncryptionAuxInfo = NULL;
    EncryptPara.dwFlags = 0;
    EncryptPara.dwInnerContentType = 0;

    cRecipientCert = 1;
    rgpRecipientCert[0] = pReceiverCertContext;
    *pcbSignedAndEncryptedBlob = 0;
    pbSignedAndEncryptedBlob = NULL;

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        NULL, // the pbSignedAndEncryptedBlob
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("%d bytes for the buffer .\n"),
            *pcbSignedAndEncryptedBlob);
    }
    else
    {
        MyHandleError(TEXT("Getting the buffer length failed."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer.

    if(!(pbSignedAndEncryptedBlob = 
        (unsigned char *)malloc(*pcbSignedAndEncryptedBlob)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    //---------------------------------------------------------------
    // Call the function a second time to copy the signed and 
    // encrypted message into the buffer.

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        pbSignedAndEncryptedBlob,
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("The message is signed and encrypted.\n"));
    }
    else
    {
        MyHandleError(
            TEXT("The message failed to sign and encrypt."));
    }

    //---------------------------------------------------------------
    // Clean up.

    if(pSignerCertContext )
    {
        CertFreeCertificateContext(pSignerCertContext);
    }
    
    if(pReceiverCertContext )
    {
        CertFreeCertificateContext(pReceiverCertContext);
    }
    
    CertCloseStore(hCertStore, 0);

    //---------------------------------------------------------------
    // Return the signed and encrypted message.

    return pbSignedAndEncryptedBlob;

}  // End SignAndEncrypt.

//-------------------------------------------------------------------
// Define the DecryptAndVerify function.

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    HCERTSTORE hCertStore;
    CRYPT_DECRYPT_MESSAGE_PARA DecryptPara;
    CRYPT_VERIFY_MESSAGE_PARA VerifyPara;
    DWORD dwSignerIndex = 0;
    BYTE *pbDecrypted;
    DWORD cbDecrypted;

    //---------------------------------------------------------------
    // Open the certificate store.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Initialize the needed data structures.

    DecryptPara.cbSize = sizeof(CRYPT_DECRYPT_MESSAGE_PARA);
    DecryptPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    DecryptPara.cCertStore = 1;
    DecryptPara.rghCertStore = &hCertStore;

    VerifyPara.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyPara.hCryptProv = 0;
    VerifyPara.pfnGetSignerCertificate = NULL;
    VerifyPara.pvGetArg = NULL;
    pbDecrypted = NULL;
    cbDecrypted = 0;

    //---------------------------------------------------------------
    // Call CryptDecryptAndVerifyMessageSignature a first time
    // to determine the needed size of the buffer to hold the 
    // decrypted message.

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        NULL,           // pbDecrypted
        &cbDecrypted,
        NULL,
        NULL)))
    {
        MyHandleError(TEXT("Failed getting size."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer to hold the decrypted
    // message.

    if(!(pbDecrypted = (BYTE *)malloc(cbDecrypted)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        pbDecrypted,
        &cbDecrypted,
        NULL,
        NULL)))
    {
        pbDecrypted = NULL;
    }

    //---------------------------------------------------------------
    // Close the certificate store.

    CertCloseStore(
        hCertStore,
        0);

    //---------------------------------------------------------------
    // Return the decrypted string or NULL.

    return pbDecrypted;

} // End of DecryptandVerify.

//-------------------------------------------------------------------
// Define the MyHandleError function.

void WriteSignedAndEncryptedBlob(
     DWORD cbBlob,
     BYTE *pbBlob)
{
    // Open an output file, write the file, and close the file.
    // This function would be used to save the signed and encrypted 
    // message to a file that would be sent to the intended receiver.
    // Note: The only receiver able to decrypt and verify this
    // message will have access to the private key associated 
    // with the public key from the certificate used when 
    // the message was encrypted.

    FILE *hOutputFile;

    if( !(hOutputFile = _tfopen(TEXT("sandvout.txt"), TEXT("wb"))))
    {
        MyHandleError(TEXT("Output file was not opened.\n"));
    }

    fwrite(
        &cbBlob,
        sizeof(DWORD),
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The size of the BLOB was not written.\n"));
    }

    fwrite(
        pbBlob,
        cbBlob,
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The bytes of the BLOB were not written.\n"));
    }
    else
    {
        _tprintf(TEXT("The BLOB has been written to the file.\n"));
    }
    
    fclose(hOutputFile);
}  // End of WriteSignedAndEcryptedBlob.


//-------------------------------------------------------------------
// Define the ShowBytes function.
// This function displays the contents of a BYTE buffer. Characters
// less than '0' or greater than 'z' are all displayed as '-'.

void ShowBytes(BYTE *s, DWORD len)
{
    DWORD TotalChars = 0;
    DWORD ThisLine = 0;

    while(TotalChars < len)
    {
        if(ThisLine > 70)
        {
            ThisLine = 0;
            _tprintf(TEXT("\n"));
        }
        if( s[TotalChars] < '0' || s[TotalChars] > 'z')
        {
            _tprintf(TEXT("-"));
        }
        else
        {
            _tprintf(TEXT("%c"), s[TotalChars]);
        }

        TotalChars++;
        ThisLine++;
    }

    _tprintf(TEXT("\n"));
} // End of ShowBytes.

```



 

 
