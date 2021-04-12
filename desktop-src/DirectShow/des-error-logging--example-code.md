---
description: 'Registrazione degli errori DES: codice di esempio'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'Registrazione degli errori DES: codice di esempio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522778"
---
# <a name="des-error-logging-example-code"></a>Registrazione degli errori DES: codice di esempio

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il codice di esempio seguente presenta un'applicazione console completa che carica e visualizza in anteprima un file di progetto XML di [servizi di modifica DirectShow](directshow-editing-services.md) , usando la classe di registrazione degli errori descritta in questa sezione. (Vedere [registrazione degli errori](logging-errors.md)). Il nome del file di progetto è hardcoded nell'applicazione.

Per rendere il codice più breve, l'applicazione console utilizza i puntatori intelligenti ATL, che elimina la necessità di chiamare **QueryInterface** e **Release**. Se si preferisce, è possibile modificare l'applicazione di esempio in [caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md). È sufficiente aggiungere il codice illustrato nella sezione precedente.


```C++
#include <atlbase.h>
#include <dshow.h>
#include <qedit.h>
#include <stdio.h>

// Declare error logging class.
class CErrReporter;

// (The implementation of CErrReporter was given previously.)

void __cdecl main(void)
{
    HRESULT hr = CoInitialize(NULL);

    if (FAILED(hr))
    {
        // Error handling is omitted for clarity.
    }

    { // Scope for smart pointers.

    CComPtr<IAMTimeline>   pTL;
    CComPtr<IRenderEngine> pRenderEngine; 
    CComPtr<IXml2Dex>      pXML; 
    CComPtr<IGraphBuilder> pGraph;

    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**) &pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**) &pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**) &pRenderEngine);

    // Set the error log.
    CComQIPtr<IAMSetErrorLog, &IID_IAMSetErrorLog> pSetLog(pTL);
    if (pSetLog)
    {
        IAMErrorLog *pLog = new CErrReporter;    
        pSetLog->put_ErrorLog(pLog);
    }
   
    // Load and preview the project.
    CComBSTR bstrFile(OLESTR("C:\\example.xtl"));
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    if (SUCCEEDED(hr))
    {
        hr = pRenderEngine->SetTimelineObject(pTL);
        hr = pRenderEngine->ConnectFrontEnd( );
        hr = pRenderEngine->RenderOutputPins( );
        hr = pRenderEngine->GetFilterGraph(&pGraph);

        CComQIPtr<IMediaControl, &IID_IMediaControl> pControl(pGraph);
        CComQIPtr<IMediaEvent, &IID_IMediaEvent> pEvent(pGraph);
        pControl->Run();

        long evCode;
        hr = pEvent->WaitForCompletion(INFINITE, &evCode);
        pControl->Stop();
    }
    // Clean up.
    pRenderEngine->ScrapIt();
    }
    CoUninitialize();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



