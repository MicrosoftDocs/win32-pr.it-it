---
title: Uso del cambio di flusso di eventi Live
description: Uso del cambio di flusso di eventi Live
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221136"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="35499-118">Uso del cambio di flusso di eventi Live</span><span class="sxs-lookup"><span data-stu-id="35499-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="35499-119">I flussi multimediali possono anche essere controllati dall'interazione dei comandi di script incorporati in un flusso multimediale con elementi metafile di Windows Media in una playlist di metafile.</span><span class="sxs-lookup"><span data-stu-id="35499-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="35499-120">Un evento è un particolare tipo di comando di script incorporato in un flusso multimediale o in un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="35499-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="35499-121">Quando il controllo Windows Media Player riceve il comando script, l'evento viene elaborato come definito dall'elemento **Event** nella playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="35499-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="35499-122">Windows Media Player passa dal flusso corrente in cui viene eseguito il rendering ed esegue il rendering del contenuto a cui si fa riferimento nell'elemento dell' **evento** della playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="35499-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="35499-123">L'elemento **Event** viene in genere usato nella produzione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="35499-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="35499-124">Un elemento **evento** è simile a un elemento **entry** , ma ogni gestisce la riproduzione di flussi e file multimediali in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="35499-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="35499-125">L'elemento **entry** viene usato per creare playlist.</span><span class="sxs-lookup"><span data-stu-id="35499-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="35499-126">Un flusso o un file multimediale a cui si fa riferimento in un elemento **entry** inizia la riproduzione quando il flusso o il file multimediale a cui viene fatto riferimento nella **voce** precedente termina.</span><span class="sxs-lookup"><span data-stu-id="35499-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="35499-127">Un flusso a cui viene fatto riferimento in un **evento** viene riprodotto solo quando viene ricevuto un comando di script specifico.</span><span class="sxs-lookup"><span data-stu-id="35499-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="35499-128">Ad esempio, quando Windows Media Player riceve un comando script con tipo stringa "EVENT" e la stringa di comando "AdLINK", Cerca nella playlist gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="35499-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="35499-129">Windows Media Player quindi passa dal flusso Live per riprodurre il flusso o il file multimediale contenuto nell' **evento**, in questo caso AdLINK. WMA.</span><span class="sxs-lookup"><span data-stu-id="35499-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="35499-130">Il codice `WHENDONE="RESUME"` indica a Windows Media Player di riprendere la riproduzione del flusso precedente al termine di AdLINK. WMA.</span><span class="sxs-lookup"><span data-stu-id="35499-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="35499-131">La mancata gestione di ogni evento incorporato in un flusso multimediale o in un file multimediale può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="35499-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="35499-132">Se si vuole usare il cambio di flusso di eventi live, è necessario includere un elemento **Event** nella playlist per gestire ogni comando di script degli eventi incorporato nei flussi multimediali o nei file multimediali della playlist.</span><span class="sxs-lookup"><span data-stu-id="35499-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="35499-133">Prima di creare la playlist, è necessario conoscere i dettagli relativi ai comandi di script incorporati nel contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="35499-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="35499-134">Se è presente un comando script di evento che si desidera ignorare con Windows Media Player, includere un elemento **Event** nella playlist per gestire l'evento, ma fare riferimento a un URL fittizio nel gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="35499-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="35499-135">Inserimento ad</span><span class="sxs-lookup"><span data-stu-id="35499-135">Ad Insertion</span></span>

<span data-ttu-id="35499-136">Questa tecnica può essere utilizzata per l'inserimento di annunci.</span><span class="sxs-lookup"><span data-stu-id="35499-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="35499-137">Ad esempio, durante una trasmissione Internet diretta di una partita a palla, è possibile inviare un comando all'inizio di ogni break pubblicitario che indica a ogni client (Windows Media Player) di riprodurre le pubblicità elencate nella propria playlist.</span><span class="sxs-lookup"><span data-stu-id="35499-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="35499-138">Quando i client terminano la riproduzione dei dati commerciali, la playlist indica a ogni client di tornare alla trasmissione live.</span><span class="sxs-lookup"><span data-stu-id="35499-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="35499-139">Il rendering del contenuto multimediale dell' **evento** verrà eseguito solo quando il supporto di streaming a cui si accede trasmette lo scripting incorporato con il nome dell' **evento** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="35499-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="35499-140">Le possibilità inerenti al cambio di **eventi** sono particolarmente apprezzate, a differenza del modo in cui gli annunci raggiungono i visualizzatori attraverso la trasmissione standard e in modalità wireless con il modo in cui gli annunci possono raggiungere i visualizzatori usando le tecnologie</span><span class="sxs-lookup"><span data-stu-id="35499-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="35499-141">In passato, gli annunci broadcast potevano essere indirizzati solo ai visualizzatori, usando i dati di classificazione come criterio primario.</span><span class="sxs-lookup"><span data-stu-id="35499-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="35499-142">Gli annunci inviati usando le tecnologie Windows Media possono essere indirizzati direttamente all'utente di destinazione perché **gli eventi** e le playlist possono essere creati in tempo reale in base all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35499-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="35499-143">Per altre informazioni, vedere [personalizzazione del recapito multimediale](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="35499-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="35499-144">È anche possibile usare le playlist di metafile per visualizzare grafica, audio e testo personalizzati per la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="35499-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="35499-145">È possibile usare l'elemento **banner** come elemento figlio di un **evento** per visualizzare un'immagine di messaggio pubblicitario.</span><span class="sxs-lookup"><span data-stu-id="35499-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="35499-146">L'elemento **banner** fornisce il percorso e il file che contiene la grafica per il banner pubblicitario.</span><span class="sxs-lookup"><span data-stu-id="35499-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="35499-147">È anche possibile fornire un collegamento a un sito o a un file usando l'elemento figlio **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="35499-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="35499-148">L'URL nell'elemento **moreinfo** può fornire un collegamento a un numero ancora maggiore di annunci sul Web.</span><span class="sxs-lookup"><span data-stu-id="35499-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="35499-149">Nell'esempio seguente viene illustrato l'utilizzo di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="35499-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="35499-150">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="35499-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="35499-151">L'esempio seguente inserisce il file annuncio. WMA nel flusso di trasmissione unicast broadcast quando un client riceve un **evento** del comando script con l'attributo **Name** impostato su "timeout".</span><span class="sxs-lookup"><span data-stu-id="35499-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="35499-152">**CLIENTSKIP** è impostato su No per impedire che l'annuncio trasmesso venga ignorato.</span><span class="sxs-lookup"><span data-stu-id="35499-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="35499-153">In questo esempio, il flusso di Active Directory deve essere riprodotto prima di tornare al flusso originale.</span><span class="sxs-lookup"><span data-stu-id="35499-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="35499-154">Al termine dell'annuncio, il client riprende la riproduzione del flusso originale.</span><span class="sxs-lookup"><span data-stu-id="35499-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="35499-155">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="35499-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="35499-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35499-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35499-157">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="35499-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="35499-158">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="35499-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="35499-159">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="35499-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="35499-160">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="35499-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




