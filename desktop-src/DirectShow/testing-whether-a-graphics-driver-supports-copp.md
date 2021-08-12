---
description: Verifica se un driver di grafica supporta COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Verifica se un driver di grafica supporta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651831"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Verifica se un driver di grafica supporta COPP

Certified Output Protection Protocol (COPP) consente a un'applicazione di proteggere il contenuto video durante il viaggio dalla scheda video al dispositivo di visualizzazione. Se un driver di grafica supporta COPP, il driver contiene una catena di certificati, firmata da Microsoft, che autentica il driver. Le applicazioni di riproduzione che usano COPP per applicare la protezione del contenuto devono convalidare la catena di certificati per assicurarsi che il driver non sia stato manomesso.

Tuttavia, potrebbe essere necessario controllare se un driver di grafica supporta COPP, senza convalidare il certificato. Ad esempio, quando un provider di supporti digitali elava una licenza DRM (Digital Rights Management), potrebbe essere necessario verificare se l'utente dispone di un driver di grafica abilitato per COPP. Non è necessario che il provider imposi il COPP nel momento in cui elava la licenza. deve solo verificare se il driver supporta COPP.

Il codice seguente illustra come verificare se un driver supporta COPP. L'applicazione deve passare il nome di un file video che verrà usato per testare il driver. Questa operazione è necessaria perché il filtro del renderer di combinazione video in Microsoft® DirectShow® inizializza una sessione COPP solo dopo la connessione del filtro. Questa funzione può essere inclusa in un'applicazione client per verificare se il driver è in grado di eseguire COPP.

> [!Note]  
> Se il computer dell'utente ha due schede grafiche, questa funzione testa il driver per la scheda grafica primaria, ma non la scheda grafica secondaria.

 


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

[Uso del protocollo di protezione dell'output certificato](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



