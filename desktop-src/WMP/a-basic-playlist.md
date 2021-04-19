---
title: Una playlist di base
description: Una playlist di base
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Playlist Windows Media Metafile, esempio di playlist di base
- playlist, esempio di playlist di base
- playlist di metafile, esempio di playlist di base
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Windows Media Player, esempio di playlist di base
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314784"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="ff0b6-125">Una playlist di base</span><span class="sxs-lookup"><span data-stu-id="ff0b6-125">A Basic Playlist</span></span>

<span data-ttu-id="ff0b6-126">Nell'esempio di playlist seguente viene illustrato un set di base di elementi della playlist.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="ff0b6-127">Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="ff0b6-128">**Esempio di codice**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="ff0b6-129">La tabella seguente fornisce informazioni dettagliate sull'uso di ogni elemento nel codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="ff0b6-130">Linea</span><span class="sxs-lookup"><span data-stu-id="ff0b6-130">Line</span></span>                                                                                            | <span data-ttu-id="ff0b6-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff0b6-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="ff0b6-132">L'elemento [ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="ff0b6-133">L'attributo **Version** specifica il numero di versione degli elementi del metafile.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ff0b6-134">\<TITLE>Demo di base della playlist\</TITLE></span><span class="sxs-lookup"><span data-stu-id="ff0b6-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="ff0b6-135">L'elemento [title](title-element--metafile.md) identifica il titolo della playlist nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="ff0b6-136">Windows Media Player visualizza questi metadati come titolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="ff0b6-137">Inizia l'elemento [entry](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0b6-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="ff0b6-138">Un elemento **entry** è un modo per definire una clip specifica in una playlist</span><span class="sxs-lookup"><span data-stu-id="ff0b6-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ff0b6-139">\<TITLE>Una voce in una playlist di base\</TITLE></span><span class="sxs-lookup"><span data-stu-id="ff0b6-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="ff0b6-140">Identifica il titolo del clip della playlist.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="ff0b6-141">È diverso dall'elemento **title** precedente, perché questo è annidato all'interno di un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="ff0b6-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="ff0b6-142">Windows Media Player visualizza questi metadati come titolo della clip.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ff0b6-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="ff0b6-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="ff0b6-144">L'elemento [Author](author-element.md) identifica l'autore del clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="ff0b6-145">Windows Media Player visualizza questi metadati come **autore** della clip.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="ff0b6-146">Un commento.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-146">A comment.</span></span> <span data-ttu-id="ff0b6-147">I [Commenti](comments.md) sono visibili solo quando viene visualizzato il codice e si trovano nello stesso formato dei commenti **XML** .</span><span class="sxs-lookup"><span data-stu-id="ff0b6-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="ff0b6-148">Puntatore effettivo al file multimediale.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-148">Actual pointer to the media file.</span></span> <span data-ttu-id="ff0b6-149">L'elemento [ref](ref-element.md) identifica la riga come puntatore al contenuto multimediale, mentre l'attributo **href** è l'URL del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="ff0b6-150">In questo caso, l'URL utilizza il protocollo MMS, in modo che punti a un server Windows Media. I file multimediali nel server multimediale non vengono in genere conservati nello stesso percorso dei documenti HTML.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="ff0b6-151">Si noti l'uso della chiusura di tipo XML dell'elemento "/>" invece di " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="ff0b6-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="ff0b6-152">Poiché questo elemento non ha elementi figlio, si chiude.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="ff0b6-153">Specifica la fine dell'elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="ff0b6-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="ff0b6-154">Specifica la fine della playlist.</span><span class="sxs-lookup"><span data-stu-id="ff0b6-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="ff0b6-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff0b6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff0b6-156">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ff0b6-157">**Playlist di esempio**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="ff0b6-158">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ff0b6-159">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ff0b6-160">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ff0b6-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





