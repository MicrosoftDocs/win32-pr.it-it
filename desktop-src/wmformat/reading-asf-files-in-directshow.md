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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="11b39-120">Lettura di file ASF in DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="11b39-120">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="11b39-121">La riproduzione dei file ASF viene gestita dal filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="11b39-121">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="11b39-122">Quando il lettore WM ASF legge un file, viene creato automaticamente un pin di output per ogni flusso, inclusi i flussi Web, i flussi dei comandi di script e qualsiasi altro tipo di flusso arbitrario.</span><span class="sxs-lookup"><span data-stu-id="11b39-122">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="11b39-123">Nel caso di file a più velocità in bit, i PIN vengono creati solo per i flussi attualmente selezionati.</span><span class="sxs-lookup"><span data-stu-id="11b39-123">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="11b39-124">Il lettore WM ASF supporta l'interfaccia DirectShow **IMediaSeeking** , che consente alle applicazioni di eseguire ricerche temporali all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="11b39-124">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="11b39-125">Tuttavia, la riproduzione a velocità diverse da 1,0 (come specificato in **IMediaSeeking:: serate**) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="11b39-125">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="11b39-126">Il filtro espone inoltre diverse interfacce di Windows Media Format SDK, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="11b39-126">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="11b39-127">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="11b39-127">Interface</span></span>                                        | <span data-ttu-id="11b39-128">Modalità di esposizione</span><span class="sxs-lookup"><span data-stu-id="11b39-128">How exposed</span></span>                            | <span data-ttu-id="11b39-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="11b39-129">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11b39-130">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="11b39-130">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="11b39-131">Da **IServiceProvider** al filtro</span><span class="sxs-lookup"><span data-stu-id="11b39-131">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="11b39-132">Fornito per le applicazioni che devono riprodurre contenuti protetti da DRM (Digital Rights Management).</span><span class="sxs-lookup"><span data-stu-id="11b39-132">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="11b39-133">Questa interfaccia può essere utilizzata anche per ottenere le altre interfacce direttamente sull'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="11b39-133">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="11b39-134">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="11b39-134">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="11b39-135">**QueryInterface** sul filtro</span><span class="sxs-lookup"><span data-stu-id="11b39-135">**QueryInterface** on filter</span></span>           | <span data-ttu-id="11b39-136">Fornito in modo che le applicazioni possano leggere gli attributi di file e contenuto, nonché informazioni su marcatore e script e metadati.</span><span class="sxs-lookup"><span data-stu-id="11b39-136">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="11b39-137">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="11b39-137">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="11b39-138">**QueryInterface** sul filtro</span><span class="sxs-lookup"><span data-stu-id="11b39-138">**QueryInterface** on filter</span></span>           | <span data-ttu-id="11b39-139">Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto WM Reader.</span><span class="sxs-lookup"><span data-stu-id="11b39-139">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="11b39-140">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="11b39-140">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="11b39-141">**QueryInterface** sul filtro</span><span class="sxs-lookup"><span data-stu-id="11b39-141">**QueryInterface** on filter</span></span>           | <span data-ttu-id="11b39-142">Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="11b39-142">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="11b39-143">Il filtro [WM ASF Reader](wm-asf-reader-filter.md) è stato reso disponibile per la prima volta in DirectShow 8,0.</span><span class="sxs-lookup"><span data-stu-id="11b39-143">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="11b39-144">La versione del filtro fornita con DirectShow 8,1 e 9,0 supporta la versione 7. *x* di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="11b39-144">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="11b39-145">La versione più recente del filtro, insieme agli altri componenti di QASF, viene fornita con e supporta Windows Media Format 9 Series SDK e versioni successive e sostituisce il filtro in DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="11b39-145">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="11b39-146">Se si installa Windows Media Format SDK dopo l'installazione di DirectX 8. *x* o 9. *x* SDK, la versione DirectX di qasf.dll viene sovrascritta con la versione serie 9.</span><span class="sxs-lookup"><span data-stu-id="11b39-146">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="11b39-147">Questa situazione non dovrebbe presentare problemi tranne che in uno scenario in cui si otterrà un comportamento diverso nel metodo DirectShow **IGraphBuilder:: RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="11b39-147">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="11b39-148">La versione SDK di Windows Media Format 9 Series del lettore WM ASF è il filtro di origine predefinito per le estensioni di file con estensione ASF, WMV e WMA.</span><span class="sxs-lookup"><span data-stu-id="11b39-148">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="11b39-149">Questo significa che il lettore WM ASF viene creato automaticamente e aggiunto al grafico del filtro da Filter Graph Manager nei metodi, ad esempio **IGraphBuilder:: RenderFile** o **IGraphBuilder:: AddSourceFilter** , quando viene specificato un file di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="11b39-149">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="11b39-150">In DirectX 9,0 e versioni precedenti e Windows XP Service Pack 1 e versioni precedenti, il metodo **RenderFile** usa il filtro sorgente Windows Media precedente.</span><span class="sxs-lookup"><span data-stu-id="11b39-150">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="11b39-151">Questo comportamento è stato mantenuto per garantire la compatibilità con le applicazioni che usavano Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="11b39-151">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="11b39-152">Per ulteriori informazioni sul filtro origine Windows Media legacy, vedere la documentazione di DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="11b39-152">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="11b39-153">Per riprodurre un file ASF con contenuto basato su Windows Media usando il lettore WM ASF, i tre passaggi principali consiste nel creare un'istanza di Filter Graph Manager, chiamare **IGraphBuilder:: RenderFile** per creare il grafico e quindi chiamare **IMediaControl:: Run** per riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="11b39-153">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="11b39-154">L'esempio di codice seguente è un programma completo che riproduce un file ASF con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="11b39-154">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="11b39-155">Per eseguire questo esempio, è necessario che sia installato DirectX SDK e che l'ambiente di compilazione sia configurato in base alle istruzioni riportate nell'argomento relativo alla configurazione dell'ambiente di compilazione nella documentazione di DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="11b39-155">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="11b39-156">Inoltre, è necessario specificare un file nel computer nella chiamata a **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="11b39-156">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


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



<span data-ttu-id="11b39-157">Si noti che il codice dell'applicazione per questo semplice esempio non fa mai riferimento al lettore WM ASF in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="11b39-157">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="11b39-158">Tale filtro viene creato, connesso, eseguito e infine rilasciato da Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="11b39-158">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="11b39-159">In molti scenari, tuttavia, potrebbe essere necessario configurare il lettore di ASF WM prima di iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="11b39-159">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




