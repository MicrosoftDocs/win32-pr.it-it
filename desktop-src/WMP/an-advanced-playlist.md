---
title: Una playlist avanzata
description: Una playlist avanzata
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Playlist Windows Media Metafile, esempio di playlist avanzato
- playlist, esempio di playlist avanzato
- playlist di metafile, esempio di playlist avanzato
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Esempio di Windows Media Player, playlist avanzata
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044504"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="9952e-125">Una playlist avanzata</span><span class="sxs-lookup"><span data-stu-id="9952e-125">An Advanced Playlist</span></span>

<span data-ttu-id="9952e-126">Nell'esempio di playlist seguente viene illustrato come usare un set più completo di elementi della playlist.</span><span class="sxs-lookup"><span data-stu-id="9952e-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="9952e-127">Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="9952e-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="9952e-128">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="9952e-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="9952e-129">La tabella seguente descrive la playlist avanzata precedente.</span><span class="sxs-lookup"><span data-stu-id="9952e-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="9952e-130">Linea</span><span class="sxs-lookup"><span data-stu-id="9952e-130">Line</span></span>                                                                                            | <span data-ttu-id="9952e-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9952e-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="9952e-132">L'elemento [ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="9952e-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="9952e-133">L'attributo **Version** specifica il numero di versione degli elementi del metafile.</span><span class="sxs-lookup"><span data-stu-id="9952e-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="9952e-134">L'elemento [title](title-element--metafile.md) identifica il titolo della playlist nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="9952e-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="9952e-135">Windows Media Player visualizza questi metadati come titolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9952e-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="9952e-136">L'elemento [astratto](abstract-element.md) fornisce la descrizione comando per il titolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9952e-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="9952e-137">L'elemento [moreinfo](moreinfo-element.md) collega il titolo show a un URL.</span><span class="sxs-lookup"><span data-stu-id="9952e-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="9952e-138">La sospensione del puntatore del mouse sul titolo Show accede alla descrizione comando, se definita.</span><span class="sxs-lookup"><span data-stu-id="9952e-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="9952e-139">Selezionando Mostra titolo verrà aperto l'URL designato.</span><span class="sxs-lookup"><span data-stu-id="9952e-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="9952e-140">L'elemento [banner](banner-element.md) crea un banner pubblicitario in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9952e-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="9952e-141">L'attributo **href** specifica l'icona del banner (che deve essere 194 pixel di larghezza per 32 pixel di altezza).</span><span class="sxs-lookup"><span data-stu-id="9952e-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="9952e-142">L'elemento [astratto](abstract-element.md) fornisce la descrizione comando per l' **intestazione**.</span><span class="sxs-lookup"><span data-stu-id="9952e-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="9952e-143">L'elemento [moreinfo](moreinfo-element.md) collega l'icona del **banner** a un URL.</span><span class="sxs-lookup"><span data-stu-id="9952e-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="9952e-144">Il puntatore del mouse sul **banner** accede a una descrizione comando, se definita.</span><span class="sxs-lookup"><span data-stu-id="9952e-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="9952e-145">Se si seleziona il **banner** , viene aperto l'URL designato.</span><span class="sxs-lookup"><span data-stu-id="9952e-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="9952e-146">L'elemento [param](param-element.md) definisce un parametro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9952e-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="9952e-147">L'attributo **Name** definisce il nome del parametro personalizzato come "Track".</span><span class="sxs-lookup"><span data-stu-id="9952e-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="9952e-148">L'attributo **value** definisce il valore di "Track" come "1".</span><span class="sxs-lookup"><span data-stu-id="9952e-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="9952e-149">Chiude l'elemento **banner**</span><span class="sxs-lookup"><span data-stu-id="9952e-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="9952e-150">Inizia il blocco dell'elemento [entry](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9952e-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="9952e-151">Questo elemento definisce una clip in una playlist specificando un collegamento nell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="9952e-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="9952e-152">Impostando **ClientSkip** su "No" si indica che l'utente non può eseguire rapidamente l'avanzamento o passare alla clip successiva</span><span class="sxs-lookup"><span data-stu-id="9952e-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="9952e-153">Crea un banner pubblicitario.</span><span class="sxs-lookup"><span data-stu-id="9952e-153">Creates an advertising banner.</span></span> <span data-ttu-id="9952e-154">**Href** è la rappresentazione grafica del banner (194x32 pixel).</span><span class="sxs-lookup"><span data-stu-id="9952e-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="9952e-155">Fornisce la descrizione comando per l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="9952e-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="9952e-156">Fornisce un collegamento all'URL per il banner.</span><span class="sxs-lookup"><span data-stu-id="9952e-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="9952e-157">La selezione del banner si connette all'URL.</span><span class="sxs-lookup"><span data-stu-id="9952e-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="9952e-158">Chiude l'elemento **banner**</span><span class="sxs-lookup"><span data-stu-id="9952e-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="9952e-159">Fornisce un collegamento all'URL per il testo del **titolo** della clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="9952e-160">Un commento.</span><span class="sxs-lookup"><span data-stu-id="9952e-160">A comment.</span></span> <span data-ttu-id="9952e-161">I [Commenti](comments.md) sono visibili solo quando viene visualizzato il codice.</span><span class="sxs-lookup"><span data-stu-id="9952e-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="9952e-162">Fornisce la descrizione comando per il testo del **titolo** della clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="9952e-163">Identifica il titolo della clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-163">Identifies the title of the clip.</span></span> <span data-ttu-id="9952e-164">Si tratta del **titolo** della clip perché è annidato all'interno di un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="9952e-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="9952e-165">Windows Media Player visualizza questi metadati come titolo della clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="9952e-166">Identifica l'autore del clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="9952e-167">Questi metadati vengono visualizzati come **autore** della clip da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9952e-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="9952e-168">L'elemento [Copyright](copyright-element.md) specifica i copyright associati al clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="9952e-169">Windows Media Player visualizza questi metadati come clip COPYRIGHT.</span><span class="sxs-lookup"><span data-stu-id="9952e-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="9952e-170">Commento, nello stesso formato dei commenti **XML** .</span><span class="sxs-lookup"><span data-stu-id="9952e-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="9952e-171">URL per il contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-171">URL for the media content.</span></span> <span data-ttu-id="9952e-172">L'elemento [ref](ref-element.md) identifica la riga come puntatore al contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="9952e-173">L'attributo **href** è l'URL del file. Si noti l'uso della chiusura di tipo XML dell'elemento "/>" invece di " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="9952e-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="9952e-174">Poiché questo elemento non ha elementi figlio, si chiude.</span><span class="sxs-lookup"><span data-stu-id="9952e-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="9952e-175">Specifica la fine dell'elemento del primo elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="9952e-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="9952e-176">Inizia il secondo elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="9952e-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="9952e-177">Identifica il titolo del secondo clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="9952e-178">Identifica l'autore del secondo clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="9952e-179">Un commento.</span><span class="sxs-lookup"><span data-stu-id="9952e-179">A comment.</span></span> <span data-ttu-id="9952e-180">Sarà visibile solo quando viene visualizzato il codice.</span><span class="sxs-lookup"><span data-stu-id="9952e-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="9952e-181">Testo della descrizione comando per il testo del **titolo** della clip.</span><span class="sxs-lookup"><span data-stu-id="9952e-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="9952e-182">Un commento.</span><span class="sxs-lookup"><span data-stu-id="9952e-182">A comment.</span></span> <span data-ttu-id="9952e-183">Sarà visibile solo quando viene visualizzato il codice.</span><span class="sxs-lookup"><span data-stu-id="9952e-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="9952e-184">Identifica la riga come puntatore al contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="9952e-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="9952e-185">L'attributo **href** è l'URL del file.</span><span class="sxs-lookup"><span data-stu-id="9952e-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="9952e-186">Specifica la fine del secondo elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="9952e-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="9952e-187">Specifica la fine della playlist.</span><span class="sxs-lookup"><span data-stu-id="9952e-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="9952e-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9952e-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9952e-189">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="9952e-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9952e-190">**Playlist di esempio**</span><span class="sxs-lookup"><span data-stu-id="9952e-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="9952e-191">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="9952e-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9952e-192">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9952e-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9952e-193">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9952e-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





