---
title: Esempio di creazione di una chiave di sessione
description: Esempio di creazione di una chiave di sessione
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows MEDIA Format SDK, chiavi di sessione
- Windows Media Format SDK, chiavi di contenuto
- Windows Media Format SDK, codice di esempio
- Windows Media Format SDK, esempi di codice
- digital rights management (DRM), chiavi di sessione
- DRM (digital rights management), chiavi di sessione
- digital rights management (DRM), chiavi di contenuto
- DRM (digital rights management),chiavi di contenuto
- digital rights management (DRM), codice di esempio
- DRM (digital rights management),codice di esempio
- digital rights management (DRM), esempi di codice
- DRM (digital rights management),esempi di codice
- API estese del client DRM, chiavi di sessione
- API estese client, chiavi di sessione
- API estese del client DRM, chiavi di contenuto
- API estese client, chiavi di contenuto
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
- chiavi di sessione
- chiavi di contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef4a9c673b0aef24e010bff0f9a84beaf6321a81fe4ac8a8a9935c126983eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964140"
---
# <a name="create-session-key-example"></a>Esempio di creazione di una chiave di sessione

La chiave di sessione viene usata per proteggere la chiave contenuto. Il codice seguente illustra come creare una chiave di sessione, ma lascia i dettagli della generazione casuale della chiave.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi di importazione DRM**](drm-import-examples.md)
</dt> </dl>

 

 




