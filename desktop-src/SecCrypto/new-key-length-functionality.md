---
description: Il provider di base usava solo chiavi simmetriche a 40 bit.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nuove funzionalità per la lunghezza della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233496"
---
# <a name="new-key-length-functionality"></a>Nuove funzionalità per la lunghezza della chiave

Il provider di base usava solo [*chiavi simmetriche*](../secgloss/s-gly.md)a 40 bit. L'aggiunta di chiavi più lunghe nel provider migliorato e il fatto che le chiavi importate possono essere di lunghezza arbitraria richiede un metodo per eseguire una query sulla lunghezza per una chiave specifica. Per trovare la lunghezza effettiva di una chiave in bit, un utente può chiamare [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con il \_ valore del parametro KP KEYLEN. La lunghezza della chiave viene restituita nella **DWORD** a cui punta il parametro *pbData* .

> [!Note]  
> Per proteggersi dagli attacchi di [*crittanalisi*](../secgloss/c-gly.md) in fase di esecuzione, le applicazioni devono verificare la presenza di [*lunghezze di chiave*](../secgloss/k-gly.md) insufficienti e inviare una notifica all'utente.

 

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



 

 
