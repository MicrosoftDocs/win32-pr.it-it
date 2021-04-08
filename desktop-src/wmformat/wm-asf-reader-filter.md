---
title: Filtro di lettura ASF WM (Windows Media Format 11 SDK)
description: Filtro di lettura ASF WM
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF Reader
- DirectShow, WM ASF Reader
- Filtri QASF, lettore ASF WM
- Lettore ASF WM
- ASF (Advanced Systems Format), lettore WM ASF
- ASF (formato avanzato dei sistemi), lettore WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739383"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="a705e-109">Filtro di lettura ASF WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a705e-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a705e-110">Quando si specifica il nome di un file ASF o un URL, il lettore WM ASF legge il contenuto compresso, analizza i flussi ed espone un pin di output per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="a705e-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="a705e-111">Questo filtro si connette a valle al Windows Media Audio o Windows Media Video DMOs, che eseguono la decompressione.</span><span class="sxs-lookup"><span data-stu-id="a705e-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="a705e-112">La ricerca è supportata se il file ASF è ricercabile.</span><span class="sxs-lookup"><span data-stu-id="a705e-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="a705e-113">Il lettore WM ASF applica timestamp agli esempi di supporti basati sul timestamp nel file ASF, ma non modifica in alcun modo i timestamp.</span><span class="sxs-lookup"><span data-stu-id="a705e-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="a705e-114">Internamente, il filtro usa l'oggetto lettore Windows Media Format per leggere il contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a705e-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="a705e-115">In DirectX SDK, questo filtro non è il filtro di origine predefinito per i file ASF, quindi con tale SDK non è possibile usare questo filtro con il metodo **RenderFile** . è necessario aggiungerlo in modo esplicito al grafico di filtro utilizzando il relativo identificatore di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="a705e-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="a705e-116">Questo comportamento è diverso con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a705e-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="a705e-117">Quando si installano le librerie di runtime di Windows Media Format SDK, il lettore WM ASF viene registrato come filtro predefinito per i file ASF.</span><span class="sxs-lookup"><span data-stu-id="a705e-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="a705e-118">La tabella seguente contiene informazioni sul filtro WM ASF Reader, ad esempio le interfacce e i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="a705e-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a705e-119">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="a705e-119">Filter interfaces</span></span>      | <span data-ttu-id="a705e-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementato parzialmente.</span><span class="sxs-lookup"><span data-stu-id="a705e-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="a705e-121">Vedere la sezione Osservazioni.), **IWMReaderAdvanced2** (parzialmente implementato), **IWMDRMReader** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a705e-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="a705e-122">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="a705e-122">Input pin media types</span></span>  | <span data-ttu-id="a705e-123">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a705e-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="a705e-124">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="a705e-124">Input pin interfaces</span></span>   | <span data-ttu-id="a705e-125">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a705e-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="a705e-126">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="a705e-126">Output pin media types</span></span> | <span data-ttu-id="a705e-127">\_Video MEDIATYPE, \_ audio MEDIATYPE, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ filetransfer</span><span class="sxs-lookup"><span data-stu-id="a705e-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="a705e-128">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="a705e-128">Format type</span></span>            | <span data-ttu-id="a705e-129">**VIDEOINFOHEADER2** se il contenuto è [*interlacciato*](wmformat-glossary.md), in caso contrario **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="a705e-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="a705e-130">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="a705e-130">Output pin interfaces</span></span>  | <span data-ttu-id="a705e-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (tramite **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a705e-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="a705e-132">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="a705e-132">Filter CLSID</span></span>           | <span data-ttu-id="a705e-133">\_WMASFREADER CLSID</span><span class="sxs-lookup"><span data-stu-id="a705e-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a705e-134">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a705e-134">Property Page CLSID</span></span>    | <span data-ttu-id="a705e-135">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a705e-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a705e-136">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="a705e-136">Executable</span></span>             | <span data-ttu-id="a705e-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="a705e-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="a705e-138">Merito</span><span class="sxs-lookup"><span data-stu-id="a705e-138">Merit</span></span>                  | <span data-ttu-id="a705e-139">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="a705e-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a705e-140">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="a705e-140">Filter Category</span></span>        | <span data-ttu-id="a705e-141">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="a705e-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a705e-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="a705e-142">Remarks</span></span>

<span data-ttu-id="a705e-143">Il lettore WM ASF implementa parzialmente le interfacce **IWMReaderAdvanced** e **IWMReaderAdvanced2** per consentire alle applicazioni di accedere ai metodi informativi nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="a705e-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="a705e-144">L'implementazione del filtro passa semplicemente le chiamate attraverso all'interfaccia sull'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="a705e-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="a705e-145">I metodi di streaming non sono implementati perché il filtro deve avere il controllo completo sul processo di streaming.</span><span class="sxs-lookup"><span data-stu-id="a705e-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="a705e-146">Vengono implementati i seguenti metodi **IWMReaderAdvanced** e **IWMReaderAdvanced2** :</span><span class="sxs-lookup"><span data-stu-id="a705e-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="a705e-147">**IWMReaderAdvanced:: GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="a705e-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="a705e-148">**IWMReaderAdvanced:: SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="a705e-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="a705e-149">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="a705e-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="a705e-150">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="a705e-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="a705e-151">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="a705e-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="a705e-152">**IWMReaderAdvanced2:: getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="a705e-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="a705e-153">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="a705e-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="a705e-154">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="a705e-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="a705e-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a705e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a705e-156">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="a705e-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="a705e-157">**Lettura di file ASF in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="a705e-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




