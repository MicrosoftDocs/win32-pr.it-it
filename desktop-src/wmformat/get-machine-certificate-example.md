---
title: Esempio di ottenere il certificato del computer
description: Esempio di ottenere il certificato del computer
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows MEDIA Format SDK, certificati computer
- Windows MEDIA Format SDK, certificati
- Windows MEDIA Format SDK, codice di esempio
- Windows MEDIA Format SDK, esempi di codice
- digital rights management (DRM), certificati computer
- DRM (Digital Rights Management),certificati computer
- digital rights management (DRM), certificati
- DRM (Digital Rights Management),certificati
- digital rights management (DRM), codice di esempio
- DRM (Digital Rights Management),codice di esempio
- DRM (Digital Rights Management), esempi di codice
- DRM (Digital Rights Management),esempi di codice
- API estese del client DRM, certificati del computer
- API client estese, certificati computer
- API estese del client DRM, certificati
- API estese client,certificati
- API estese del client DRM, codice di esempio
- API estese client,codice di esempio
- API estese del client DRM, esempi di codice
- API estese client, esempi di codice
- certificati, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964010"
---
# <a name="get-machine-certificate-example"></a>Esempio di ottenere il certificato del computer

L'esempio seguente illustra come recuperare la raccolta di certificati del computer:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi di importazione DRM**](drm-import-examples.md)
</dt> </dl>

 

 




