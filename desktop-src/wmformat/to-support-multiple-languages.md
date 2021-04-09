---
title: Per supportare più lingue
description: Per supportare più lingue
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, supporto del linguaggio
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- ASF (Advanced Systems Format), supporto per le lingue
- ASF (formato avanzato dei sistemi), supporto per le lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956264"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="daeef-112">Per supportare più lingue</span><span class="sxs-lookup"><span data-stu-id="daeef-112">To Support Multiple Languages</span></span>

<span data-ttu-id="daeef-113">È possibile supportare più lingue sia nei flussi che nei metadati.</span><span class="sxs-lookup"><span data-stu-id="daeef-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="daeef-114">Il nucleo del supporto di più lingue in Windows Media Format SDK è l'interfaccia [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , che mantiene un elenco delle lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="daeef-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="daeef-115">L'elenco di lingue fornisce a ogni lingua supportata un indice, che viene usato in vari oggetti nell'SDK quando si gestiscono più lingue.</span><span class="sxs-lookup"><span data-stu-id="daeef-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="daeef-116">Il metodo [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) aggiunge un linguaggio all'elenco.</span><span class="sxs-lookup"><span data-stu-id="daeef-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="daeef-117">È possibile identificare le lingue già presenti nell'elenco ottenendo il numero totale di lingue con [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e quindi scorrendo le lingue che chiamano [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) per ciascuna.</span><span class="sxs-lookup"><span data-stu-id="daeef-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="daeef-118">L'indice del linguaggio è in base zero.</span><span class="sxs-lookup"><span data-stu-id="daeef-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="daeef-119">Per configurare l'esclusione reciproca per lingua</span><span class="sxs-lookup"><span data-stu-id="daeef-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="daeef-120">La configurazione di un semplice oggetto di esclusione reciproca per lingua è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="daeef-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="daeef-121">Ogni flusso è ora associato a una lingua.</span><span class="sxs-lookup"><span data-stu-id="daeef-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="daeef-122">Il linguaggio associato a un flusso può essere impostato usando [**IWMStreamConfig3:: tolanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span><span class="sxs-lookup"><span data-stu-id="daeef-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="daeef-123">Una volta configurati tutti i flussi che si escludono a vicenda, è sufficiente creare un oggetto di esclusione reciproca come per qualsiasi altro tipo.</span><span class="sxs-lookup"><span data-stu-id="daeef-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="daeef-124">Chiamare quindi [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passando \_ \_ la lingua WMMUTEX CLSID per il tipo.</span><span class="sxs-lookup"><span data-stu-id="daeef-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="daeef-125">I flussi che si escludono a vicenda dalla lingua diventano più complessi quando i flussi esclusivi si escludono a vicenda anche per velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="daeef-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="daeef-126">In questo caso è necessario usare record che si escludono a vicenda, eseguendo i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="daeef-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="daeef-127">Creare un oggetto di esclusione reciproca per i flussi di velocità in bit diverse in ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="daeef-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="daeef-128">Per ulteriori informazioni sulla creazione di un oggetto di esclusione reciproca per velocità in bit, vedere [utilizzo dell'esclusione reciproca a più bit rate](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="daeef-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="daeef-129">Creare un oggetto di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="daeef-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="daeef-130">Chiamare [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) e pass CLSID \_ WMMUTEX \_ Language per specificare l'esclusività in base alla lingua.</span><span class="sxs-lookup"><span data-stu-id="daeef-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="daeef-131">Ottenere un puntatore all'interfaccia [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) dell'oggetto di esclusione reciproca creato nel passaggio 2 chiamando il metodo **QueryInterface** di [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="daeef-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="daeef-132">Chiamare il metodo [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una volta per ogni lingua, per creare record di flusso che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="daeef-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="daeef-133">Per ogni record creato nel passaggio 4, aggiungere i flussi della lingua appropriata con le chiamate a [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span><span class="sxs-lookup"><span data-stu-id="daeef-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="daeef-134">Per leggere file con più lingue</span><span class="sxs-lookup"><span data-stu-id="daeef-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="daeef-135">L'oggetto Reader fornisce metodi per identificare le lingue disponibili dei flussi in un file.</span><span class="sxs-lookup"><span data-stu-id="daeef-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="daeef-136">È possibile recuperare il numero di lingue supportate per un output chiamando [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span><span class="sxs-lookup"><span data-stu-id="daeef-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="daeef-137">È quindi possibile recuperare i dettagli relativi a ogni lingua con le chiamate a [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span><span class="sxs-lookup"><span data-stu-id="daeef-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="daeef-138">È possibile specificare la lingua da riprodurre passando l'indice di tale lingua al Reader con una chiamata a [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="daeef-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="daeef-139">Verrà selezionata la lingua specificata mantenendo la selezione automatica dei flussi per tutti gli altri oggetti di esclusione reciproca del file.</span><span class="sxs-lookup"><span data-stu-id="daeef-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daeef-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daeef-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daeef-141">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="daeef-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="daeef-142">**Interfaccia IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="daeef-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="daeef-143">**Interfaccia IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="daeef-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="daeef-144">**Interfaccia IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="daeef-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="daeef-145">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="daeef-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="daeef-146">**Interfaccia IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="daeef-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="daeef-147">**Interfaccia IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="daeef-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




