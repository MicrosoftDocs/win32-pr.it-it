---
title: Riproduzione del flusso Web in DirectShow
description: Riproduzione del flusso Web in DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, riproduzione del flusso Web
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), riproduzione del flusso Web
- ASF (formato avanzato dei sistemi), riproduzione del flusso Web
- DirectShow, riproduzione del flusso Web
- Flussi Web, DirectShow
- Flussi Web, riproduzione in DirectShow
- flussi, riproduzione del flusso Web in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955291"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="f2efa-113">Riproduzione del flusso Web in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2efa-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="f2efa-114">Microsoft DirectShow supporta i flussi Web (vedere [flussi Web](web-streams.md) per altre informazioni) negli scenari di riproduzione dei file tramite il filtro di [lettura ASF WM](wm-asf-reader-filter.md) , ma è necessario scrivere un filtro DirectShow personalizzato per acquisire e salvare in modo permanente il flusso.</span><span class="sxs-lookup"><span data-stu-id="f2efa-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="f2efa-115">Per riprodurre i flussi Web nel contenuto trasmesso da un server che esegue Servizi Windows Media, utilizzare il controllo ActiveX® della serie Windows Media Player 9 incorporato in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="f2efa-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="f2efa-116">Quando si specifica un file contenente flussi di tipo \_ filetransfer WMMEDIATYPE, il lettore WM ASF creerà un pin di output per tale file.</span><span class="sxs-lookup"><span data-stu-id="f2efa-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="f2efa-117">Il blocco di formato sarà una struttura del [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) .</span><span class="sxs-lookup"><span data-stu-id="f2efa-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="f2efa-118">Se non è disponibile alcun filtro downstream in grado di gestire tale tipo di supporto, il pin rimarrà non connesso, ma il file continuerà a riprodurre i flussi audio e/o video.</span><span class="sxs-lookup"><span data-stu-id="f2efa-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="f2efa-119">È importante comprendere che ogni esempio di supporto in un flusso Web contiene una struttura [**di \_ intestazione di \_ esempio \_ webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , che ha una lunghezza variabile a seconda della lunghezza del membro **wszURL** .</span><span class="sxs-lookup"><span data-stu-id="f2efa-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="f2efa-120">Il puntatore ai dati di esempio punta inizialmente a questa struttura ed è necessario far avanzare il puntatore oltre la struttura per accedere ai dati effettivi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="f2efa-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="f2efa-121">Il filtro del gestore del flusso Web deve essere basato sulla classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="f2efa-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="f2efa-122">Nel metodo **DoRenderSample** il filtro dovrà analizzare la struttura per ottenere informazioni sul flusso Web e quindi eseguire l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="f2efa-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="f2efa-123">In genere, questa operazione comporterà il salvataggio del file su disco e la chiamata a **CommitUrlCacheEntry** e **CreateUrlCacheEntry** per inserire i file nella cache di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f2efa-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="f2efa-124">Il filtro deve gestire i file multipart, ovvero i file più grandi di un campione, e deve anche gestire i comandi di rendering, che sono specificati dal membro **WMT \_ webstream \_ Sample \_ header. wSampleType** .</span><span class="sxs-lookup"><span data-stu-id="f2efa-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="f2efa-125">Il filtro Invia un **\_ \_ evento OLE EC** all'applicazione, insieme al testo dell' **intestazione di \_ esempio webstream WMT \_ . stringa \_ wszURL** che contiene il nome del file di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="f2efa-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="f2efa-126">L'applicazione fa quindi in modo che nel browser venga visualizzata la pagina specificata.</span><span class="sxs-lookup"><span data-stu-id="f2efa-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="f2efa-127">Se il flusso Web è stato creato correttamente, il file deve essere già presente nella cache.</span><span class="sxs-lookup"><span data-stu-id="f2efa-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="f2efa-128">Per ulteriori informazioni sugli **\_ \_ eventi OLE** **CBaseRenderer**, **DoRenderSample** e EC, vedere la documentazione relativa a DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="f2efa-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2efa-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2efa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2efa-130">**Flussi Web**</span><span class="sxs-lookup"><span data-stu-id="f2efa-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




