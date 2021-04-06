---
title: Esempio di creazione della chiave simmetrica
description: Esempio di creazione della chiave simmetrica
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- Windows Media Format SDK, chiavi simmetriche
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice
- Digital Rights Management (DRM), chiavi di contenuto
- DRM (Digital Rights Management), chiavi simmetriche
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- API estese del client DRM, chiavi simmetriche
- API estese client, chiavi simmetriche
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
- chiavi simmetriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881dfd0d318d7d699b44ca9c3f77f22f9acfc689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045336"
---
# <a name="create-content-key-example"></a>Esempio di creazione della chiave simmetrica

La chiave simmetrica viene usata per crittografare esempi di contenuti multimediali per l'importazione DRM di Windows Media. Nell'esempio di codice riportato di seguito viene illustrato come creare e inizializzare una struttura di chiavi del contenuto.


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi di importazione DRM**](drm-import-examples.md)
</dt> </dl>

 

 




