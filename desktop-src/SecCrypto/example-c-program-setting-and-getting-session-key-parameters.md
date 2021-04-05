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
# <a name="example-c-program-setting-and-getting-session-key-parameters"></a><span data-ttu-id="dec42-103">Esempio di programma C: impostazione e recupero dei parametri della chiave della sessione</span><span class="sxs-lookup"><span data-stu-id="dec42-103">Example C Program: Setting and Getting Session Key Parameters</span></span>

<span data-ttu-id="dec42-104">L'esempio seguente crea una chiave di sessione casuale, ottiene e stampa alcuni parametri predefiniti della chiave, imposta i nuovi parametri sulla chiave originale, quindi ottiene e stampa il valore del nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="dec42-104">The following example creates a random session key, gets and prints some default parameters of that key, sets a new parameters on the original key, then gets and prints the value of that new parameter.</span></span> <span data-ttu-id="dec42-105">Si pulisce eliminando la chiave della sessione e rilasciando il contesto crittografico.</span><span class="sxs-lookup"><span data-stu-id="dec42-105">It cleans up by destroying the session key and releasing the cryptographic context.</span></span>

<span data-ttu-id="dec42-106">In questo esempio viene illustrato l'utilizzo delle attività e delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dec42-106">This example illustrates the use of the following tasks and functions:</span></span>

-   <span data-ttu-id="dec42-107">Accesso a un CSP utilizzando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="dec42-107">Accessing a CSP using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="dec42-108">Archiviazione di un buffer con byte casuali tramite [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span><span class="sxs-lookup"><span data-stu-id="dec42-108">Filing a buffer with random bytes using [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span></span>
-   <span data-ttu-id="dec42-109">Creazione di una chiave di sessione mediante [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span><span class="sxs-lookup"><span data-stu-id="dec42-109">Creating a session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="dec42-110">Recupero del valore dei parametri chiave utilizzando [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="dec42-110">Getting the value of key parameters using [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam).</span></span>
-   <span data-ttu-id="dec42-111">Uso di [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) per modificare il processo di generazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="dec42-111">Using [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) to alter the key generation process.</span></span>
-   <span data-ttu-id="dec42-112">Eliminazione delle chiavi tramite [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="dec42-112">Destroying the keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="dec42-113">Rilascio del CSP con [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="dec42-113">Releasing the CSP with [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="dec42-114">In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="dec42-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="dec42-115">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="dec42-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="dec42-116">Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="dec42-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


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



 

 



