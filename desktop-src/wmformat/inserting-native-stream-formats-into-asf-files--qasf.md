---
title: Inserimento di formati di flusso nativi in file ASF (QASF)
description: Inserimento di formati di flusso nativi in file ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media Format SDK, formati di flussi nativi (QASF)
- Windows Media Format SDK, inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK, DirectShow
- Formato di sistemi avanzati (ASF), inserimento di formati di flussi nativi (QASF)
- ASF (Advanced Systems Format), inserimento di formati di flusso nativi (QASF)
- ASF (Advanced Systems Format), formati di flussi nativi (QASF)
- ASF (formato avanzato dei sistemi), formati di flussi nativi (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, formati di flussi nativi (QASF)
- DirectShow, inserimento di formati di flusso nativi in file ASF (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856693"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="0c5a1-118">Inserimento di formati di flusso nativi in file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="0c5a1-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="0c5a1-119">Per impostazione predefinita, il [writer WM ASF](wm-asf-writer-filter.md) prevede flussi audio e video non compressi nei pin di input e usa Windows Media Format SDK per accedere ai codec Windows Media Audio e Windows Media video, che comprimono i flussi.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="0c5a1-120">Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="0c5a1-121">Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e Digital Rights Management (DRM), senza la necessità di transcodificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="0c5a1-122">Per creare un file ASF che contiene contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico del filtro a Monte del writer ASF WM e ignorare il meccanismo di compressione del writer ASF WM chiamando [**IConfigAsfWriter2:: separat**](iconfigasfwriter2-setparam.md) nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="0c5a1-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="0c5a1-123">Configurare quindi il filtro con il profilo desiderato.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="0c5a1-124">È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="0c5a1-125">In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="0c5a1-126">Per ulteriori informazioni, vedere [per creare file ASF con codec di terze parti](to-create-asf-files-using-third-party-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="0c5a1-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="0c5a1-127">Quando si connette il writer ASF WM al filtro upstream, usare il metodo **IGraphBuilder:: ConnectDirect** .</span><span class="sxs-lookup"><span data-stu-id="0c5a1-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="0c5a1-128">Non usare alcun metodo di "connessione intelligente", ad esempio **IGraphBuilder:: Connect** o **IGraphBuilder:: RenderFile** per connettere il filtro in quanto questa operazione Disabilita la modalità "bypass Compression" del filtro.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




