---
title: Filtro per writer ASF WM (Windows Media Format 11 SDK)
description: Filtro writer ASF WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, WM-writer ASF
- Filtri QASF, writer ASF WM
- Writer ASF WM, informazioni
- ASF (Advanced Systems Format), writer ASF WM
- ASF (formato avanzato dei sistemi), writer ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300787"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="1ab6f-109">Filtro per writer ASF WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="1ab6f-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1ab6f-110">Il filtro del writer ASF WM accetta un numero variabile di flussi di input e crea un file ASF.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="1ab6f-111">Il filtro gestisce tutte le compressioni e il multiplexing (anche se è possibile ignorare il meccanismo di compressione).</span><span class="sxs-lookup"><span data-stu-id="1ab6f-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="1ab6f-112">È possibile usare il filtro WM ASF Writer in diversi scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di Audio-Video file multimediali con interfoliazione (AVI) o MPEG digitali per lo streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="1ab6f-113">Questo filtro rappresenta l'unico modo per creare i file di Microsoft Windows Media Audio e Windows Media Video in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="1ab6f-114">Per altre informazioni, vedere [creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="1ab6f-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="1ab6f-115">La tabella seguente contiene informazioni sul filtro del writer ASF WM, ad esempio le interfacce e i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab6f-116">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1ab6f-116">Filter interfaces</span></span>      | <span data-ttu-id="1ab6f-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="1ab6f-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="1ab6f-118">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1ab6f-118">Input pin media types</span></span>  | <span data-ttu-id="1ab6f-119">Dipendente dal profilo.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-119">Dependent on the profile.</span></span> <span data-ttu-id="1ab6f-120">Tipi generalmente non compressi, ad esempio MEDIATYPE \_ audio o MEDIATYPE \_ video, sebbene i tipi compressi possano essere accettati se corrispondono al profilo</span><span class="sxs-lookup"><span data-stu-id="1ab6f-120">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="1ab6f-121">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1ab6f-121">Input pin interfaces</span></span>   | <span data-ttu-id="1ab6f-122">**Ipin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="1ab6f-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="1ab6f-123">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1ab6f-123">Output pin media types</span></span> | <span data-ttu-id="1ab6f-124">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="1ab6f-124">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="1ab6f-125">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1ab6f-125">Output pin interfaces</span></span>  | <span data-ttu-id="1ab6f-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="1ab6f-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="1ab6f-127">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1ab6f-127">Filter CLSID</span></span>           | <span data-ttu-id="1ab6f-128">\_WMASFWRITER CLSID</span><span class="sxs-lookup"><span data-stu-id="1ab6f-128">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="1ab6f-129">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1ab6f-129">Property page CLSID</span></span>    | <span data-ttu-id="1ab6f-130">\_WMASFWRITERPROPERTIES CLSID</span><span class="sxs-lookup"><span data-stu-id="1ab6f-130">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="1ab6f-131">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1ab6f-131">Executable</span></span>             | <span data-ttu-id="1ab6f-132">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="1ab6f-132">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="1ab6f-133">Merito</span><span class="sxs-lookup"><span data-stu-id="1ab6f-133">Merit</span></span>                  | <span data-ttu-id="1ab6f-134">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="1ab6f-134">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="1ab6f-135">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="1ab6f-135">Filter Category</span></span>        | <span data-ttu-id="1ab6f-136">Non specificato</span><span class="sxs-lookup"><span data-stu-id="1ab6f-136">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="1ab6f-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ab6f-137">Remarks</span></span>

<span data-ttu-id="1ab6f-138">Il numero di pin di input sul filtro dipende dal profilo passato al filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-138">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="1ab6f-139">Viene creato un pin del tipo di supporto appropriato per ogni flusso definito nel profilo.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-139">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="1ab6f-140">I pin di input supportano un metodo dell'interfaccia **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-140">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="1ab6f-141">Tutti gli altri metodi restituiscono E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-141">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="1ab6f-142">Chiamare il metodo **GetFormat** per eseguire una query sul formato di compressione della destinazione del PIN, definito dal profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-142">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="1ab6f-143">Usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) per impostare il profilo.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-143">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="1ab6f-144">L'interfaccia **IServiceProvider** del filtro consente alle applicazioni di recuperare l'interfaccia [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , definita in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-144">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="1ab6f-145">L'interfaccia **IWMWriterAdvanced2** controlla la deinterlacciamento dei video ed è utile se l'input è un'origine [*interlacciata*](wmformat-glossary.md) , ad esempio DV (video digitale).</span><span class="sxs-lookup"><span data-stu-id="1ab6f-145">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="1ab6f-146">Usare i metodi **GetInputSetting** e **SetInputSetting** per controllare la deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-146">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="1ab6f-147">Non è consigliabile che i client usino uno degli altri metodi su questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-147">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="1ab6f-148">Questa interfaccia può essere ottenuta solo dopo che il filtro è stato aggiunto al grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab6f-148">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="1ab6f-149">Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="1ab6f-149">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="1ab6f-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ab6f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab6f-151">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="1ab6f-151">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
