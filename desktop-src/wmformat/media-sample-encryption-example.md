---
title: Esempio di crittografia di esempio multimediale
description: Esempio di crittografia di esempio multimediale
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Media Format SDK, crittografia di esempio multimediale
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice
- Digital Rights Management (DRM), crittografia di esempio multimediale
- DRM (Digital Rights Management), crittografia di esempio multimediale
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- API estese del client DRM, crittografia di esempio multimediale
- API estese client, crittografia di esempio multimediale
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045310"
---
# <a name="media-sample-encryption-example"></a><span data-ttu-id="97c62-118">Esempio di crittografia di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="97c62-118">Media Sample Encryption Example</span></span>

<span data-ttu-id="97c62-119">Nell'esempio incompleto riportato di seguito viene illustrato come crittografare un esempio di supporto utilizzando la crittografia DRM.</span><span class="sxs-lookup"><span data-stu-id="97c62-119">The following incomplete example demonstrates how to encrypt a media sample using DRM encryption.</span></span> <span data-ttu-id="97c62-120">L'algoritmo di crittografia RC4 è stato escluso dall'esempio a causa di restrizioni dello spazio.</span><span class="sxs-lookup"><span data-stu-id="97c62-120">The RC4 encryption algorithm has been left out of the example due to space restrictions.</span></span>


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="97c62-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97c62-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97c62-122">**Esempi di importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="97c62-122">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




