---
title: Elemento EVENT (WMP SDK)
description: L'elemento EVENT definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script contrassegnato come un evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Finestra degli elementi evento Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324992"
---
# <a name="event-element"></a><span data-ttu-id="93331-104">Elemento EVENT</span><span class="sxs-lookup"><span data-stu-id="93331-104">EVENT Element</span></span>

<span data-ttu-id="93331-105">L'elemento **Event** definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script contrassegnato come un evento.</span><span class="sxs-lookup"><span data-stu-id="93331-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="93331-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="93331-106">Attributes</span></span>

<span data-ttu-id="93331-107">**Nome** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="93331-107">**NAME** (required)</span></span>

<span data-ttu-id="93331-108">Nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="93331-108">The name of the event.</span></span>

<span data-ttu-id="93331-109">**WHENDONE** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="93331-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="93331-110">Valore che definisce la funzione di Windows Media Player dopo la riproduzione del contenuto A cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="93331-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="93331-111">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="93331-111">The following values are possible.</span></span>



| <span data-ttu-id="93331-112">Valore</span><span class="sxs-lookup"><span data-stu-id="93331-112">Value</span></span>  | <span data-ttu-id="93331-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93331-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93331-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="93331-114">RESUME</span></span> | <span data-ttu-id="93331-115">La voce corrente (il clip interrotto dall'evento) riprende la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="93331-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="93331-116">Se il contenuto è archiviato, riprende nello stesso punto in cui è stato interrotto; Se il contenuto è trasmesso, riprende nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="93331-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="93331-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="93331-117">NEXT</span></span>   | <span data-ttu-id="93331-118">L'elemento **entry** successivo viene riprodotto come se l'evento non si fosse verificato e Windows Media Player avesse raggiunto la fine della clip corrente.</span><span class="sxs-lookup"><span data-stu-id="93331-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="93331-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="93331-119">BREAK</span></span>  | <span data-ttu-id="93331-120">Se la voce corrente si trova all'interno di un ciclo di **ripetizione** , il ciclo termina come se il numero di ripetizioni fosse stato completato.</span><span class="sxs-lookup"><span data-stu-id="93331-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="93331-121">In caso contrario, Windows Media Player passa alla fine della playlist come se la voce finale fosse stata completata come di consueto.</span><span class="sxs-lookup"><span data-stu-id="93331-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="93331-122">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="93331-122">Parent/Child Elements</span></span>



| <span data-ttu-id="93331-123">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="93331-123">Hierarchy</span></span>       | <span data-ttu-id="93331-124">Elementi</span><span class="sxs-lookup"><span data-stu-id="93331-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="93331-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="93331-125">Parent elements</span></span> | <span data-ttu-id="93331-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="93331-126">**ASX**</span></span>                 |
| <span data-ttu-id="93331-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="93331-127">Child elements</span></span>  | <span data-ttu-id="93331-128">**voce**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="93331-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="93331-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="93331-129">Remarks</span></span>

<span data-ttu-id="93331-130">Questo elemento definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script etichettato come un evento.</span><span class="sxs-lookup"><span data-stu-id="93331-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="93331-131">Un evento è un particolare tipo di comando script incorporato in un flusso inviato a Windows Media Player costituito da una stringa doppia.</span><span class="sxs-lookup"><span data-stu-id="93331-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="93331-132">La prima stringa è la parola "Event" e la seconda stringa è il nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="93331-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="93331-133">Il nome dell'evento nella seconda stringa deve corrispondere al nome dell'evento definito nel metafile.</span><span class="sxs-lookup"><span data-stu-id="93331-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="93331-134">La corrispondenza non fa distinzione tra maiuscole e minuscole. Gli eventi possono essere inviati a Windows Media Player la ricezione di un flusso in tempo reale oppure possono essere salvati in un file. ASF,. WMA o. WMV che viene recapitato come flusso unicast su richiesta.</span><span class="sxs-lookup"><span data-stu-id="93331-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="93331-135">Quando Windows Media Player riceve il comando script, elabora l'evento come definito dall'elemento **Event** .</span><span class="sxs-lookup"><span data-stu-id="93331-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="93331-136">Questo elemento definisce un ambito di elementi **entry** o **ENTRYREF** elaborati ogni volta che Windows Media Player riceve il comando script con l'evento denominato.</span><span class="sxs-lookup"><span data-stu-id="93331-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="93331-137">**ENTRYREF** può essere un URL che punta a una pagina ASP.</span><span class="sxs-lookup"><span data-stu-id="93331-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="93331-138">Con questo elemento, è possibile specificare un comportamento per il cambio di flusso quasi in tempo reale, anziché le modifiche di flusso PreCreate usando riferimenti ad altre parti di contenuto o metafile di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93331-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="93331-139">Quando si usano le pagine ASP per generare playlist, è necessario specificare un valore per la *risposta*. Proprietà **ContentType** e la *risposta*. **scade** la proprietà nella pagina ASP a causa di problemi di latenza con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="93331-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="93331-140">*Risposta*. **ContentType** deve essere un'estensione di nome di file valida per i file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93331-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="93331-141">I tipi validi includono. ASF,. asx,. WMA,. Wax,. WMV e. wvx.</span><span class="sxs-lookup"><span data-stu-id="93331-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="93331-142">Per informazioni dettagliate sull'uso dell'oggetto **Response** in ASP, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="93331-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="93331-143">Questo elemento può essere visualizzato in qualsiasi punto all'interno dell'elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="93331-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="93331-144">Se più elementi **evento** all'interno di un elemento **ASX** hanno valori identici per gli attributi del **nome** , Windows Media Player utilizza la prima occorrenza all'interno dell'elemento **ASX** e ignora tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="93331-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="93331-145">Quando gli elementi dell' **evento** hanno attributi di **nome** distinti, il relativo ordine nell'elemento **ASX** non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="93331-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="93331-146">Windows Media Player elimina gli eventi ricevuti durante l'elaborazione di un altro evento.</span><span class="sxs-lookup"><span data-stu-id="93331-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="93331-147">L'annidamento degli eventi non è supportato.</span><span class="sxs-lookup"><span data-stu-id="93331-147">Nesting of events is not supported.</span></span> <span data-ttu-id="93331-148">Quando Windows Media Player è in modalità di anteprima, il contenuto dell'evento non è vincolato dall'elemento **PREVIEWDURATION** . la lunghezza totale del contenuto di un evento può essere riprodotto anche se la durata dell'anteprima dell'elemento **voce** attivo scade prima della fine dell'evento.</span><span class="sxs-lookup"><span data-stu-id="93331-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="93331-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="93331-149">Examples</span></span>

<span data-ttu-id="93331-150">In questo esempio, quando Windows Media Player riceve l'evento del comando per script e la stringa di comando "AdLINK" nel supporto di streaming di cui viene eseguito il rendering, Cerca nella playlist un **eventoname** "AdLINK".</span><span class="sxs-lookup"><span data-stu-id="93331-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="93331-151">Windows Media Player passa dal flusso di cui viene eseguito il rendering e riproduce il contenuto a cui si fa riferimento nell' **evento**" https://example.microsoft.com/adlink.htm ".</span><span class="sxs-lookup"><span data-stu-id="93331-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="93331-152">L'attributo **entry** **CLIENTSKIP** è impostato su No per impedire che il clip dell' **evento** venga ignorato.</span><span class="sxs-lookup"><span data-stu-id="93331-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="93331-153">Deve essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="93331-153">It must be played.</span></span>

<span data-ttu-id="93331-154">Lo script `WHENDONE="RESUME"` indica a Windows Media Player di riprendere la riproduzione del supporto precedente passato da non appena AdLINK. ASF è terminato.</span><span class="sxs-lookup"><span data-stu-id="93331-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="93331-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93331-155">Requirements</span></span>



| <span data-ttu-id="93331-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="93331-156">Requirement</span></span> | <span data-ttu-id="93331-157">Valore</span><span class="sxs-lookup"><span data-stu-id="93331-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="93331-158">Versione</span><span class="sxs-lookup"><span data-stu-id="93331-158">Version</span></span><br/> | <span data-ttu-id="93331-159">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="93331-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93331-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93331-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93331-161">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="93331-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="93331-162">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="93331-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="93331-163">**Modello a oggetti di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="93331-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





