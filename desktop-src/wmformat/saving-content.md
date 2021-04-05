---
title: Salvataggio del contenuto
description: Salvataggio del contenuto
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, salvataggio contenuto
- Windows Media Format SDK, fast cache streaming
- Formato Advanced Systems (ASF), salvataggio contenuto
- ASF (formato avanzato dei sistemi), salvataggio del contenuto
- Advanced Systems Format (ASF), streaming fast cache
- ASF (formato avanzato dei sistemi), streaming fast cache
- flussi, salvataggio di contenuto
- Streaming fast cache, salvataggio contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724084"
---
# <a name="saving-content"></a><span data-ttu-id="f4135-111">Salvataggio del contenuto</span><span class="sxs-lookup"><span data-stu-id="f4135-111">Saving Content</span></span>

<span data-ttu-id="f4135-112">Usando questo SDK, un'applicazione può salvare il contenuto scaricato o trasmesso nel computer locale dell'utente, chiamando il metodo [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) sull'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="f4135-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="f4135-113">Per il contenuto trasmesso, il server deve usare il flusso fast cache, come descritto nella sezione [Abilitazione del flusso fast cache dal client](enabling-fast-cache-streaming-from-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="f4135-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="f4135-114">Per il contenuto trasmesso, il metodo **SaveFileAs** crea un file ASX che punta a un file ASF che contiene il contenuto salvato.</span><span class="sxs-lookup"><span data-stu-id="f4135-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="f4135-115">Se l'oggetto Reader esegue lo streaming di una playlist sul lato server, ogni voce viene salvata come file ASF separato e il file ASX punta a ognuno dei file ASF.</span><span class="sxs-lookup"><span data-stu-id="f4135-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="f4135-116">Per il contenuto scaricato, il metodo **SaveFileAs** crea semplicemente un file ASF.</span><span class="sxs-lookup"><span data-stu-id="f4135-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="f4135-117">Per salvare il contenuto in un file locale, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4135-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="f4135-118">Chiamare [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) con l'URL.</span><span class="sxs-lookup"><span data-stu-id="f4135-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="f4135-119">**Open** è una chiamata asincrona e restituisce immediatamente un valore.</span><span class="sxs-lookup"><span data-stu-id="f4135-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="f4135-120">Attendere il completamento dell'operazione, come descritto in [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="f4135-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="f4135-121">Eseguire una query sull'oggetto Reader per l'interfaccia [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .</span><span class="sxs-lookup"><span data-stu-id="f4135-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="f4135-122">Controllare se il contenuto può essere salvato chiamando il metodo [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) .</span><span class="sxs-lookup"><span data-stu-id="f4135-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="f4135-123">Se il metodo restituisce false, il contenuto non può essere salvato localmente.</span><span class="sxs-lookup"><span data-stu-id="f4135-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="f4135-124">In caso contrario, procedere al passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="f4135-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="f4135-125">Chiamare il metodo [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) per determinare se il server sta usando lo streaming fast cache.</span><span class="sxs-lookup"><span data-stu-id="f4135-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="f4135-126">Chiamare [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) con un nome file per il file locale.</span><span class="sxs-lookup"><span data-stu-id="f4135-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="f4135-127">Se il metodo **IsUsingFastCache** ha restituito true, assegnare al file il nome di un'estensione asx.</span><span class="sxs-lookup"><span data-stu-id="f4135-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="f4135-128">In caso contrario, assegnare al file il nome di un'estensione. ASF,. WMA o. wmv.</span><span class="sxs-lookup"><span data-stu-id="f4135-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="f4135-129">L'applicazione può annullare l'operazione di salvataggio mentre è in corso, chiamando il metodo [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .</span><span class="sxs-lookup"><span data-stu-id="f4135-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="f4135-130">Il contenuto salvato potrebbe essere protetto con DRM, quindi potrebbe non essere possibile riprodurre il file in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="f4135-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="f4135-131">Per ulteriori informazioni sulla protezione del contenuto, vedere [Digital Rights Management Features](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="f4135-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4135-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4135-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4135-133">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="f4135-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="f4135-134">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="f4135-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




