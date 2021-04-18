---
title: Uso dei metafile per un cambio di flusso trasparente
description: Uso dei metafile per un cambio di flusso trasparente
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Playlist Windows Media Metafile, cambio di flusso di eventi Live
- playlist, cambio di flusso di eventi Live
- playlist di metafile, cambio di flusso di eventi Live
- Playlist Windows Media Metafile, cambio di flusso di eventi
- playlist, cambio di flusso di eventi
- playlist di metafile, cambio di flusso di eventi
- Playlist Windows Media Metafile, inserimento ad
- playlist, inserimento di annunci
- playlist di metafile, inserimento di annunci
- Windows Media Player, cambio di flusso di eventi Live
- Windows Media Player, cambio del flusso di eventi
- Windows Media Player, inserimento di annunci
- cambio di flusso di eventi Live
- cambio di flusso di eventi
- inserimento ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297909"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="7559d-118">Uso dei metafile per un cambio di flusso trasparente</span><span class="sxs-lookup"><span data-stu-id="7559d-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="7559d-119">È possibile semplificare il cambio di flusso senza interruzioni usando le playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="7559d-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="7559d-120">In genere, quando viene terminata una parte di contenuto, il buffering viene eseguito per il clip o il flusso successivo prima che venga aperto, se è contenuto ricevuto da un server dei flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="7559d-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="7559d-121">Servizi multimediali di Microsoft Windows consente di eliminare o almeno ridurre al minimo il tempo di memorizzazione nel buffer e l'esecuzione di un'altra parte di contenuto trasmesso quasi immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7559d-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="7559d-122">La modalità di funzionamento normale per Windows Media Player consiste nell'aprire il successivo flusso multimediale a cui fa riferimento la playlist 20 secondi prima della fine del flusso attualmente sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="7559d-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="7559d-123">In genere fornisce una transizione senza problemi tra flussi multimediali, a seconda di altri fattori, ad esempio i tempi di accesso Web.</span><span class="sxs-lookup"><span data-stu-id="7559d-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="7559d-124">Usare l'elemento **Event** in una playlist insieme ai comandi OPENEVENT del codificatore per facilitare il cambio tra i flussi o i file.</span><span class="sxs-lookup"><span data-stu-id="7559d-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="7559d-125">L'invio di un comando OPENEVENT di 20 secondi o più prima del comando dell'evento può ridurre al minimo i ritardi nel cambio del flusso.</span><span class="sxs-lookup"><span data-stu-id="7559d-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="7559d-126">Quindi Windows Media Player è in grado di precaricare una parte del contenuto di streaming imminente in un buffer.</span><span class="sxs-lookup"><span data-stu-id="7559d-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="7559d-127">Usare Windows Media Encoder per inviare un comando script nel flusso usando il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="7559d-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="7559d-128">Il nome dell'evento deve essere quello definito nell'elemento **Event** nella playlist.</span><span class="sxs-lookup"><span data-stu-id="7559d-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="7559d-129">Quando Windows Media Player riceve un comando di script OPENEVENT dal codificatore, Cerca l'elemento **Event** nella playlist e avvia il buffering della clip o del flusso definito nell'elemento **Event** .</span><span class="sxs-lookup"><span data-stu-id="7559d-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="7559d-130">Windows Media Player quindi queste informazioni fino all'evento effettivo con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="7559d-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="7559d-131">Quando viene ricevuto l'evento denominato, Windows Media Player passa a tale contenuto precedentemente memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="7559d-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="7559d-132">Non è possibile usare caratteri Unicode per il comando script OPENEVENT nel file multimediale o nell'elemento **Event** nella playlist.</span><span class="sxs-lookup"><span data-stu-id="7559d-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7559d-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7559d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7559d-134">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="7559d-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7559d-135">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="7559d-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7559d-136">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="7559d-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="7559d-137">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="7559d-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7559d-138">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7559d-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7559d-139">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7559d-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




