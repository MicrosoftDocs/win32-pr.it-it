---
title: Per eseguire la transcodifica del contenuto con la ricompressione intelligente
description: Per eseguire la transcodifica del contenuto con la ricompressione intelligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK, codifica del contenuto
- Windows Media Format SDK, ricompressione intelligente
- Windows Media Format SDK, ricompressione
- Windows Media Format SDK, Windows Media Audio Codec
- ASF (Advanced Systems Format), codifica del contenuto
- ASF (formato avanzato dei sistemi), transcodifica del contenuto
- ASF (Advanced Systems Format), ricompressione intelligente
- ASF (formato avanzato dei sistemi), ricompressione intelligente
- ASF (Advanced Systems Format), ricompressione
- ASF (formato avanzato dei sistemi), ricompressione
- ASF (Advanced Systems Format), codec Windows Media Audio
- ASF (Advanced Systems Format), Windows Media Audio Codec
- transcodifica del contenuto
- ricompressione intelligente
- ricompressione
- Codec Windows Media Audio, transcodifica del contenuto
- codec, codec Windows Media Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336353"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="50be1-120">Per eseguire la transcodifica del contenuto con la ricompressione intelligente</span><span class="sxs-lookup"><span data-stu-id="50be1-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="50be1-121">È possibile transcodificare il contenuto da una velocità in bit a un'altra usando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="50be1-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="50be1-122">In genere, ciò implica semplicemente la decodifica del contenuto e la codifica di nuovo nella velocità in bit desiderata.</span><span class="sxs-lookup"><span data-stu-id="50be1-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="50be1-123">Il codec Windows Media Audio 9 supporta la ricompressione intelligente, che consente la transcodifica che ottiene una qualità migliore del normale.</span><span class="sxs-lookup"><span data-stu-id="50be1-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="50be1-124">Per la ricompressione intelligente, il flusso audio originale deve essere codificato con il codec Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="50be1-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="50be1-125">Sono supportate tutte le versioni del codec, ma i codec audio specializzati (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) non lo sono.</span><span class="sxs-lookup"><span data-stu-id="50be1-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="50be1-126">Se l'audio originale è stato codificato con il codec di Windows Media Audio 9 senza perdita di dati, non è necessario usare la ricompressione intelligente perché non è stata persa alcuna informazione nella codifica originale.</span><span class="sxs-lookup"><span data-stu-id="50be1-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="50be1-127">Per usare la ricompressione intelligente, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="50be1-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="50be1-128">Configurare un oggetto Reader con il file di origine per la lettura.</span><span class="sxs-lookup"><span data-stu-id="50be1-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="50be1-129">Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="50be1-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="50be1-130">Configurare un oggetto writer da usare per la transcodifica del file.</span><span class="sxs-lookup"><span data-stu-id="50be1-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="50be1-131">Impostare il nome del file per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="50be1-131">Set the file name for the new file.</span></span> <span data-ttu-id="50be1-132">Selezionare un profilo da usare per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="50be1-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="50be1-133">Imposta il profilo selezionato nell'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="50be1-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="50be1-134">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="50be1-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="50be1-135">Ottenere un puntatore all'interfaccia [**IWMProfile**](iwmprofile.md) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50be1-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="50be1-136">Recuperare l'interfaccia [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) per il flusso audio da transcodificare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="50be1-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="50be1-137">Ottenere l'interfaccia [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) per l'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50be1-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="50be1-138">Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="50be1-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="50be1-139">Ottenere le dimensioni della struttura alla prima chiamata e allocare la memoria per il passaggio di un buffer alla seconda chiamata.</span><span class="sxs-lookup"><span data-stu-id="50be1-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="50be1-140">Ottenere un puntatore all'interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per l'input nel writer chiamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="50be1-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="50be1-141">Ottenere l'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) per l'oggetto proprietà del supporto di input chiamando **IWMInputMediaProps:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50be1-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="50be1-142">Usare il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per impostare la proprietà g \_ wszOriginalWaveFormat.</span><span class="sxs-lookup"><span data-stu-id="50be1-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="50be1-143">Utilizzare la struttura **WAVEFORMATEX** ottenuta nel passaggio 6 come valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="50be1-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="50be1-144">Includere le modifiche apportate alle proprietà del supporto di input chiamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passandogli un puntatore all'interfaccia **IWMInputMediaProps** .</span><span class="sxs-lookup"><span data-stu-id="50be1-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="50be1-145">Iniziare a leggere gli esempi dal file originale e passarli al writer con le chiamate a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="50be1-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50be1-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50be1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50be1-147">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="50be1-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="50be1-148">**Interfaccia IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="50be1-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="50be1-149">**Interfaccia IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="50be1-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="50be1-150">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="50be1-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="50be1-151">**Interfaccia IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="50be1-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="50be1-152">**Interfaccia IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="50be1-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




