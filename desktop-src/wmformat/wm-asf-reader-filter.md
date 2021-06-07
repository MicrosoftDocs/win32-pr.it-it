---
title: Filtro lettore ASF WM (Windows Media Format 11 SDK)
description: Informazioni sul filtro lettore ASF WM.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,Lettore ASF WM
- DirectShow, Lettore ASF WM
- Filtri QASF, Lettore ASF WM
- Lettore ASF WM
- Advanced Systems Format (ASF),Lettore ASF WM
- ASF (Advanced Systems Format),Lettore ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444282"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="17525-109">Filtro lettore ASF WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="17525-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="17525-110">Quando viene specificato il nome di un file ASF o di un URL, il lettore ASF WM legge il contenuto compresso, analizza i flussi ed espone un pin di output per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="17525-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="17525-111">Questo filtro connette downstream al Windows Media Audio o Windows Media Video dmo, che esecuno la decompressione.</span><span class="sxs-lookup"><span data-stu-id="17525-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="17525-112">La ricerca è supportata se il file ASF è ricercabile.</span><span class="sxs-lookup"><span data-stu-id="17525-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="17525-113">Il lettore ASF WM applica timestamp agli esempi multimediali in base al timestamp nel file ASF, ma non modifica in alcun modo i timestamp.</span><span class="sxs-lookup"><span data-stu-id="17525-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="17525-114">Internamente, il filtro usa l'oggetto lettore di Windows Media Format per leggere il contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17525-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="17525-115">In DirectX SDK questo filtro non è il filtro di origine predefinito per i file ASF, quindi con tale SDK non è possibile usare questo filtro con il **metodo RenderFile.** È necessario aggiungerlo in modo esplicito al grafico dei filtri usando il relativo identificatore di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="17525-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="17525-116">Questo comportamento è diverso con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="17525-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="17525-117">Quando si installano le librerie di runtime di Windows Media Format SDK, WM ASF Reader viene registrato come filtro predefinito per i file ASF.</span><span class="sxs-lookup"><span data-stu-id="17525-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="17525-118">La tabella seguente contiene informazioni sul filtro Lettore ASF WM, ad esempio le interfacce e i tipi di supporti supportati.</span><span class="sxs-lookup"><span data-stu-id="17525-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="17525-119">Filtrare le informazioni</span><span class="sxs-lookup"><span data-stu-id="17525-119">Filter Information</span></span>                      |  <span data-ttu-id="17525-120">Tipi</span><span class="sxs-lookup"><span data-stu-id="17525-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17525-121">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="17525-121">Filter interfaces</span></span>      | <span data-ttu-id="17525-122">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (implementato parzialmente.</span><span class="sxs-lookup"><span data-stu-id="17525-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="17525-123">Vedere Osservazioni, **IWMReaderAdvanced2** (implementato parzialmente), **IWMDRMReader** (tramite **IServiceProvider)**</span><span class="sxs-lookup"><span data-stu-id="17525-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="17525-124">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="17525-124">Input pin media types</span></span>  | <span data-ttu-id="17525-125">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="17525-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="17525-126">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="17525-126">Input pin interfaces</span></span>   | <span data-ttu-id="17525-127">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="17525-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="17525-128">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="17525-128">Output pin media types</span></span> | <span data-ttu-id="17525-129">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="17525-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="17525-130">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="17525-130">Format type</span></span>            | <span data-ttu-id="17525-131">**VIDEOINFOHEADER2 se** il contenuto è [*interlacciato;*](wmformat-glossary.md)in caso **contrario, VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="17525-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="17525-132">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="17525-132">Output pin interfaces</span></span>  | <span data-ttu-id="17525-133">**IMediaSeeking,** **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="17525-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="17525-134">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="17525-134">Filter CLSID</span></span>           | <span data-ttu-id="17525-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="17525-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="17525-136">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="17525-136">Property Page CLSID</span></span>    | <span data-ttu-id="17525-137">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="17525-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="17525-138">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="17525-138">Executable</span></span>             | <span data-ttu-id="17525-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="17525-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="17525-140">Merito</span><span class="sxs-lookup"><span data-stu-id="17525-140">Merit</span></span>                  | <span data-ttu-id="17525-141">PROBABILITÀ \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="17525-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="17525-142">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="17525-142">Filter Category</span></span>        | <span data-ttu-id="17525-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="17525-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="17525-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="17525-144">Remarks</span></span>

<span data-ttu-id="17525-145">Il lettore ASF WM implementa parzialmente le interfacce **IWMReaderAdvanced** e **IWMReaderAdvanced2** per consentire alle applicazioni di accedere ai metodi in formato informativo sull'oggetto lettore.</span><span class="sxs-lookup"><span data-stu-id="17525-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="17525-146">L'implementazione del filtro passa semplicemente le chiamate all'interfaccia sull'oggetto reader.</span><span class="sxs-lookup"><span data-stu-id="17525-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="17525-147">I metodi di streaming non vengono implementati perché il filtro deve avere il controllo completo sul processo di streaming.</span><span class="sxs-lookup"><span data-stu-id="17525-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="17525-148">Vengono **implementati i metodi IWMReaderAdvanced** e **IWMReaderAdvanced2** seguenti:</span><span class="sxs-lookup"><span data-stu-id="17525-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="17525-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="17525-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="17525-150">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="17525-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="17525-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="17525-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="17525-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="17525-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="17525-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="17525-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="17525-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="17525-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="17525-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="17525-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="17525-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="17525-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="17525-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17525-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17525-158">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="17525-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="17525-159">**Lettura di file ASF in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="17525-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




