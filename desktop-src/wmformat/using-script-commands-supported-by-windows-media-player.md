---
title: Uso di comandi script supportati da Windows Media Player
description: Uso di comandi script supportati da Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK, comandi script
- Windows Media Format SDK, Windows Media Player
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (formato avanzato dei sistemi), Windows Media Player
- script, comandi
- script, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044798"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="afbf8-112">Uso di comandi script supportati da Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="afbf8-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="afbf8-113">Windows Media Format SDK non fornisce supporto nativo per l'analisi e la risposta ai comandi di script.</span><span class="sxs-lookup"><span data-stu-id="afbf8-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="afbf8-114">È necessario includere qualsiasi logica relativa ai comandi di script nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afbf8-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="afbf8-115">Anche i tipi di script usati devono essere definiti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afbf8-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="afbf8-116">È possibile includere codice per gestire gli stessi comandi script supportati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="afbf8-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="afbf8-117">La gestione della compatibilità con Windows Media Player rende i file più universali che se si incorporano comandi script personalizzati.</span><span class="sxs-lookup"><span data-stu-id="afbf8-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="afbf8-118">Nella tabella seguente sono elencati i tipi di script supportati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="afbf8-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="afbf8-119">Tipo di script</span><span class="sxs-lookup"><span data-stu-id="afbf8-119">Script type</span></span> | <span data-ttu-id="afbf8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afbf8-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afbf8-121">URL</span><span class="sxs-lookup"><span data-stu-id="afbf8-121">URL</span></span>         | <span data-ttu-id="afbf8-122">Il lettore invia l'URL specificato al browser per la visualizzazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="afbf8-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="afbf8-123">Se viene usato un controllo Player incorporato, è possibile aggiungere un riferimento al frame specifico all'URL usando la sintassi &&*FrameName* .</span><span class="sxs-lookup"><span data-stu-id="afbf8-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="afbf8-124">FILENAME</span><span class="sxs-lookup"><span data-stu-id="afbf8-124">FILENAME</span></span>    | <span data-ttu-id="afbf8-125">URL di un altro file multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="afbf8-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="afbf8-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="afbf8-126">CAPTION</span></span>     | <span data-ttu-id="afbf8-127">Una stringa di testo visualizzata nell'area didascalie di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="afbf8-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="afbf8-128">Questo tipo supporta la formattazione HTML standard, quindi il testo può essere formattato nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="afbf8-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="afbf8-129">Un esempio di utilizzo è la didascalia closed.</span><span class="sxs-lookup"><span data-stu-id="afbf8-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="afbf8-130">EVENTO</span><span class="sxs-lookup"><span data-stu-id="afbf8-130">EVENT</span></span>       | <span data-ttu-id="afbf8-131">Nome di un evento che deve verificarsi.</span><span class="sxs-lookup"><span data-stu-id="afbf8-131">The name of an event that is to occur.</span></span> <span data-ttu-id="afbf8-132">Il tipo di evento supporta la personalizzazione per usi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="afbf8-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="afbf8-133">Il codice per l'evento specificato deve essere definito nel metafile di Windows Media per il flusso affinché il lettore esegua l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="afbf8-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="afbf8-134">Un esempio d'uso è l'inserimento di annunci.</span><span class="sxs-lookup"><span data-stu-id="afbf8-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="afbf8-135">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="afbf8-135">OPENEVENT</span></span>   | <span data-ttu-id="afbf8-136">Questo script precede l'evento effettivo.</span><span class="sxs-lookup"><span data-stu-id="afbf8-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="afbf8-137">Il OPENEVENT consente al lettore di pre-memorizzare il contenuto nel buffer in modo che, quando si verifica l'evento, il passaggio tra i flussi risulti trasparente.</span><span class="sxs-lookup"><span data-stu-id="afbf8-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="afbf8-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="afbf8-138">TEXT</span></span>        | <span data-ttu-id="afbf8-139">Una stringa di testo visualizzata nell'area didascalie di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="afbf8-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="afbf8-140">Può essere testo normale, SAMI o testo formattato HTML.</span><span class="sxs-lookup"><span data-stu-id="afbf8-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="afbf8-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afbf8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afbf8-142">**Uso di comandi script**</span><span class="sxs-lookup"><span data-stu-id="afbf8-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




