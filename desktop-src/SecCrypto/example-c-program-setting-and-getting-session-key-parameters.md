---
description: L'esempio seguente crea una chiave di sessione casuale, ottiene e stampa alcuni parametri predefiniti della chiave, imposta i nuovi parametri sulla chiave originale, quindi ottiene e stampa il valore del nuovo parametro.
ms.assetid: 00f93036-05c9-4585-842a-a42a7faea2a5
title: 'Esempio di programma C: impostazione e recupero dei parametri della chiave della sessione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be59b8b47c5becd8576a409d659f99d97b7ee3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883298"
---
# <a name="example-c-program-setting-and-getting-session-key-parameters"></a>Esempio di programma C: impostazione e recupero dei parametri della chiave della sessione

L'esempio seguente crea una chiave di sessione casuale, ottiene e stampa alcuni parametri predefiniti della chiave, imposta i nuovi parametri sulla chiave originale, quindi ottiene e stampa il valore del nuovo parametro. Si pulisce eliminando la chiave della sessione e rilasciando il contesto crittografico.

In questo esempio viene illustrato l'utilizzo delle attività e delle funzioni seguenti:

-   Accesso a un CSP utilizzando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Archiviazione di un buffer con byte casuali tramite [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).
-   Creazione di una chiave di sessione mediante [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).
-   Recupero del valore dei parametri chiave utilizzando [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam).
-   Uso di [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) per modificare il processo di generazione delle chiavi.
-   Eliminazione delle chiavi tramite [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).
-   Rilascio del CSP con [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).

In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md). Il codice per questa funzione è incluso nell'esempio. Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.

#include <windows.h>
#include <wincrypt.h>
#include <stdio.h>
#include <tchar.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

void MyHandleError(PCTSTR psz);

void main()
{
    HCRYPTPROV hProv;
    HCRYPTKEY hKey;
    DWORD dwMode;
    BYTE pbData[16];
    BYTE pbRandomData[8];
    DWORD dwCount;
    DWORD i;

    // Acquire a cryptographic provider context handle.
    if(!CryptAcquireContext(
        &hProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        MyHandleError(TEXT("Error during CryptAcquireContext."));
    }

    //  Generate eight bytes of random data into pbRandomData.
    if( CryptGenRandom(
            hProv,
            8,
            pbRandomData))
    {
        _tprintf(TEXT("Eight bytes of random data have been generated.\n"));
    }
    else
    {
        MyHandleError(TEXT("Random bytes were not correctly generated."));
    }

    // Create a random block cipher session key.
    if(!CryptGenKey(
            hProv, 
            CALG_RC4, 
            CRYPT_EXPORTABLE, 
            &hKey)) 
    {
        MyHandleError(TEXT("Error during CryptGenKey."));
    }

    // Read the cipher mode.
    dwCount = sizeof(DWORD);
    if(CryptGetKeyParam(
        hKey, 
        KP_MODE, 
        (PBYTE)&dwMode, 
        &dwCount, 
        0))
    {
        // Print the cipher mode.
        _tprintf(TEXT("Default cipher mode: %d\n"), dwMode);
    }
    else
    {
        MyHandleError(TEXT("Error during CryptGetKeyParam."));
    }

    // Read the initialization vector.

    //  Get the length of the initialization vector.
    if(!CryptGetKeyParam(
        hKey, 
        KP_IV, 
        NULL,     
        &dwCount, 
        0)) 
    {
        MyHandleError(TEXT("Error getting the IV length"));
    }

    // Get the initialization vector, itself.
    if(CryptGetKeyParam(
        hKey, 
        KP_IV, 
        pbData, 
        &dwCount, 
        0))
    {
        // Print the initialization vector.
        _tprintf(TEXT("Default IV:"));
        for(i = 0; i < dwCount; i++) 
        {
            _tprintf(TEXT("%2.2x "),pbData[i]);
        }

        _tprintf(TEXT("\n"));
    }
    else
    {
        MyHandleError(TEXT("Error getting the IV."));
    }

    //  Reset the initialization vector.
    if(CryptSetKeyParam(
        hKey,
        KP_IV,
        pbRandomData,
        0))
    {
        _tprintf(TEXT("New initialization vector is set.\n"));
    }
    else
    {
        MyHandleError(TEXT("The new IV was not set."));
    }

    // Read the new initialization vector.

    //  Get the length of the new initialization vector.
    if(!CryptGetKeyParam(
        hKey, 
        KP_IV, 
        NULL,     
        &dwCount, 
        0)) 
    {
        MyHandleError(TEXT("Error getting the IV length"));
    }

    // Get the initialization vector, itself.
    if(CryptGetKeyParam(
        hKey, 
        KP_IV, 
        pbData, 
        &dwCount, 
        0))
    {
        // Print the initialization vector.
        _tprintf(TEXT("RE-set IV:"));
        for(i = 0; i < dwCount; i++) 
        {
            _tprintf(TEXT("%2.2x "),pbData[i]);
        }
        
        _tprintf(TEXT("\n"));
    }
    else
    {
        MyHandleError(TEXT("Error getting the IV."));
    }

    //  Clean up.

    //  Destroy the session key.
    if(hKey)
    { 
        CryptDestroyKey(hKey);
    }

    // Release the provider handle.
    if(hProv)
    { 
        CryptReleaseContext(hProv, 0);
    }
} // End of main.

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(PTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.
```



 

 



