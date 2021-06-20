---
title: Lettura di file ASF in DirectShow (Windows Media Format 11 SDK)
description: La riproduzione dei file ASF viene gestita dal filtro lettore ASF WM. Informazioni sulla lettura dei file ASF in DirectShow in Windows Media Format 11 SDK.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK,lettura di file ASF
- Windows Media Format SDK,filtro lettore ASF WM
- Windows Media Format SDK, interfaccia IMediaSeeking
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format),DirectShow
- Advanced Systems Format (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- Advanced Systems Format (ASF), filtro lettore ASF WM
- ASF (Advanced Systems Format), filtro lettore ASF WM
- Advanced Systems Format (ASF), interfaccia IMediaSeeking
- ASF (Advanced Systems Format), interfaccia IMediaSeeking
- DirectShow,lettura di file ASF
- DirectShow, filtro lettore ASF WM
- Interfaccia DirectShow,IMediaSeeking
- Filtro lettore ASF WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404324"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lettura di file ASF in DirectShow (Windows Media Format 11 SDK)

La riproduzione dei file ASF viene gestita dal filtro [lettore ASF WM.](wm-asf-reader-filter.md) Quando il lettore ASF WM legge un file, crea automaticamente un pin di output per ogni flusso, inclusi flussi Web, flussi di comandi script e qualsiasi altro tipo di flusso arbitrario. Nel caso di più file di velocità in bit, i pin vengono creati solo per i flussi attualmente selezionati.

Wm ASF Reader supporta l'interfaccia **DirectShow IMediaSeeking,** che consente alle applicazioni di eseguire la ricerca temporale all'interno del file. Tuttavia, la riproduzione a velocità diverse dalla 1.0 (come specificato in **IMediaSeeking::SetRate)** non è supportata.

Il filtro espone anche diverse interfacce di Windows Media Format SDK, come descritto nella tabella seguente.



| Interfaccia                                        | Come viene esposto                            | Commenti                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Tramite **IServiceProvider su** filtro | Fornito per le applicazioni che devono riprodurre contenuto protetto da Digital Rights Management (DRM). Questa interfaccia può essere usata anche per ottenere direttamente altre interfacce nell'oggetto reader. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** su filtro           | Fornito in modo che le applicazioni possano leggere attributi di file e contenuto, nonché informazioni e metadati relativi a marcatori e script.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** su filtro           | Parzialmente implementata nel filtro in modo che le applicazioni possano accedere ai metodi in formato informativo nell'oggetto lettore WM.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** su filtro           | Parzialmente implementata nel filtro in modo che le applicazioni possano accedere ai metodi in informazioni sull'oggetto reader.                                                                         |



 

Il [filtro lettore ASF WM](wm-asf-reader-filter.md) è stato reso disponibile per la prima volta in DirectShow 8.0. La versione del filtro fornita con DirectShow 8.1 e 9.0 supporta la versione 7. *x* di Windows Media Format SDK. La versione più recente del filtro, insieme agli altri componenti QASF, viene fornita con e supporta Windows Media Format 9 Series SDK e versioni successive e sostituisce il filtro in DirectX 9.0. Se si installa Windows Media Format SDK dopo l'installazione di DirectX 8. *x* o 9. *x* SDK, si sovrascriverà la versione DirectX di qasf.dll con la versione serie 9. Questa operazione non deve presentare problemi tranne che in uno scenario in cui il comportamento sarà diverso nel metodo **DirectShow IGraphBuilder::RenderFile.** La versione di Windows Media Format 9 Series SDK di WM ASF Reader è il filtro di origine predefinito per le estensioni di file asf, wmv e wma. Ciò significa che il lettore ASF WM viene creato automaticamente e aggiunto al grafico dei filtri da Filter Graph Manager in metodi come **IGraphBuilder::RenderFile** o **IGraphBuilder::AddSourceFilter** quando viene specificato un file di questo tipo. In DirectX 9.0 e versioni precedenti e Windows XP Service Pack 1 e versioni precedenti, il **metodo RenderFile** usa il filtro origine Windows Media meno recente. Questo comportamento è stato mantenuto per garantire la compatibilità con le versioni precedenti con le applicazioni che Windows Media Player 6.4. Per altre informazioni sul filtro origine Windows Media legacy, vedere la documentazione di DirectShow SDK.

Per riprodurre un file ASF con contenuto basato su Windows Media usando WM ASF Reader, i tre passaggi principali sono creare un'istanza di Filter Graph Manager, chiamare **IGraphBuilder::RenderFile** per creare il grafo e quindi chiamare **IMediaControl::Run** per riprodurre il file. L'esempio di codice seguente è un programma completo che riproduce un file ASF usando DirectShow. Per eseguire questo esempio, è necessario che DirectX SDK sia installato e che l'ambiente di compilazione sia configurato in base alle istruzioni riportate nell'argomento della documentazione di DirectShow SDK "Impostazione dell'ambiente di compilazione". È inoltre necessario specificare un file nel computer nella chiamata a **RenderFile**.


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



Si noti che il codice dell'applicazione per questo semplice esempio non fa mai riferimento in modo specifico al lettore ASF WM. Tale filtro viene creato, connesso, eseguito e infine rilasciato da Filter Graph Manager. In molti scenari, tuttavia, può essere necessario configurare il lettore ASF WM prima di iniziare la riproduzione.

 

 




