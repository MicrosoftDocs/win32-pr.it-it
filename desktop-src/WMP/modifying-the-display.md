---
title: Modifica della visualizzazione
description: Modifica della visualizzazione
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Playlist Windows Media Metafile, modifica delle visualizzazioni
- playlist, modifica di visualizzazioni
- playlist di metafile, modifica delle visualizzazioni
- Playlist Windows Media Metafile, visualizzazione modifiche
- playlist, visualizzazione delle modifiche
- playlist di metafile, visualizzazione della modifica
- Media Player di Windows, modifica della visualizzazione
- Media Player di Windows, modifica delle visualizzazioni
- Windows Media Player, proprietà testo
- Windows Media Player, proprietà immagine
- Windows Media Player, proprietà MOREINFO
- Media Player di Windows, testo astratto
- Proprietà di MOREINFO
- Testo astratto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044500"
---
# <a name="modifying-the-display"></a><span data-ttu-id="31dd5-117">Modifica della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="31dd5-117">Modifying the Display</span></span>

<span data-ttu-id="31dd5-118">Le playlist possono modificare l'interfaccia utente di Windows Media Player in quattro modi principali:</span><span class="sxs-lookup"><span data-stu-id="31dd5-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="31dd5-119">Proprietà testo</span><span class="sxs-lookup"><span data-stu-id="31dd5-119">Text properties</span></span>
-   <span data-ttu-id="31dd5-120">Proprietà dell'immagine</span><span class="sxs-lookup"><span data-stu-id="31dd5-120">Image properties</span></span>
-   <span data-ttu-id="31dd5-121">Proprietà di MOREINFO</span><span class="sxs-lookup"><span data-stu-id="31dd5-121">MOREINFO properties</span></span>
-   <span data-ttu-id="31dd5-122">Testo astratto</span><span class="sxs-lookup"><span data-stu-id="31dd5-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="31dd5-123">Proprietà testo</span><span class="sxs-lookup"><span data-stu-id="31dd5-123">Text properties</span></span>

<span data-ttu-id="31dd5-124">Windows Media Player consente la visualizzazione del testo dei metadati title, Author, copyright e Description.</span><span class="sxs-lookup"><span data-stu-id="31dd5-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="31dd5-125">I metadati della clip possono provenire dal flusso o dal file multimediale oppure possono provenire da una playlist.</span><span class="sxs-lookup"><span data-stu-id="31dd5-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="31dd5-126">Mostra i metadati provengono dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="31dd5-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="31dd5-127">In generale, le playlist rappresentano un metodo migliore per passare le proprietà di testo a Windows Media Player, soprattutto se è probabile che gli elementi di testo cambino.</span><span class="sxs-lookup"><span data-stu-id="31dd5-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="31dd5-128">È più semplice modificare il testo in una playlist anziché ricreare un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="31dd5-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="31dd5-129">Poiché le proprietà lette da una playlist eseguono l'override di quelle contenute nel file multimediale, è possibile aggiornare facilmente il testo visualizzato aggiungendo il nuovo testo alla proprietà corrispondente in una playlist.</span><span class="sxs-lookup"><span data-stu-id="31dd5-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="31dd5-130">Nell'esempio seguente, il testo dei metadati title e Author nella playlist sostituisce il titolo e il testo dell'autore contenuti nel file multimediale, Sample. WMA.</span><span class="sxs-lookup"><span data-stu-id="31dd5-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="31dd5-131">Il testo della **Descrizione** viene recuperato da un file Windows Media a cui si fa riferimento in un elemento **entry** a meno che non esista un elemento **astratto** in una playlist di metafile.</span><span class="sxs-lookup"><span data-stu-id="31dd5-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="31dd5-132">Se è presente un testo **astratto** , verrà visualizzato, sovrascrivendo il testo della **Descrizione** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="31dd5-133">Proprietà dell'immagine</span><span class="sxs-lookup"><span data-stu-id="31dd5-133">Image properties</span></span>

<span data-ttu-id="31dd5-134">Le immagini banner possono essere aggiunte all'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="31dd5-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="31dd5-135">Il grafico può essere usato per la pubblicità, fornire informazioni e fornire l'accesso ai siti Web, per citare alcune possibilità.</span><span class="sxs-lookup"><span data-stu-id="31dd5-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="31dd5-136">Usare l'elemento **banner** per specificare un'immagine grafica (32 pixel di altezza di 194 pixel di larghezza) per la visualizzazione da parte di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="31dd5-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="31dd5-137">Il grafico viene visualizzato sotto qualsiasi contenuto video.</span><span class="sxs-lookup"><span data-stu-id="31dd5-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="31dd5-138">È possibile aggiungere un collegamento ipertestuale al banner usando l'elemento figlio **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="31dd5-139">Una descrizione comando può essere definita da un elemento **astratto** all'interno dell'ambito dell'elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="31dd5-140">Qualsiasi testo della descrizione comando definito può essere visualizzato posizionando il puntatore del mouse sull'icona del banner.</span><span class="sxs-lookup"><span data-stu-id="31dd5-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="31dd5-141">Se si seleziona l'icona del banner con il puntatore del mouse, viene attivato qualsiasi collegamento ipertestuale definito con l'elemento **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="31dd5-142">Il formato grafico preferito del **banner** è il formato gif.</span><span class="sxs-lookup"><span data-stu-id="31dd5-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="31dd5-143">Il formato JPG può essere usato se il grafico è dimensionato correttamente.</span><span class="sxs-lookup"><span data-stu-id="31dd5-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="31dd5-144">Nell'esempio precedente viene illustrato l'utilizzo dell'elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="31dd5-145">Le immagini **banner** non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="31dd5-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="31dd5-146">Per ulteriori informazioni sui banner, vedere la pagina relativa [alla grafica personalizzata in Windows Media Player](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="31dd5-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="31dd5-147">Proprietà di MOREINFO</span><span class="sxs-lookup"><span data-stu-id="31dd5-147">MOREINFO properties</span></span>

<span data-ttu-id="31dd5-148">Le aree di testo e immagine dell'interfaccia utente possono essere associate agli URL.</span><span class="sxs-lookup"><span data-stu-id="31dd5-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="31dd5-149">Durante la riproduzione, gli utenti possono selezionare una di queste sezioni per connettersi all'URL associato nella Web browser.</span><span class="sxs-lookup"><span data-stu-id="31dd5-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="31dd5-150">Ad esempio, è possibile associare il sito Web di un inserzionista a un'immagine del banner pubblicitario, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="31dd5-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="31dd5-151">Testo astratto</span><span class="sxs-lookup"><span data-stu-id="31dd5-151">ABSTRACT text</span></span>

<span data-ttu-id="31dd5-152">Il testo **astratto** viene usato per visualizzare una breve descrizione popup delle aree di testo o immagine dell'interfaccia utente a cui è associata.</span><span class="sxs-lookup"><span data-stu-id="31dd5-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="31dd5-153">Durante la riproduzione, se il puntatore del mouse viene posizionato su una di queste aree, viene visualizzata una descrizione comando accanto al puntatore del mouse che Visualizza il testo **astratto** associato all'area.</span><span class="sxs-lookup"><span data-stu-id="31dd5-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="31dd5-154">Il testo **astratto** viene recuperato da un metafile e viene definito con l'elemento **abstract** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="31dd5-155">L'elemento **astratto** può essere un elemento figlio di una **voce** o di un elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="31dd5-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31dd5-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31dd5-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31dd5-157">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="31dd5-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="31dd5-158">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="31dd5-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="31dd5-159">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="31dd5-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="31dd5-160">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="31dd5-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




