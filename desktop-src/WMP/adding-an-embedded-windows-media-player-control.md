---
title: Aggiunta di un controllo Media Player Windows incorporato
description: Aggiunta di un controllo Media Player Windows incorporato
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Playlist Windows Media Metafile, aggiunta di controlli Media Player Windows incorporati
- playlist, aggiunta di controlli Media Player Windows incorporati
- playlist di metafile, aggiunta di controlli Media Player Windows incorporati
- Playlist Windows Media Metafile, controlli Media Player Windows incorporati
- playlist, controlli Media Player incorporati di Windows
- playlist di metafile, controlli Media Player Windows incorporati
- Aggiunta di controlli Media Player Windows incorporati
- controlli Media Player incorporati di Windows
- Windows Media Player, aggiunta di controlli incorporati
- Windows Media Player, controlli incorporati
- HTMLView, aggiunta di controlli Media Player incorporati di Windows
- HTMLView, controlli Media Player incorporati di Windows
- HTMLView, modello a oggetti di Windows Media Player
- HTMLView, modello a oggetti del lettore
- Modello a oggetti di Windows Media Player, informazioni
- modello a oggetti, informazioni
- Oggetto Player
- Windows Media, modello a oggetti del lettore
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396387"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="3396c-121">Aggiunta di un controllo Media Player Windows incorporato</span><span class="sxs-lookup"><span data-stu-id="3396c-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="3396c-122">Esistono due motivi per cui è consigliabile aggiungere un'istanza incorporata di Windows Media Player alla presentazione di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="3396c-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="3396c-123">Prima di tutto, se si desidera visualizzare il contenuto video, è necessario utilizzare il controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3396c-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="3396c-124">In secondo luogo, se si desidera sfruttare le funzionalità del modello a oggetti di Windows Media Player dalla pagina Web di HTMLView, è necessario utilizzare un'istanza del controllo Player a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="3396c-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="3396c-125">Uso del controllo Player per visualizzare il video nel contenuto di HTMLView</span><span class="sxs-lookup"><span data-stu-id="3396c-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="3396c-126">In genere, Windows Media Player Visualizza i video usando il riquadro video e visualizzazione della funzionalità **Now Playing** .</span><span class="sxs-lookup"><span data-stu-id="3396c-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="3396c-127">Poiché HTMLView usa quest'area per visualizzare la pagina Web, è necessario fornire un'area di visualizzazione video aggiuntiva se si vuole che il lettore riproduca video.</span><span class="sxs-lookup"><span data-stu-id="3396c-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="3396c-128">Questa operazione è facile da eseguire tramite il controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3396c-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="3396c-129">Per usare il controllo Player per visualizzare video, incorporare il controllo nella pagina Web HTMLView usando il tag **Object** .</span><span class="sxs-lookup"><span data-stu-id="3396c-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="3396c-130">Si tratta della stessa tecnica usata per incorporare il controllo Player in una pagina Web in cui si vuole visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="3396c-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="3396c-131">Nell'esempio di codice seguente viene illustrata la sintassi di base per incorporare il controllo Player in Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="3396c-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="3396c-132">Il parametro *autostart* garantisce che il contenuto venga riprodotto automaticamente ogni volta che viene specificato un nuovo URL.</span><span class="sxs-lookup"><span data-stu-id="3396c-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="3396c-133">Il valore specificato per *uiMode* dipende dall'utente, ma in genere si vuole specificare "None" durante la creazione di contenuto per le presentazioni di htmlview.</span><span class="sxs-lookup"><span data-stu-id="3396c-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="3396c-134">Quando si incorpora il controllo Media Player Windows per visualizzare i video in questo modo, l'utente può controllare la riproduzione usando i controlli del lettore in modalità completa, pertanto non è necessario fornire controlli di trasporto aggiuntivi nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3396c-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="3396c-135">È possibile utilizzare lo spazio che in genere si alloca per i controlli di trasporto per visualizzare più testo, elementi grafici o collegamenti ad altro contenuto.</span><span class="sxs-lookup"><span data-stu-id="3396c-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="3396c-136">Non specificare un parametro *URL* quando si incorpora il controllo Media Player Windows in una pagina Web progettata per la visualizzazione in una presentazione htmlview.</span><span class="sxs-lookup"><span data-stu-id="3396c-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="3396c-137">Specificare invece i file multimediali digitali nel file con estensione asx che consente di aprire il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3396c-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="3396c-138">Dato che l'area di visualizzazione video è disponibile nella pagina Web di HTMLView, è possibile decidere dove posizionare il video e la dimensione desiderata per l'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3396c-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="3396c-139">Ad esempio, è possibile contenere l'oggetto **Player** all'interno di un elemento HTML **div** , quindi specificare la posizione in cui il **div** deve collocare la visualizzazione video nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3396c-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="3396c-140">È possibile modificare le dimensioni della visualizzazione video specificando i valori per gli attributi Height e Width dell'elemento **Object** .</span><span class="sxs-lookup"><span data-stu-id="3396c-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="3396c-141">È anche possibile specificare questi valori usando il codice di script.</span><span class="sxs-lookup"><span data-stu-id="3396c-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="3396c-142">Uso del modello a oggetti del lettore</span><span class="sxs-lookup"><span data-stu-id="3396c-142">Using the Player object model</span></span>

<span data-ttu-id="3396c-143">Il modello a oggetti di Windows Media Player espone proprietà, metodi ed eventi che è possibile usare nelle pagine Web di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="3396c-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="3396c-144">Quando si incorpora il controllo ActiveX di Windows Media Player nella pagina Web di HTMLView, è possibile accedere automaticamente al modello a oggetti del lettore.</span><span class="sxs-lookup"><span data-stu-id="3396c-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="3396c-145">Se si incorpora il controllo Windows Media Player nella pagina Web di HTMLView, non usare il modello a oggetti del lettore per specificare il file multimediale digitale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="3396c-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="3396c-146">Se, ad esempio, si usa codice script per specificare un valore per la proprietà **URL** del controllo incorporato, la pagina Web HtmlView verrà scaricata dalla funzionalità **Now Playing** durante la riproduzione del file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="3396c-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="3396c-147">Per evitare che ciò accada, aprire sempre i file con estensione asx che includono i parametri HTMLView quando è necessario usare lo script per aprire il contenuto multimediale digitale dalla pagina Web di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="3396c-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3396c-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3396c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3396c-149">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="3396c-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="3396c-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="3396c-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="3396c-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="3396c-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="3396c-152">**Impostazioni. avvio automatico**</span><span class="sxs-lookup"><span data-stu-id="3396c-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




