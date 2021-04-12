---
title: Esempio di inizializzazione dell'importazione DRM
description: Esempio di inizializzazione dell'importazione DRM
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), inizializzare l'importazione
- DRM (Digital Rights Management), inizializzare l'importazione
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- API estese del client DRM, inizializzare l'importazione
- API estese client, inizializzazione importazione
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221974"
---
# <a name="initialize-drm-import-example"></a><span data-ttu-id="601d1-123">Esempio di inizializzazione dell'importazione DRM</span><span class="sxs-lookup"><span data-stu-id="601d1-123">Initialize DRM Import Example</span></span>

<span data-ttu-id="601d1-124">Nell'esempio di codice seguente viene illustrato come inizializzare un oggetto writer DRM per l'importazione DRM:</span><span class="sxs-lookup"><span data-stu-id="601d1-124">The following code example illustrates how to initialize a DRM writer object for DRM Import:</span></span>


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a><span data-ttu-id="601d1-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="601d1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="601d1-126">**Esempio di creazione della chiave simmetrica**</span><span class="sxs-lookup"><span data-stu-id="601d1-126">**Create Content Key Example**</span></span>](create-content-key-example.md)
</dt> <dt>

[<span data-ttu-id="601d1-127">**Esempio di creazione della chiave della sessione**</span><span class="sxs-lookup"><span data-stu-id="601d1-127">**Create Session Key Example**</span></span>](create-session-key-example.md)
</dt> <dt>

[<span data-ttu-id="601d1-128">**Esempi di importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="601d1-128">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




