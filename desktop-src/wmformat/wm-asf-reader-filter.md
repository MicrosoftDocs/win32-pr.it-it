---
title: Filtro lettore ASF WM (Windows Media Format 11 SDK)
description: Informazioni sul filtro lettore ASF WM per Windows Media Format 11 SDK. Esaminare le informazioni sui filtri e vedere gli argomenti correlati.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,Lettore ASF WM
- DirectShow, Lettore ASF WM
- filtri QASF, Lettore ASF WM
- Lettore ASF WM
- Advanced Systems Format (ASF),Lettore ASF WM
- ASF (Advanced Systems Format),Lettore ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119646"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="2804c-110">Filtro lettore ASF WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="2804c-110">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="2804c-111">Quando viene specificato il nome di un file ASF o di un URL, il lettore ASF WM legge il contenuto compresso, analizza i flussi ed espone un pin di output per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="2804c-111">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="2804c-112">Questo filtro connette downstream al Windows Media Audio o Windows Media Video dmo, che esecuno la decompressione.</span><span class="sxs-lookup"><span data-stu-id="2804c-112">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="2804c-113">La ricerca è supportata se il file ASF è ricercabile.</span><span class="sxs-lookup"><span data-stu-id="2804c-113">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="2804c-114">Il lettore ASF WM applica timestamp agli esempi multimediali in base al timestamp nel file ASF, ma non modifica in alcun modo i timestamp.</span><span class="sxs-lookup"><span data-stu-id="2804c-114">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="2804c-115">Internamente, il filtro usa l'oggetto lettore di Windows Media Format per leggere il contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2804c-115">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="2804c-116">In DirectX SDK questo filtro non è il filtro di origine predefinito per i file ASF, quindi con tale SDK non è possibile usare questo filtro con il **metodo RenderFile.** È necessario aggiungerlo in modo esplicito al grafico dei filtri usando il relativo identificatore di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="2804c-116">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="2804c-117">Questo comportamento è diverso con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="2804c-117">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="2804c-118">Quando si installano le librerie di runtime di Windows Media Format SDK, WM ASF Reader viene registrato come filtro predefinito per i file ASF.</span><span class="sxs-lookup"><span data-stu-id="2804c-118">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="2804c-119">La tabella seguente contiene informazioni sul filtro Lettore ASF WM, ad esempio le interfacce e i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="2804c-119">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="2804c-120">Filtrare le informazioni</span><span class="sxs-lookup"><span data-stu-id="2804c-120">Filter Information</span></span>                      |  <span data-ttu-id="2804c-121">Tipi</span><span class="sxs-lookup"><span data-stu-id="2804c-121">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2804c-122">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="2804c-122">Filter interfaces</span></span>      | <span data-ttu-id="2804c-123">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (implementato parzialmente.</span><span class="sxs-lookup"><span data-stu-id="2804c-123">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="2804c-124">Vedere Osservazioni, **IWMReaderAdvanced2** (implementato parzialmente), **IWMDRMReader** (tramite **IServiceProvider)**</span><span class="sxs-lookup"><span data-stu-id="2804c-124">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="2804c-125">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="2804c-125">Input pin media types</span></span>  | <span data-ttu-id="2804c-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="2804c-126">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="2804c-127">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="2804c-127">Input pin interfaces</span></span>   | <span data-ttu-id="2804c-128">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="2804c-128">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="2804c-129">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="2804c-129">Output pin media types</span></span> | <span data-ttu-id="2804c-130">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="2804c-130">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="2804c-131">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="2804c-131">Format type</span></span>            | <span data-ttu-id="2804c-132">**VIDEOINFOHEADER2 se** il contenuto è [*interlacciato;*](wmformat-glossary.md)in caso **contrario, VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="2804c-132">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="2804c-133">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="2804c-133">Output pin interfaces</span></span>  | <span data-ttu-id="2804c-134">**IMediaSeeking,** **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="2804c-134">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="2804c-135">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="2804c-135">Filter CLSID</span></span>           | <span data-ttu-id="2804c-136">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="2804c-136">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="2804c-137">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="2804c-137">Property Page CLSID</span></span>    | <span data-ttu-id="2804c-138">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="2804c-138">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="2804c-139">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="2804c-139">Executable</span></span>             | <span data-ttu-id="2804c-140">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="2804c-140">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="2804c-141">Merito</span><span class="sxs-lookup"><span data-stu-id="2804c-141">Merit</span></span>                  | <span data-ttu-id="2804c-142">PROBABILITÀ \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="2804c-142">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="2804c-143">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="2804c-143">Filter Category</span></span>        | <span data-ttu-id="2804c-144">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2804c-144">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2804c-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="2804c-145">Remarks</span></span>

<span data-ttu-id="2804c-146">Il lettore ASF WM implementa parzialmente le interfacce **IWMReaderAdvanced** e **IWMReaderAdvanced2** per consentire alle applicazioni di accedere ai metodi in formato informativo sull'oggetto reader.</span><span class="sxs-lookup"><span data-stu-id="2804c-146">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="2804c-147">L'implementazione del filtro passa semplicemente le chiamate all'interfaccia sull'oggetto reader.</span><span class="sxs-lookup"><span data-stu-id="2804c-147">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="2804c-148">I metodi di streaming non vengono implementati perché il filtro deve avere il controllo completo sul processo di streaming.</span><span class="sxs-lookup"><span data-stu-id="2804c-148">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="2804c-149">Vengono **implementati i metodi IWMReaderAdvanced** e **IWMReaderAdvanced2** seguenti:</span><span class="sxs-lookup"><span data-stu-id="2804c-149">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="2804c-150">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="2804c-150">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="2804c-151">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="2804c-151">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="2804c-152">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="2804c-152">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="2804c-153">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="2804c-153">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="2804c-154">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="2804c-154">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="2804c-155">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="2804c-155">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="2804c-156">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="2804c-156">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="2804c-157">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="2804c-157">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="2804c-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2804c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2804c-159">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="2804c-159">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="2804c-160">**Lettura di file ASF in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="2804c-160">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




