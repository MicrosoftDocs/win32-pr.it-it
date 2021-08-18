---
description: Enumera i certificati in un archivio certificati, visualizza l'oggetto e l'utente di ogni certificato e converte il nome del soggetto da ogni certificato nel formato con codifica ASN.1 (Abstract Syntax Notation One) e quindi di nuovo nel formato decodificato.
ms.assetid: 8b4771da-0996-40fb-98ce-73efe8e3534f
title: 'Programma C di esempio: conversione di nomi da certificati ad ASN.1 e indietro'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e1093f47500592c32142f4680c046b60facc690f7c794c7b850b18e810242e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993061"
---
# <a name="example-c-program-converting-names-from-certificates-to-asn1-and-back"></a>Programma C di esempio: conversione di nomi da certificati ad ASN.1 e indietro

Nell'esempio seguente vengono enumerati i certificati in un archivio [*certificati,*](../secgloss/c-gly.md)vengono visualizzati l'oggetto e l'utente di ogni certificato e il nome del soggetto di ogni certificato viene convertito nel formato codificato ASN.1 [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) e quindi nel formato decodificato.

Questo esempio illustra le attività e le [*funzioni CryptoAPI*](../secgloss/c-gly.md) seguenti:

-   Apertura di un archivio di sistema [**tramite CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Uso [**di CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore) per ottenere il primo certificato dall'archivio aperto.
-   Uso [**di CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per ottenere il nome soggetto e il nome utente dal certificato.
-   Uso [**di CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) per convertire il nome del soggetto dal certificato nel formato con codifica ASN.1.
-   Uso [**di CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea) per convertire una stringa con codifica ASN.1 nel formato decodificato.
-   Chiusura di un archivio certificati [**tramite CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) con il flag **CERT \_ CLOSE STORE \_ CHECK \_ \_ FLAG.**


```C++
#pragma comment(lib, "crypt32.lib")



//-------------------------------------------------------------------
// Example C Program: 
// Converting a name from a certificate to an ASN.1 encoded string
// and back.

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MY_STRING_TYPE (CERT_OID_NAME_STR)

//-------------------------------------------------------------------
// Declare auxiliary functions

void MyHandleError(LPTSTR);
void Local_wait();

void main(void)
{
    HCERTSTORE hCertStore;
    PCCERT_CONTEXT pCertContext;

    //---------------------------------------------------------------
    // Begin Processing by opening a certificate store.

    if(!(hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        MY_ENCODING_TYPE,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"MY")))
    {
        MyHandleError(TEXT("The MY system store did not open."));
    }

    //---------------------------------------------------------------
    //       Loop through the certificates in the store. 
    //       For each certificate,
    //             get and print the name of the 
    //                  certificate subject and issuer.
    //             convert the subject name from the certificate
    //                  to an ASN.1 encoded string and print the
    //                  octets from that string.
    //             convert the encoded string back into its form 
    //                  in the certificate.

    pCertContext = NULL;
    while(pCertContext = CertEnumCertificatesInStore(
        hCertStore,
        pCertContext))
    {
        LPTSTR pszString;
        LPTSTR pszName;
        DWORD cbSize;
        CERT_BLOB blobEncodedName;

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of subject of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            0,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(
            pCertContext,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszName,
            cbSize))

        {
            _tprintf(TEXT("\nSubject -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of Issuer of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            pszName,   
            cbSize))
        {
            _tprintf(TEXT("Issuer  -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //       Convert the subject name to an ASN.1 encoded
        //       string and print the octets in that string.

        //       First : Get the number of bytes that must 
        //       be allocated for the string.

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            NULL,
            0);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes needed for a string to hold the
        //  converted name, including the null terminator. 
        //  If it returns one, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //        Allocated the needed buffer. Note that this
        //        memory must be freed inside the loop or the 
        //        application will leak memory.

        if(!(pszString = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        //-----------------------------------------------------------
        //       Call the function again to get the string. 

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            pszString,
            cbSize);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes in the string, including the null terminator.
        //  If it returns 1, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //    Get the length needed to convert the string back 
        //    back into the name as it was in the certificate.

        if(!(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            NULL,        // NULL to get the number of bytes 
                            // needed for the buffer.          
            &cbSize,     // Pointer to a DWORD to hold the 
                            // number of bytes needed for the 
                            // buffer
            NULL )))     // Optional address of a pointer to
                            // old the location for an error in the 
                            // input string.
        {
            MyHandleError(
                TEXT("Could not get the length of the BLOB."));
        }

        if (!(blobEncodedName.pbData = (LPBYTE)malloc(cbSize)))
        {
            MyHandleError(
                TEXT("Memory Allocation for the BLOB failed."));
        }
        blobEncodedName.cbData = cbSize;

        if(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            blobEncodedName.pbData,
            &blobEncodedName.cbData,
            NULL))
        {
            _tprintf(TEXT("CertStrToName created the BLOB.\n"));
        }
        else
        {
            MyHandleError(TEXT("Could not create the BLOB."));
        }

        //-----------------------------------------------------------
        //       Free the memory.

        free(blobEncodedName.pbData);
        free(pszString);

        //-----------------------------------------------------------
        //       Pause before information on the next certificate
        //       is displayed.

        Local_wait();

    } // End of while loop
     
    _tprintf(
        TEXT("\nThere are no more certificates in the store. \n"));

    //---------------------------------------------------------------
    //   Close the MY store.

    if(CertCloseStore(
        hCertStore,
        CERT_CLOSE_STORE_CHECK_FLAG))
    {
        _tprintf(TEXT("The store is closed. ")
            TEXT("All certificates are released.\n"));
    }
    else
    {
        _tprintf(TEXT("The store was closed, ")
            TEXT("but certificates still in use.\n"));
    }

    _tprintf(TEXT("This demonstration program ran to completion ")
        TEXT("without error.\n"));

    Local_wait();

} // End of main

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr,
        TEXT("An error occurred in running the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

void Local_wait()
{
//-------------------------------------------------------------------
//  This function prints a prompt string 
//  and wait for the user to hit enter.
//  It provides a pause with its length controlled by the user.

     _tprintf(TEXT("Hit Enter to continue : "));
     getchar();
}
```



 

 
