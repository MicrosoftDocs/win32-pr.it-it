---
title: Esempio di ottenere un certificato del computer
description: Esempio di ottenere un certificato del computer
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Media Format SDK, certificati computer
- Windows Media Format SDK, certificati
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice
- Digital Rights Management (DRM), certificati computer
- DRM (Digital Rights Management), certificati computer
- Digital Rights Management (DRM), certificati
- DRM (Digital Rights Management), certificati
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- API estese client DRM, certificati computer
- API estese client, certificati computer
- API estese del client DRM, certificati
- API estese client, certificati
- API estese del client DRM, codice di esempio
- API estese client, codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
- certificati, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396610"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="d981a-124">Esempio di ottenere un certificato del computer</span><span class="sxs-lookup"><span data-stu-id="d981a-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="d981a-125">Nell'esempio seguente viene illustrato come recuperare la raccolta di certificati del computer:</span><span class="sxs-lookup"><span data-stu-id="d981a-125">The following example shows how to retrieve the machine certificate collection:</span></span>


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d981a-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d981a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d981a-127">**Esempi di importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="d981a-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




