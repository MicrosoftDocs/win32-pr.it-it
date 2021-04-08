---
description: Vengono illustrati diversi modi per utilizzare CryptAcquireContext e le funzioni CryptoAPI correlate per utilizzare un provider del servizio di crittografia (CSP) e un contenitore di chiavi.
ms.assetid: e8d2503c-a38f-44f6-a653-ae9c7bf903bd
title: 'Esempio di programma C: uso di CryptAcquireContext'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074d1967d8a32001e620b089280c034887b90cd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749570"
---
# <a name="example-c-program-using-cryptacquirecontext"></a><span data-ttu-id="e2e00-103">Esempio di programma C: uso di CryptAcquireContext</span><span class="sxs-lookup"><span data-stu-id="e2e00-103">Example C Program: Using CryptAcquireContext</span></span>

<span data-ttu-id="e2e00-104">Nell'esempio seguente vengono illustrati diversi modi per utilizzare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e le funzioni CryptoAPI correlate per utilizzare un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e un [*contenitore di chiavi*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2e00-104">The following example demonstrates several different ways to use the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) and related CryptoAPI functions to work with a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="e2e00-105">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2e00-105">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="e2e00-106">Utilizzare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per acquisire un handle per il CSP predefinito e il contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2e00-106">Use the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to acquire a handle for the default CSP and the default key container.</span></span> <span data-ttu-id="e2e00-107">Se non esiste un contenitore di chiavi predefinito, usare la funzione **CryptAcquireContext** per creare il contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2e00-107">If no default key container exists, use the **CryptAcquireContext** function to create the default key container.</span></span>
-   <span data-ttu-id="e2e00-108">Utilizzare la funzione [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) per recuperare informazioni su un provider CSP e un contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="e2e00-108">Use the [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) function to retrieve information about a CSP and a key container.</span></span>
-   <span data-ttu-id="e2e00-109">Aumentare il [*numero di riferimenti*](../secgloss/r-gly.md) nel provider utilizzando la funzione [**CryptContextAddRef**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref) .</span><span class="sxs-lookup"><span data-stu-id="e2e00-109">Increase the [*reference count*](../secgloss/r-gly.md) on the provider by using the [**CryptContextAddRef**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref) function.</span></span>
-   <span data-ttu-id="e2e00-110">Rilasciare un CSP utilizzando la funzione [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) .</span><span class="sxs-lookup"><span data-stu-id="e2e00-110">Release a CSP by using the [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) function.</span></span>
-   <span data-ttu-id="e2e00-111">Creare un contenitore di chiavi denominato usando la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="e2e00-111">Create a named key container by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span>
-   <span data-ttu-id="e2e00-112">Acquisire un handle per un CSP usando il contenitore di chiavi appena creato.</span><span class="sxs-lookup"><span data-stu-id="e2e00-112">Acquire a handle for a CSP by using the newly created key container.</span></span>
-   <span data-ttu-id="e2e00-113">Eliminare un contenitore di chiavi tramite la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="e2e00-113">Delete a key container by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span>

<span data-ttu-id="e2e00-114">In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="e2e00-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="e2e00-115">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="e2e00-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="e2e00-116">Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e00-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
//  Copyright (C) Microsoft.  All rights reserved.
//  Example code using CryptAcquireContext.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void main(void)
{
    //---------------------------------------------------------------
    // Declare and initialize variables.
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Get a handle to the default PROV_RSA_FULL provider.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
    }
    else
    {
        if (GetLastError() == NTE_BAD_KEYSET)
        {
            // No default container was found. Attempt to create it.
            if(CryptAcquireContext(
                &hCryptProv, 
                NULL, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create the default ")
                    TEXT("key container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("A general error running ")
                TEXT("CryptAcquireContext."));
        }
    }

    CHAR pszName[1000];
    DWORD cbName;

    //---------------------------------------------------------------
    // Read the name of the CSP.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_NAME, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Provider name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading CSP name.\n"));
    }

    //---------------------------------------------------------------
    // Read the name of the key container.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_CONTAINER, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Key Container name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading key container name.\n"));
    }
    //---------------------------------------------------------------
    // Perform cryptographic operations.
    //...

    //---------------------------------------------------------------
    //  Add to the reference count on the provider. When the 
    //  reference count on a provider is greater than one,  
    //  CryptReleaseContext reduces the reference count but does not 
    //  free the provider.

    if(CryptContextAddRef(
        hCryptProv, 
        NULL, 
        0)) 
    {
        _tprintf(TEXT("CryptcontextAddRef succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptContextAddRef!\n"));
    }

    //---------------------------------------------------------------
    //  The reference count on hCryptProv is now greater than one. 
    //  The first call to CryptReleaseContext will not release the 
    //  provider handle. 

    //---------------------------------------------------------------
    //  Release the context once.
    if (CryptReleaseContext(hCryptProv, 0))
    {
        _tprintf(TEXT("The first call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #1!\n"));
    }

    //---------------------------------------------------------------
    // Release the provider handle again.
    if (CryptReleaseContext(hCryptProv, 0)) 
    {
        _tprintf(TEXT("The second call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #2!\n"));
    }

    //---------------------------------------------------------------
    // Get a handle to a PROV_RSA_FULL provider and
    // create a key container named "My Sample Key Container".
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    hCryptProv = NULL;
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName,
        NULL, 
        PROV_RSA_FULL, 
        CRYPT_NEWKEYSET)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded. \n"));
        _tprintf(TEXT("New key set created. \n")); 

        //-----------------------------------------------------------
        // Release the provider handle and the key container.
        if(hCryptProv)
        {
            if(CryptReleaseContext(hCryptProv, 0)) 
            {
                hCryptProv = NULL;
                _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
            }
            else
            {
                MyHandleError(TEXT("Error during ")
                    TEXT("CryptReleaseContext!\n"));
            }
        }
    }
    else
    {
        if(GetLastError() == NTE_EXISTS)
        {
            _tprintf(TEXT("The named key container could not be ")
                TEXT("created because it already exists.\n"));
            
            // Just continue the program. The named container 
            // will be reopened below.
        }
        else
        {
            MyHandleError(TEXT("Error during CryptAcquireContext ")
                TEXT("for a new key container."));
        }
    }

    //---------------------------------------------------------------
    // Get a handle to the provider by using the new key container. 
    // Note: This key container will be empty until keys
    // are explicitly created by using the CryptGenKey function.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        0)) 
    {
        _tprintf(TEXT("Acquired the key set just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }

    //---------------------------------------------------------------
    // Perform cryptographic operations.

    //---------------------------------------------------------------
    // Release the provider handle.
    if(CryptReleaseContext(
        hCryptProv, 
        0)) 
    {
        _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptReleaseContext!\n"));
    }

    //---------------------------------------------------------------
    // Delete the new key container.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        CRYPT_DELETEKEYSET)) 
    {
        _tprintf(TEXT("Deleted the key container just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }
} // End of main.
```



 

 
