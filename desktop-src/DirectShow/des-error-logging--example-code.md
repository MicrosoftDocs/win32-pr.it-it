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
# <a name="des-error-logging-example-code"></a><span data-ttu-id="e49dd-103">Registrazione degli errori DES: codice di esempio</span><span class="sxs-lookup"><span data-stu-id="e49dd-103">DES Error Logging: Example Code</span></span>

<span data-ttu-id="e49dd-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="e49dd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e49dd-105">Il codice di esempio seguente presenta un'applicazione console completa che carica e visualizza in anteprima un file di progetto XML di [servizi di modifica DirectShow](directshow-editing-services.md) , usando la classe di registrazione degli errori descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="e49dd-105">The following sample code presents a complete console application that loads and previews a [DirectShow Editing Services](directshow-editing-services.md) XML project file, using the error logging class described in this section.</span></span> <span data-ttu-id="e49dd-106">(Vedere [registrazione degli errori](logging-errors.md)). Il nome del file di progetto è hardcoded nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e49dd-106">(See [Logging Errors](logging-errors.md).) The name of the project file is hard-coded into the application.</span></span>

<span data-ttu-id="e49dd-107">Per rendere il codice più breve, l'applicazione console utilizza i puntatori intelligenti ATL, che elimina la necessità di chiamare **QueryInterface** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="e49dd-107">To make the code shorter, the console application uses ATL smart pointers, which removes the need to call **QueryInterface** and **Release**.</span></span> <span data-ttu-id="e49dd-108">Se si preferisce, è possibile modificare l'applicazione di esempio in [caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="e49dd-108">If you prefer, you can modify the sample application in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span> <span data-ttu-id="e49dd-109">È sufficiente aggiungere il codice illustrato nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="e49dd-109">Simply add the code shown in the previous section.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e49dd-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e49dd-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e49dd-111">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="e49dd-111">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



