---
title: Filtro WM ASF Writer (Windows Media Format 11 SDK)
description: Informazioni sul filtro WM ASF Writer per Windows Media Format 11 SDK. Esaminare le informazioni sui filtri e vedere gli argomenti correlati.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK,WM ASF Writer
- DirectShow, WM ASF Writer
- filtri QASF, WM ASF Writer
- WM ASF Writer,about
- Advanced Systems Format (ASF),WM ASF Writer
- ASF (Advanced Systems Format),WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119666"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="997f5-110">Filtro WM ASF Writer (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="997f5-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="997f5-111">Il filtro WM ASF Writer accetta un numero variabile di flussi di input e crea un file ASF.</span><span class="sxs-lookup"><span data-stu-id="997f5-111">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="997f5-112">Il filtro gestisce tutti i tipi di compressione e multiplexing (anche se il meccanismo di compressione può essere ignorato).</span><span class="sxs-lookup"><span data-stu-id="997f5-112">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="997f5-113">È possibile usare il filtro WM ASF Writer in vari scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di file multimediali digitali Audio-Video interleaved (AVI) o MPEG per lo streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="997f5-113">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="997f5-114">Questo filtro rappresenta l'unico modo per creare file Windows Media Audio e Windows Media Video Microsoft in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="997f5-114">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="997f5-115">Per altre informazioni, vedere [Creazione di file ASF in DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="997f5-115">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="997f5-116">La tabella seguente contiene informazioni sul filtro WM ASF Writer, ad esempio le interfacce e i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="997f5-116">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="997f5-117">Filtrare le informazioni</span><span class="sxs-lookup"><span data-stu-id="997f5-117">Filter Information</span></span>                       |  <span data-ttu-id="997f5-118">Tipi</span><span class="sxs-lookup"><span data-stu-id="997f5-118">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="997f5-119">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="997f5-119">Filter interfaces</span></span>      | <span data-ttu-id="997f5-120">**IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="997f5-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="997f5-121">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="997f5-121">Input pin media types</span></span>  | <span data-ttu-id="997f5-122">Dipende dal profilo.</span><span class="sxs-lookup"><span data-stu-id="997f5-122">Dependent on the profile.</span></span> <span data-ttu-id="997f5-123">In genere tipi non compressi come MEDIATYPE Audio o MEDIATYPE Video, anche se i tipi compressi possono essere accettati \_ \_ se corrispondono al profilo</span><span class="sxs-lookup"><span data-stu-id="997f5-123">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="997f5-124">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="997f5-124">Input pin interfaces</span></span>   | <span data-ttu-id="997f5-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="997f5-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="997f5-126">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="997f5-126">Output pin media types</span></span> | <span data-ttu-id="997f5-127">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="997f5-127">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="997f5-128">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="997f5-128">Output pin interfaces</span></span>  | <span data-ttu-id="997f5-129">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="997f5-129">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="997f5-130">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="997f5-130">Filter CLSID</span></span>           | <span data-ttu-id="997f5-131">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="997f5-131">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="997f5-132">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="997f5-132">Property page CLSID</span></span>    | <span data-ttu-id="997f5-133">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="997f5-133">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="997f5-134">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="997f5-134">Executable</span></span>             | <span data-ttu-id="997f5-135">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="997f5-135">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="997f5-136">Merito</span><span class="sxs-lookup"><span data-stu-id="997f5-136">Merit</span></span>                  | <span data-ttu-id="997f5-137">NON \_ \_ USARE \_</span><span class="sxs-lookup"><span data-stu-id="997f5-137">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="997f5-138">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="997f5-138">Filter Category</span></span>        | <span data-ttu-id="997f5-139">Non specificato</span><span class="sxs-lookup"><span data-stu-id="997f5-139">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="997f5-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="997f5-140">Remarks</span></span>

<span data-ttu-id="997f5-141">Il numero di pin di input nel filtro dipende dal profilo passato al filtro.</span><span class="sxs-lookup"><span data-stu-id="997f5-141">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="997f5-142">Viene creato un pin del tipo di supporto appropriato per ogni flusso definito nel profilo.</span><span class="sxs-lookup"><span data-stu-id="997f5-142">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="997f5-143">I pin di input supportano un metodo **dall'interfaccia IAMStreamConfig:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="997f5-143">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="997f5-144">Tutti gli altri metodi restituiscono E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="997f5-144">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="997f5-145">Chiamare il **metodo GetFormat** per eseguire una query sul formato di compressione di destinazione del pin, definito dal profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="997f5-145">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="997f5-146">Usare [**l'interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) per impostare il profilo.</span><span class="sxs-lookup"><span data-stu-id="997f5-146">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="997f5-147">L'interfaccia **IServiceProvider** del filtro consente alle applicazioni di recuperare [**l'interfaccia IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) definita in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="997f5-147">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="997f5-148">**L'interfaccia IWMWriterAdvanced2** controlla la risoluzione deinterlacciamento video ed è utile se l'input è un'origine [*interlacciata,*](wmformat-glossary.md) ad esempio DV (video digitale).</span><span class="sxs-lookup"><span data-stu-id="997f5-148">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="997f5-149">Usare i **metodi GetInputSetting** **e SetInputSetting** per controllare la deinterlacing.</span><span class="sxs-lookup"><span data-stu-id="997f5-149">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="997f5-150">Non è consigliabile che i client usino uno degli altri metodi in questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="997f5-150">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="997f5-151">Questa interfaccia può essere ottenuta solo dopo l'aggiunta del filtro al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="997f5-151">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="997f5-152">Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="997f5-152">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="997f5-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="997f5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="997f5-154">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="997f5-154">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
