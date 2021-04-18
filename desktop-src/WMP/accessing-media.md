---
title: Accesso ai supporti
description: Accesso ai supporti
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Playlist Windows Media Metafile, accesso ai file multimediali
- playlist, accesso ai file multimediali
- playlist di metafile, accesso ai file multimediali
- Playlist Windows Media Metafile, accesso multimediale
- playlist, accesso ai supporti
- playlist di metafile, accesso multimediale
- Playlist Windows Media Metafile, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Playlist Windows Media Metafile, impostazione durata
- playlist, impostazione della durata
- playlist di metafile, impostazione della durata
- Windows Media Player, accesso ai supporti
- Windows Media Player, accesso ai file multimediali
- Windows Media Player, controllo della riproduzione
- Media Player di Windows, impostazione della durata
- accesso ai supporti
- accesso ai supporti
- controllo della riproduzione
- impostazione della durata
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298577"
---
# <a name="accessing-media"></a><span data-ttu-id="74edf-123">Accesso ai supporti</span><span class="sxs-lookup"><span data-stu-id="74edf-123">Accessing Media</span></span>

<span data-ttu-id="74edf-124">Usare le playlist per specificare e controllare i supporti di streaming o i file multimediali che Windows Media Player riproduce.</span><span class="sxs-lookup"><span data-stu-id="74edf-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="74edf-125">Usare l'elemento **entry** per specificare un singolo elemento multimediale, ovvero un file multimediale o un flusso Live, e tutti gli elementi figlio, ad esempio immagini, collegamenti **moreinfo** e testo **astratto** .</span><span class="sxs-lookup"><span data-stu-id="74edf-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="74edf-126">Usare un elemento **ENTRYREF** per specificare una playlist.</span><span class="sxs-lookup"><span data-stu-id="74edf-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="74edf-127">Una playlist può contenere uno o più elementi **entry** o **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="74edf-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="74edf-128">Windows Media Player esegue una playlist iniziando dalla prima voce e quindi riproducendo ogni voce a sua volta fino al termine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="74edf-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="74edf-129">Un elemento **entry** può puntare a qualsiasi tipo di supporto che Windows Media Player possa riprodurre.</span><span class="sxs-lookup"><span data-stu-id="74edf-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="74edf-130">Sono inclusi i file WMA, WMV, ASF e AVI, per citarne alcuni, ma anche i flussi live.</span><span class="sxs-lookup"><span data-stu-id="74edf-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="74edf-131">Usando una serie di elementi **entry** o **ENTRYREF** per fare riferimento al contenuto multimediale, è possibile usare una playlist per inviare un singolo flusso costituito da più origini.</span><span class="sxs-lookup"><span data-stu-id="74edf-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="74edf-132">I flussi a cui si fa riferimento verranno riprodotti in sequenza e saranno considerati come un flusso continuo dal visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="74edf-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="74edf-133">La playlist può ad esempio contenere due elementi **entry** : un'introduzione standard da un file Windows Media con estensione WMA e un flusso di Windows Media Live.</span><span class="sxs-lookup"><span data-stu-id="74edf-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="74edf-134">Una playlist non deve contenere collegamenti a file multimediali con contenuto creato con diverse versioni di Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="74edf-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="74edf-135">In una playlist di metafile, se sono presenti collegamenti per i file multimediali con contenuto DRM versione 1 e per i file multimediali creati con versioni successive di DRM, Windows Media Player giocherà solo il contenuto di DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="74edf-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="74edf-136">Controllo della riproduzione</span><span class="sxs-lookup"><span data-stu-id="74edf-136">Controlling Playback</span></span>

<span data-ttu-id="74edf-137">Usare le playlist per controllare non solo quale clip multimediale viene riprodotto, ma anche quali parti della clip vengono riprodotte e come.</span><span class="sxs-lookup"><span data-stu-id="74edf-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="74edf-138">È possibile usare le playlist per definire un set di clip da ciclare o ripetere, per impostare la durata della riproduzione e per assegnare le ore di inizio e i marcatori di inizio e di fine per ogni voce.</span><span class="sxs-lookup"><span data-stu-id="74edf-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="74edf-139">Gli elementi **StartTime**, **STARTMARKER** e **ENDMARKER** funzionano insieme ai marcatori nel file multimediale.</span><span class="sxs-lookup"><span data-stu-id="74edf-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="74edf-140">Ad esempio, la playlist seguente usa un banner ad e il collegamento **moreinfo** associato in una **voce** e fa riferimento a **STARTMARKER** e **ENDMARKER**.</span><span class="sxs-lookup"><span data-stu-id="74edf-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="74edf-141">Impostazione della durata</span><span class="sxs-lookup"><span data-stu-id="74edf-141">Setting Duration</span></span>

<span data-ttu-id="74edf-142">Usare l'elemento **Duration** per specificare per quanto tempo riprodurre un clip o un set di clip.</span><span class="sxs-lookup"><span data-stu-id="74edf-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="74edf-143">È anche possibile usare l'attributo **PREVIEWMODE** dell'elemento **ASX** insieme all'elemento **PREVIEWDURATION** per specificare per quanto tempo riprodurre un clip o un set di clip.</span><span class="sxs-lookup"><span data-stu-id="74edf-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="74edf-144">Impostare l'attributo **PREVIEWMODE** su Yes per utilizzare l'elemento **PREVIEWDURATION** per specificare per quanto tempo riprodurre il clip associato.</span><span class="sxs-lookup"><span data-stu-id="74edf-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="74edf-145">Gli elementi **PREVIEWDURATION** e **Duration** hanno lo stesso comportamento.</span><span class="sxs-lookup"><span data-stu-id="74edf-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74edf-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74edf-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74edf-147">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="74edf-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="74edf-148">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="74edf-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="74edf-149">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="74edf-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="74edf-150">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="74edf-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




