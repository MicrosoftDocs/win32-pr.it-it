---
title: Filtro WRITER ASF WM (Windows Media Format 11 SDK)
description: Informazioni sul filtro WM ASF Writer.
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
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444702"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="a2465-109">Filtro WRITER ASF WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a2465-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a2465-110">Il filtro WM ASF Writer accetta un numero variabile di flussi di input e crea un file ASF.</span><span class="sxs-lookup"><span data-stu-id="a2465-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="a2465-111">Il filtro gestisce tutti i tipi di compressione e multiplexing (anche se il meccanismo di compressione può essere ignorato).</span><span class="sxs-lookup"><span data-stu-id="a2465-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="a2465-112">È possibile usare il filtro WM ASF Writer in vari scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di file multimediali digitali Audio-Video interleaved (AVI) o MPEG per lo streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="a2465-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="a2465-113">Questo filtro rappresenta l'unico modo per creare file Windows Media Audio e Windows Media Video Microsoft in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a2465-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="a2465-114">Per altre informazioni, vedere [Creazione di file ASF in DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="a2465-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="a2465-115">La tabella seguente contiene informazioni sul filtro WM ASF Writer, ad esempio le interfacce e i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="a2465-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="a2465-116">Filtrare le informazioni</span><span class="sxs-lookup"><span data-stu-id="a2465-116">Filter Information</span></span>                       |  <span data-ttu-id="a2465-117">Tipi</span><span class="sxs-lookup"><span data-stu-id="a2465-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2465-118">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="a2465-118">Filter interfaces</span></span>      | <span data-ttu-id="a2465-119">**IAMFilterMiscFlags,** **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="a2465-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="a2465-120">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="a2465-120">Input pin media types</span></span>  | <span data-ttu-id="a2465-121">Dipende dal profilo.</span><span class="sxs-lookup"><span data-stu-id="a2465-121">Dependent on the profile.</span></span> <span data-ttu-id="a2465-122">In genere tipi non compressi come MEDIATYPE Audio o MEDIATYPE Video, anche se i tipi compressi possono essere accettati \_ \_ se corrispondono al profilo</span><span class="sxs-lookup"><span data-stu-id="a2465-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="a2465-123">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="a2465-123">Input pin interfaces</span></span>   | <span data-ttu-id="a2465-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a2465-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="a2465-125">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="a2465-125">Output pin media types</span></span> | <span data-ttu-id="a2465-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a2465-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="a2465-127">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="a2465-127">Output pin interfaces</span></span>  | <span data-ttu-id="a2465-128">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a2465-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="a2465-129">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="a2465-129">Filter CLSID</span></span>           | <span data-ttu-id="a2465-130">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="a2465-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="a2465-131">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a2465-131">Property page CLSID</span></span>    | <span data-ttu-id="a2465-132">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="a2465-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="a2465-133">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="a2465-133">Executable</span></span>             | <span data-ttu-id="a2465-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="a2465-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="a2465-135">Merito</span><span class="sxs-lookup"><span data-stu-id="a2465-135">Merit</span></span>                  | <span data-ttu-id="a2465-136">NON \_ \_ USARE \_</span><span class="sxs-lookup"><span data-stu-id="a2465-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="a2465-137">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="a2465-137">Filter Category</span></span>        | <span data-ttu-id="a2465-138">Non specificato</span><span class="sxs-lookup"><span data-stu-id="a2465-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="a2465-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2465-139">Remarks</span></span>

<span data-ttu-id="a2465-140">Il numero di pin di input nel filtro dipende dal profilo passato al filtro.</span><span class="sxs-lookup"><span data-stu-id="a2465-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="a2465-141">Viene creato un pin del tipo di supporto appropriato per ogni flusso definito nel profilo.</span><span class="sxs-lookup"><span data-stu-id="a2465-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="a2465-142">I pin di input supportano un metodo **dall'interfaccia IAMStreamConfig:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="a2465-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="a2465-143">Tutti gli altri metodi restituiscono E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a2465-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="a2465-144">Chiamare il **metodo GetFormat** per eseguire una query sul formato di compressione di destinazione del pin, definito dal profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="a2465-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="a2465-145">Usare [**l'interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) per impostare il profilo.</span><span class="sxs-lookup"><span data-stu-id="a2465-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="a2465-146">L'interfaccia **IServiceProvider** del filtro consente alle applicazioni di recuperare [**l'interfaccia IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) definita in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a2465-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="a2465-147">**L'interfaccia IWMWriterAdvanced2** controlla la risoluzione deinterlacciamento video ed è utile se l'input è un'origine [*interlacciata,*](wmformat-glossary.md) ad esempio DV (video digitale).</span><span class="sxs-lookup"><span data-stu-id="a2465-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="a2465-148">Usare i **metodi GetInputSetting** **e SetInputSetting** per controllare la deinterlacing.</span><span class="sxs-lookup"><span data-stu-id="a2465-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="a2465-149">Non è consigliabile che i client usino uno degli altri metodi in questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a2465-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="a2465-150">Questa interfaccia può essere ottenuta solo dopo l'aggiunta del filtro al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a2465-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="a2465-151">Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="a2465-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a2465-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2465-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2465-153">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="a2465-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
