---
title: Controllo dell'esperienza di riproduzione
description: Controllo dell'esperienza di riproduzione
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Playlist Windows Media Metafile, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Playlist Windows Media Metafile, problemi di riproduzione
- playlist, problemi di riproduzione
- playlist di metafile, problemi di riproduzione
- controllo della riproduzione
- Windows Media Player, controllo della riproduzione
- Media Player di Windows, problemi di riproduzione
- HTMLView, problemi di riproduzione
- HTMLView, controllo della riproduzione
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298519"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="74618-114">Controllo dell'esperienza di riproduzione</span><span class="sxs-lookup"><span data-stu-id="74618-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="74618-115">In questa sezione vengono illustrati alcuni dei problemi di riproduzione che possono verificarsi quando si usa la funzionalità HTMLView.</span><span class="sxs-lookup"><span data-stu-id="74618-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="74618-116">Richiedere all'utente di visualizzare il contenuto basato sul Web</span><span class="sxs-lookup"><span data-stu-id="74618-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="74618-117">Si può decidere di consentire agli utenti di usare il contenuto multimediale digitale solo quando viene visualizzato anche il contenuto basato sul Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="74618-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="74618-118">È possibile includere codice di script nella pagina Web di HTMLView che interrompe la riproduzione del contenuto multimediale digitale se l'utente passa dalla funzionalità **ora in gioco** .</span><span class="sxs-lookup"><span data-stu-id="74618-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="74618-119">A tale scopo, è possibile specificare un gestore eventi per l'evento **unload** come parte dell'elemento **Body** , come illustrato nel codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="74618-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="74618-120">È quindi possibile includere il codice di script nella funzione del gestore eventi per chiudere il file nel lettore.</span><span class="sxs-lookup"><span data-stu-id="74618-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="74618-121">Il codice di esempio seguente esegue questa operazione:</span><span class="sxs-lookup"><span data-stu-id="74618-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="74618-122">Quando l'utente passa dall' **ora alla riproduzione** facendo clic su un pulsante per aprire un'altra funzionalità di Windows Media Player, ad esempio la libreria, il lettore chiude il browser incorporato.</span><span class="sxs-lookup"><span data-stu-id="74618-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="74618-123">In questo modo si verifica l'evento **OnUnload** , eseguendo lo script nella funzione denominata **UnloadMe**.</span><span class="sxs-lookup"><span data-stu-id="74618-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="74618-124">Il metodo [Player. Close](player-close.md) interrompe la riproduzione e Scarica il file multimediale digitale corrente.</span><span class="sxs-lookup"><span data-stu-id="74618-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="74618-125">Per visualizzare nuovamente il contenuto, è necessario che l'utente riapra il file. asx originale.</span><span class="sxs-lookup"><span data-stu-id="74618-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="74618-126">Questa tecnica interrompe anche la riproduzione quando l'utente si sposta dalla pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="74618-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="74618-127">Si noti che questa tecnica non può impedire all'utente di visualizzare il contenuto multimediale digitale quando passa alla modalità personalizzata.</span><span class="sxs-lookup"><span data-stu-id="74618-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="74618-128">Si ricorda che il parametro HTMLView può essere applicato a ogni elemento **entry** in un file con estensione asx.</span><span class="sxs-lookup"><span data-stu-id="74618-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="74618-129">È possibile sfruttare questa funzionalità per garantire che il contenuto di HTMLView venga visualizzato ogni volta che viene avviato un nuovo file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="74618-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="74618-130">A tale scopo, associare un elemento **param** per HtmlView a ogni voce della playlist. asx.</span><span class="sxs-lookup"><span data-stu-id="74618-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="74618-131">Quando ogni voce viene riprodotta, il lettore torna alla modalità Full e visualizza il contenuto HTMLView specificato nella playlist.</span><span class="sxs-lookup"><span data-stu-id="74618-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="74618-132">I tipi di comando per script di FILE e URL sono disabilitati per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="74618-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="74618-133">Windows Media Player 9 Series o versioni successive fornisce impostazioni che consentono all'utente di specificare se è possibile eseguire i comandi di script di tipo URL e FILE.</span><span class="sxs-lookup"><span data-stu-id="74618-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="74618-134">Per impostazione predefinita, entrambi i tipi di comando per script non vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="74618-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="74618-135">Se si usano tipi di comando per script personalizzati, continueranno a essere eseguiti, indipendentemente dall'impostazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74618-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="74618-136">Se è necessario usare i comandi di script di tipo FILE e URL, è necessario richiedere all'utente di modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="74618-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="74618-137">Per modificare le impostazioni, fare clic su **strumenti**, quindi su **Opzioni** e infine su **sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="74618-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="74618-138">La riapertura di un HTMLView non consente di ricaricare la pagina Web</span><span class="sxs-lookup"><span data-stu-id="74618-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="74618-139">Quando l'utente apre un file con estensione asx che include un parametro HTMLView e successivamente riapre lo stesso file, Windows Media Player non aggiorna la pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="74618-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="74618-140">Ciò significa anche che se gli utenti sono autorizzati a uscire dalla pagina Web di HTMLView, il lettore non restituisce il browser incorporato alla pagina Web HTMLView iniziale.</span><span class="sxs-lookup"><span data-stu-id="74618-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="74618-141">Nascondere il percorso del contenuto</span><span class="sxs-lookup"><span data-stu-id="74618-141">Hiding the content location</span></span>

<span data-ttu-id="74618-142">Si potrebbe decidere di non volere che Windows Media Player visualizzi il percorso del contenuto multimediale digitale mentre sta eseguendo un file con estensione asx.</span><span class="sxs-lookup"><span data-stu-id="74618-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="74618-143">In genere, Windows Media Player Visualizza solo le informazioni sulla playlist stessa quando si esegue lo streaming del contenuto da Internet.</span><span class="sxs-lookup"><span data-stu-id="74618-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="74618-144">Tuttavia, è possibile eseguire altri passaggi per impedire agli utenti di determinare la posizione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="74618-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="74618-145">Ad esempio, un modo per assicurarsi che il lettore non visualizzi il percorso del contenuto è quello di trasmettere il contenuto tramite playlist lato server di servizi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="74618-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="74618-146">In questo modo, quando l'utente visualizza le proprietà per il contenuto, vede l'URL del server e non l'URL del contenuto.</span><span class="sxs-lookup"><span data-stu-id="74618-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74618-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74618-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74618-148">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="74618-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="74618-149">**PARAM (elemento)**</span><span class="sxs-lookup"><span data-stu-id="74618-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




