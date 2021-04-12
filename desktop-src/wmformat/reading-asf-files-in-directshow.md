---
title: Lettura di file ASF in DirectShow (Windows Media Format 11 SDK)
description: Lettura di file ASF in DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lettura di file ASF
- Windows Media Format SDK, filtro WM ASF Reader
- Windows Media Format SDK, interfaccia IMediaSeeking
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- ASF (Advanced Systems Format), filtro WM ASF Reader
- ASF (Advanced Systems Format), filtro WM ASF Reader
- Advanced Systems Format (ASF), interfaccia IMediaSeeking
- ASF (formato avanzato dei sistemi), interfaccia IMediaSeeking
- DirectShow, lettura di file ASF
- Filtro DirectShow, WM ASF Reader
- DirectShow, interfaccia IMediaSeeking
- Filtro di lettura ASF WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340143"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lettura di file ASF in DirectShow (Windows Media Format 11 SDK)

La riproduzione dei file ASF viene gestita dal filtro [WM ASF Reader](wm-asf-reader-filter.md) . Quando il lettore WM ASF legge un file, viene creato automaticamente un pin di output per ogni flusso, inclusi i flussi Web, i flussi dei comandi di script e qualsiasi altro tipo di flusso arbitrario. Nel caso di file a più velocità in bit, i PIN vengono creati solo per i flussi attualmente selezionati.

Il lettore WM ASF supporta l'interfaccia DirectShow **IMediaSeeking** , che consente alle applicazioni di eseguire ricerche temporali all'interno del file. Tuttavia, la riproduzione a velocità diverse da 1,0 (come specificato in **IMediaSeeking:: serate**) non è supportata.

Il filtro espone inoltre diverse interfacce di Windows Media Format SDK, come descritto nella tabella seguente.



| Interfaccia                                        | Modalità di esposizione                            | Commenti                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Da **IServiceProvider** al filtro | Fornito per le applicazioni che devono riprodurre contenuti protetti da DRM (Digital Rights Management). Questa interfaccia può essere utilizzata anche per ottenere le altre interfacce direttamente sull'oggetto Reader. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** sul filtro           | Fornito in modo che le applicazioni possano leggere gli attributi di file e contenuto, nonché informazioni su marcatore e script e metadati.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** sul filtro           | Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** sul filtro           | Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto Reader.                                                                         |



 

Il filtro [WM ASF Reader](wm-asf-reader-filter.md) è stato reso disponibile per la prima volta in DirectShow 8,0. La versione del filtro fornita con DirectShow 8,1 e 9,0 supporta la versione 7. *x* di Windows Media Format SDK. La versione più recente del filtro, insieme agli altri componenti di QASF, viene fornita con e supporta Windows Media Format 9 Series SDK e versioni successive e sostituisce il filtro in DirectX 9,0. Se si installa Windows Media Format SDK dopo l'installazione di DirectX 8. *x* o 9. *x* SDK, la versione DirectX di qasf.dll viene sovrascritta con la versione serie 9. Questa situazione non dovrebbe presentare problemi tranne che in uno scenario in cui si otterrà un comportamento diverso nel metodo DirectShow **IGraphBuilder:: RenderFile** . La versione SDK di Windows Media Format 9 Series del lettore WM ASF è il filtro di origine predefinito per le estensioni di file con estensione ASF, WMV e WMA. Questo significa che il lettore WM ASF viene creato automaticamente e aggiunto al grafico del filtro da Filter Graph Manager nei metodi, ad esempio **IGraphBuilder:: RenderFile** o **IGraphBuilder:: AddSourceFilter** , quando viene specificato un file di questo tipo. In DirectX 9,0 e versioni precedenti e Windows XP Service Pack 1 e versioni precedenti, il metodo **RenderFile** usa il filtro sorgente Windows Media precedente. Questo comportamento è stato mantenuto per garantire la compatibilità con le applicazioni che usavano Windows Media Player 6,4. Per ulteriori informazioni sul filtro origine Windows Media legacy, vedere la documentazione di DirectShow SDK.

Per riprodurre un file ASF con contenuto basato su Windows Media usando il lettore WM ASF, i tre passaggi principali consiste nel creare un'istanza di Filter Graph Manager, chiamare **IGraphBuilder:: RenderFile** per creare il grafico e quindi chiamare **IMediaControl:: Run** per riprodurre il file. L'esempio di codice seguente è un programma completo che riproduce un file ASF con DirectShow. Per eseguire questo esempio, è necessario che sia installato DirectX SDK e che l'ambiente di compilazione sia configurato in base alle istruzioni riportate nell'argomento relativo alla configurazione dell'ambiente di compilazione nella documentazione di DirectShow SDK. Inoltre, è necessario specificare un file nel computer nella chiamata a **RenderFile**.


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



Si noti che il codice dell'applicazione per questo semplice esempio non fa mai riferimento al lettore WM ASF in modo specifico. Tale filtro viene creato, connesso, eseguito e infine rilasciato da Filter Graph Manager. In molti scenari, tuttavia, potrebbe essere necessario configurare il lettore di ASF WM prima di iniziare la riproduzione.

 

 




