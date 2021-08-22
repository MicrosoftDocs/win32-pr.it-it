---
description: Crea ed esegue l'hashing di una chiave di sessione che può essere usata per crittografare un messaggio, un testo o un file.
ms.assetid: 15d4a05d-5888-4532-91fd-6cd94afe0b99
title: 'Esempio di programma C: Creazione e hash di una chiave di sessione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3264e8b7d78506f2aed663d14a4bd8278059152ce085f460ddbbc8e75325d91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007854"
---
# <a name="example-c-program-creating-and-hashing-a-session-key"></a>Esempio di programma C: Creazione e hash di una chiave di sessione

L'esempio seguente crea [*ed esegue l'hashing*](../secgloss/h-gly.md) di una chiave di [*sessione*](../secgloss/s-gly.md) che può essere usata per crittografare un messaggio, un testo o un file.

Questo esempio illustra anche l'uso delle funzioni CryptoAPI seguenti:

-   [**CryptAcquireContext per acquisire**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) un [*provider del servizio di crittografia*](../secgloss/c-gly.md).
-   [**CryptCreateHash per**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) creare un oggetto hash vuoto.
-   [**CryptGenKey per**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) creare una chiave [*di sessione casuale.*](../secgloss/s-gly.md)
-   [**CryptHashSessionKey per**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) eseguire l'hashing della chiave di sessione creata.
-   [**CryptDestroyHash per**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) eliminare l'hash.
-   [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) per eliminare la chiave creata.
-   [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) per rilasciare il provider di servizi di configurazione.

In questo esempio viene utilizzata la [**funzione MyHandleError**](myhandleerror.md). Il codice per questa funzione è incluso nell'esempio. Il codice per questa e altre funzioni ausiliarie è elencato anche in [per utilizzo generico funzioni](general-purpose-functions.md).


```C++
//  Copyright (C) Microsoft. All rights reserved.
//  
//  CreateAndHashSessionKey.cpp : Defines the entry point for the 
//  application.
//

#include <stdafx.h>

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(LPTSTR psz);

void main()
{
    HCRYPTPROV hCryptProv;
    HCRYPTHASH hHash;
    HCRYPTKEY hKey;

    //---------------------------------------------------------------
    // Acquire a cryptographic provider context handle.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        printf("CryptAcquireContext complete. \n");
    }
    else
    {
        MyHandleError("Acquisition of context failed.");
    }

    //---------------------------------------------------------------
    // Create a hash object.
    if(CryptCreateHash(
        hCryptProv, 
        CALG_MD5, 
        0, 
        0, 
        &hHash)) 
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptBeginHash!\n");
    }

    //---------------------------------------------------------------
    // Create a random session key.
    if(CryptGenKey(
        hCryptProv, 
        CALG_RC2, 
        CRYPT_EXPORTABLE, 
        &hKey)) 
    {
        printf("A random session key has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptGenKey!\n");
    }

    //---------------------------------------------------------------
    // Compute the cryptographic hash on the key object.
    if(CryptHashSessionKey(
        hHash, 
        hKey, 
        0))
    {
        printf("The session key has been hashed. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashSessionKey!\n");
    }

    /*
    Use the hash of the key object. For instance, additional data 
    could be hashed and sent in a message to several recipients. The 
    recipients will be able to verify who the message originator is 
    if the key used is also exported to them.
    */

    //---------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
        if(!(CryptDestroyHash(hHash)))
        {
            MyHandleError("Error during CryptDestroyHash");
        }
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError("Error during CryptDestroyKey");
        }
    }

    // Release the provider.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv,0)))
        {
            MyHandleError("Error during CryptReleaseContext");
        }
    }
} // End main.

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

```



 

 
