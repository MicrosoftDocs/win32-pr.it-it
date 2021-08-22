---
description: Il provider di base usa solo chiavi simmetriche a 40 bit.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nuova funzionalità di lunghezza della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1da54be20e2b7e238cc99e787a2871bea54b40b0c46e214b7280482dcd8232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407011"
---
# <a name="new-key-length-functionality"></a>Nuova funzionalità di lunghezza della chiave

Il provider di base usa solo chiavi simmetriche [*a*](../secgloss/s-gly.md)40 bit. L'aggiunta di chiavi più lunghe nel provider avanzato e il fatto che le chiavi importate possano essere di lunghezza arbitraria richiede un metodo per eseguire query sulla lunghezza di una chiave specifica. Per trovare la lunghezza effettiva di una chiave in bit, un utente può chiamare [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con il valore del parametro \_ KEYLEN KP. La lunghezza della chiave viene restituita nel **valore DWORD** a cui punta il *parametro pbData.*

> [!Note]  
> Per proteggersi da attacchi di [*tipo cryptanalysis*](../secgloss/c-gly.md) [](../secgloss/k-gly.md) di tipo stepping down, le applicazioni devono verificare la presenza di lunghezze di chiave insufficienti e notificare all'utente quando ne viene rilevata una.

 

Nell'esempio seguente viene illustrato come eseguire una query sulla lunghezza di una chiave.


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
