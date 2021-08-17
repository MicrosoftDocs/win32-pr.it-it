---
title: Esempio di inizializzazione dell'importazione DRM
description: Esempio di inizializzazione dell'importazione DRM
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows SDK formato multimediale,importazione DRM
- Windows MEDIA Format SDK, importazione
- Windows MEDIA Format SDK, codice di esempio
- Windows MEDIA Format SDK, esempi di codice
- digital rights management (DRM), importazione
- DRM (Digital Rights Management),importazione
- digital rights management (DRM), inizializzazione importazione
- DRM (Digital Rights Management),inizializzare l'importazione
- digital rights management (DRM), codice di esempio
- DRM (Digital Rights Management),codice di esempio
- DRM (Digital Rights Management), esempi di codice
- DRM (Digital Rights Management),esempi di codice
- API estese del client DRM, inizializzazione dell'importazione
- API client estese, inizializzazione importazione
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, codice di esempio
- API estese client,codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e91d0aac6e9d54dac4cd52de7d84140a9e6af580084bd22ccc0af7283900d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702122"
---
# <a name="initialize-drm-import-example"></a>Esempio di inizializzazione dell'importazione DRM

L'esempio di codice seguente illustra come inizializzare un oggetto writer DRM per L'importazione DRM:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di creazione di una chiave contente**](create-content-key-example.md)
</dt> <dt>

[**Esempio di creazione della chiave di sessione**](create-session-key-example.md)
</dt> <dt>

[**Esempi di importazione DRM**](drm-import-examples.md)
</dt> </dl>

 

 




