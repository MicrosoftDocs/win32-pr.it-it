---
title: Esempio di creazione della chiave della sessione
description: Esempio di creazione della chiave della sessione
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Media Format SDK, chiavi di sessione
- Windows Media Format SDK, chiavi simmetriche
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice
- Digital Rights Management (DRM), chiavi di sessione
- DRM (Digital Rights Management), chiavi di sessione
- Digital Rights Management (DRM), chiavi di contenuto
- DRM (Digital Rights Management), chiavi simmetriche
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- API estese del client DRM, chiavi di sessione
- API estese client, chiavi di sessione
- API estese del client DRM, chiavi simmetriche
- API estese client, chiavi simmetriche
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
- chiavi di sessione
- chiavi simmetriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045335"
---
# <a name="create-session-key-example"></a><span data-ttu-id="3d44b-125">Esempio di creazione della chiave della sessione</span><span class="sxs-lookup"><span data-stu-id="3d44b-125">Create Session Key Example</span></span>

<span data-ttu-id="3d44b-126">La chiave di sessione viene usata per proteggere la chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="3d44b-126">The session key is used to protect the content key.</span></span> <span data-ttu-id="3d44b-127">Il codice seguente illustra come creare una chiave di sessione, ma non i dettagli della generazione di chiavi casuali.</span><span class="sxs-lookup"><span data-stu-id="3d44b-127">The following code demonstrates how to create a session key, but leaves out the details of random key generation.</span></span>


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3d44b-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d44b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d44b-129">**Esempi di importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="3d44b-129">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




