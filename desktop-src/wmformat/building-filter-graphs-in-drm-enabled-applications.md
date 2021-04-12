---
title: Creazione di grafici di filtro in applicazioni DRM-Enabled
description: Creazione di grafici di filtro in applicazioni DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, creazione di grafici di filtro
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, applicazioni abilitate per DRM
- ASF (Advanced Systems Format), creazione di grafici di filtro
- ASF (Advanced Systems Format), compilazione di grafici di filtro
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), applicazioni abilitate per DRM
- ASF (Advanced Systems Format), applicazioni abilitate per DRM
- DirectShow, creazione di grafici di filtro
- DirectShow, applicazioni abilitate per DRM
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
- Digital Rights Management (DRM), creazione di grafici di filtro
- DRM (Digital Rights Management), compilazione di grafici di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336402"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="80daa-118">Creazione di grafici di filtro in applicazioni DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="80daa-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="80daa-119">Se l'applicazione DirectShow supporta la riproduzione di file protetti da DRM, in genere non è consigliabile usare **RenderFile** per creare il grafico dei filtri perché non è possibile specificare i diritti DRM richiesti prima dell'apertura del file.</span><span class="sxs-lookup"><span data-stu-id="80daa-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="80daa-120">Per impostazione predefinita, il lettore WM ASF richiede solo i diritti di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="80daa-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="80daa-121">Il filtro non viene aggiunto al grafo e pertanto non è individuabile dalle applicazioni, fino a quando un file non viene aperto correttamente.</span><span class="sxs-lookup"><span data-stu-id="80daa-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="80daa-122">Per creare un grafico di riproduzione abilitato per DRM usando il [lettore WM ASF](wm-asf-reader-filter.md), è necessario creare un'istanza del filtro usando **CoCreateInstance**, aggiungerlo al grafo del filtro usando **IGraphBuilder:: AddFilter**, configurarlo e quindi eseguire il rendering dei pin di output.</span><span class="sxs-lookup"><span data-stu-id="80daa-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="80daa-123">Questa tecnica è illustrata nell'esempio PlayWndASF.</span><span class="sxs-lookup"><span data-stu-id="80daa-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="80daa-124">Quando si compila il grafico in questo modo, è già presente il puntatore **IBaseFilter** che può essere usato per chiamare **QueryService** per ottenere **IWMDRMWriter**.</span><span class="sxs-lookup"><span data-stu-id="80daa-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="80daa-125">Questa interfaccia non è tuttavia disponibile fino a quando l'oggetto Reader di Windows Media Format SDK non viene creato internamente dal lettore WM ASF.</span><span class="sxs-lookup"><span data-stu-id="80daa-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="80daa-126">La prima opportunità per l'applicazione di impostare i diritti DRM è nel \_ \_ gestore eventi WMT no Rights \_ , come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="80daa-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="80daa-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80daa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80daa-128">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="80daa-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="80daa-129">**Elenco attributi DRM**</span><span class="sxs-lookup"><span data-stu-id="80daa-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="80daa-130">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="80daa-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="80daa-131">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="80daa-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="80daa-132">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="80daa-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="80daa-133">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="80daa-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




