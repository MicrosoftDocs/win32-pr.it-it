---
description: Verifica se un driver di grafica supporta COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Verifica se un driver di grafica supporta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316294"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Verifica se un driver di grafica supporta COPP

Certified Output Protection Protocol (COPP) consente a un'applicazione di proteggere il contenuto video mentre passa dalla scheda video al dispositivo di visualizzazione. Se un driver Graphics supporta COPP, il driver mantiene una catena di certificati, firmata da Microsoft, che esegue l'autenticazione del driver. Le applicazioni di riproduzione che usano COPP per applicare la protezione del contenuto devono convalidare la catena di certificati per garantire che il driver non sia stato alterato.

Tuttavia, potrebbe essere necessario controllare se un driver di grafica supporta COPP, senza convalidare il certificato. Ad esempio, quando un provider di contenuti multimediali digitali emette una licenza di Digital Rights Management (DRM), potrebbe essere necessario controllare se l'utente dispone di un driver della grafica abilitato per COPP. Il provider non deve applicare COPP quando rilascia la licenza; è necessario verificare solo se il driver supporta COPP.

Il codice seguente illustra come verificare se un driver supporta COPP. L'applicazione deve passare il nome di un file video che verrà usato per testare il driver. Questa operazione è necessaria perché il filtro renderer per la combinazione di video in Microsoft® DirectShow® non Inizializza una sessione COPP fino a quando il filtro non è connesso. Questa funzione può essere inclusa in un'applicazione client per verificare se il driver è in grado di eseguire COPP.

> [!Note]  
> Se nel computer dell'utente sono presenti due schede grafiche, questa funzione testa il driver per la scheda grafica primaria, ma non la scheda grafica secondaria.

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo di protezione output certificato](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



