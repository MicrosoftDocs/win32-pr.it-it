---
title: Una playlist di esempio di Radio Station
description: Una playlist di esempio di Radio Station
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Playlist Windows Media Metafile, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Playlist Windows Media Metafile, esempio di playlist della stazione radio
- playlist, esempio di playlist della stazione radio
- playlist di metafile, esempio di playlist della stazione radio
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Esempio di playlist di Windows Media Player, Radio Station
- esempi di playlist
- playlist di esempio
- playlist di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395739"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="efc3e-125">Una playlist di esempio di Radio Station</span><span class="sxs-lookup"><span data-stu-id="efc3e-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="efc3e-126">Il codice di esempio seguente illustra come creare una playlist per analizzare tre stazioni radio rock.</span><span class="sxs-lookup"><span data-stu-id="efc3e-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="efc3e-127">Il marchio di radio Adventure Works fittizio si trova nella playlist e in tutti i singoli flussi all'interno della playlist.</span><span class="sxs-lookup"><span data-stu-id="efc3e-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="efc3e-128">Quando si scrive il codice, modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="efc3e-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="efc3e-129">Viene creata una playlist per ogni stazione.</span><span class="sxs-lookup"><span data-stu-id="efc3e-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="efc3e-130">Una quarta playlist analizza i primi tre.</span><span class="sxs-lookup"><span data-stu-id="efc3e-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="efc3e-131">Le playlist vengono create per fare riferimento a inserzioni generate in modo dinamico e hanno la personalizzazione di Adventure Works radio.</span><span class="sxs-lookup"><span data-stu-id="efc3e-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="efc3e-132">Una delle playlist che rappresenta una stazione radio potrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="efc3e-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="efc3e-133">La playlist può quindi essere costruita con riferimenti alle singole playlist.</span><span class="sxs-lookup"><span data-stu-id="efc3e-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="efc3e-134">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="efc3e-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="efc3e-135">In questo esempio viene riprodotto un annuncio seguito da 30 secondi di ognuna delle tre stazioni a cui viene fatto riferimento, una dopo l'altra.</span><span class="sxs-lookup"><span data-stu-id="efc3e-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="efc3e-136">Questo ciclo si ripete per un periodo illimitato perché l'attributo **count** dell'elemento **Repeat** non è definito.</span><span class="sxs-lookup"><span data-stu-id="efc3e-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="efc3e-137">Ogni riferimento a società, organizzazioni, prodotti, persone ed eventi utilizzati negli esempi è puramente casuale</span><span class="sxs-lookup"><span data-stu-id="efc3e-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="efc3e-138">e ha il solo scopo di illustrare l'uso del prodotto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efc3e-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efc3e-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efc3e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efc3e-140">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="efc3e-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="efc3e-141">**Playlist di esempio**</span><span class="sxs-lookup"><span data-stu-id="efc3e-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="efc3e-142">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="efc3e-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="efc3e-143">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="efc3e-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="efc3e-144">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="efc3e-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




