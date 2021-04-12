---
title: Accesso alla libreria a livello di codice
description: Accesso alla libreria a livello di codice
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Library, accesso a livello di codice
- libreria, accesso
- accesso a Windows Media Player Library a livello di codice
- Libreria di Media Player Windows, aggiunta di elementi multimediali
- libreria, aggiunta di elementi multimediali
- Libreria Media Player di Windows, recupero di elementi multimediali
- raccolta, recupero di elementi multimediali
- Libreria Media Player di Windows, rimozione di elementi multimediali
- libreria, rimozione di elementi multimediali
- Aggiunta di elementi multimediali a Windows Media Player Library
- recupero di elementi multimediali dalla libreria Media Player di Windows
- rimozione di elementi multimediali dalla libreria Media Player di Windows
- recupero di metadati
- Libreria Media Player di Windows, recupero di metadati da elementi multimediali
- raccolta, recupero di metadati da elementi multimediali
- metadati, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396391"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="00549-126">Accesso alla libreria a livello di codice</span><span class="sxs-lookup"><span data-stu-id="00549-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="00549-127">Nel codice la libreria è rappresentata dall'oggetto **mediacollection** (o dall'interfaccia **IWMPMediaCollection** ).</span><span class="sxs-lookup"><span data-stu-id="00549-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="00549-128">Gli elementi multimediali sono rappresentati come oggetti **multimediali** o dall'interfaccia **IWMPMedia** .</span><span class="sxs-lookup"><span data-stu-id="00549-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="00549-129">Gli elementi della playlist sono rappresentati come oggetti **playlist** (o dall'interfaccia **IWMPPlaylist** ).</span><span class="sxs-lookup"><span data-stu-id="00549-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="00549-130">Per semplicità, in questa sezione si faranno semplicemente riferimento ai nomi degli oggetti, quando possibile.</span><span class="sxs-lookup"><span data-stu-id="00549-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="00549-131">Utilizzando l'oggetto **mediacollection** , è possibile utilizzare gli elementi multimediali e le playlist.</span><span class="sxs-lookup"><span data-stu-id="00549-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="00549-132">La libreria espone anche l'oggetto **PlaylistCollection** (o l'interfaccia **IWMPPlaylistCollection** ), che fornisce alcune funzionalità specifiche per l'uso delle playlist.</span><span class="sxs-lookup"><span data-stu-id="00549-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="00549-133">Nella maggior parte dei casi, l'oggetto **mediacollection** fornirà le funzionalità necessarie, anche quando si lavora con le playlist.</span><span class="sxs-lookup"><span data-stu-id="00549-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="00549-134">Per ulteriori informazioni sull'utilizzo di elementi multimediali, vedere [gestione di elementi multimediali](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="00549-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="00549-135">Per altre informazioni sull'uso delle playlist, vedere [gestione delle playlist](managing-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="00549-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="00549-136">Aggiunta di elementi multimediali alla libreria</span><span class="sxs-lookup"><span data-stu-id="00549-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="00549-137">L'aggiunta di contenuti multimediali digitali alla libreria è semplice.</span><span class="sxs-lookup"><span data-stu-id="00549-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="00549-138">È sufficiente chiamare il metodo [mediacollection. Add](mediacollection-add.md) , specificando il percorso del file multimediale come argomento.</span><span class="sxs-lookup"><span data-stu-id="00549-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="00549-139">Recupero di elementi multimediali dalla libreria</span><span class="sxs-lookup"><span data-stu-id="00549-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="00549-140">Quando si recuperano elementi multimediali dalla libreria, ciò che viene effettivamente recuperato è una playlist.</span><span class="sxs-lookup"><span data-stu-id="00549-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="00549-141">Anche se si prevede di recuperare un solo elemento multimediale, si otterrà un oggetto **playlist** contenente un singolo elemento, che verrà associato all'indice zero.</span><span class="sxs-lookup"><span data-stu-id="00549-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="00549-142">Se ad esempio si desidera recuperare un oggetto **multimediale** che rappresenta il brano denominato "Jeanne", è possibile utilizzare il codice JScript seguente:</span><span class="sxs-lookup"><span data-stu-id="00549-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="00549-143">Il codice precedente recupera una playlist contenente tutti gli elementi multimediali il cui nome è "Jeanne".</span><span class="sxs-lookup"><span data-stu-id="00549-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="00549-144">Per questo esempio, si supponga che sia presente un solo brano con tale nome nella libreria. si noti che la libreria supporta più canzoni con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="00549-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="00549-145">Ciò significa che è possibile prevedere che il numero di elementi nella playlist recuperata sia uguale a uno e che l'elemento multimediale venga rappresentato dall'indice zero.</span><span class="sxs-lookup"><span data-stu-id="00549-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="00549-146">Il codice di esempio seguente continua l'esempio precedente per illustrare come recuperare l'elemento multimediale dalla playlist usando il metodo [playlist. Item](playlist-item.md) .</span><span class="sxs-lookup"><span data-stu-id="00549-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="00549-147">Per ulteriori informazioni sul recupero di elementi multimediali dalle playlist, vedere [playlist e elementi multimediali](playlists-and-media-items.md) nella [Guida al controllo del lettore](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="00549-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="00549-148">Recupero di metadati da un elemento multimediale</span><span class="sxs-lookup"><span data-stu-id="00549-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="00549-149">Dopo aver recuperato un oggetto **multimediale** , è possibile leggere i valori di attributo associati al contenuto.</span><span class="sxs-lookup"><span data-stu-id="00549-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="00549-150">Nel caso più semplice, si potrebbe semplicemente voler conoscere un solo valore, ad esempio il nome dell'artista che ha eseguito una traccia musicale. Nell'esempio JScript seguente viene illustrato come utilizzare il metodo [Media. GetItemInfo](media-getiteminfo.md) per recuperare il nome dell'artista dal supporto recuperato nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="00549-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="00549-151">Un elemento multimediale può avere molti attributi diversi e l'utilizzo dei metadati non è sempre semplice come il semplice caso illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="00549-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="00549-152">Alcuni attributi, ad esempio, possono contenere più valori o avere valori in più di una lingua.</span><span class="sxs-lookup"><span data-stu-id="00549-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="00549-153">Per ulteriori informazioni sull'utilizzo dei metadati, vedere [attributi elemento multimediale](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="00549-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="00549-154">Per ulteriori informazioni sui diversi attributi, sui relativi significati e sul supporto dei tipi di file, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="00549-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="00549-155">Rimozione di elementi multimediali dalla libreria</span><span class="sxs-lookup"><span data-stu-id="00549-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="00549-156">Anche la rimozione di contenuti multimediali digitali dalla libreria è semplice.</span><span class="sxs-lookup"><span data-stu-id="00549-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="00549-157">È sufficiente chiamare **mediacollection. Remove**, fornendo l'oggetto **multimediale** che rappresenta l'elemento come primo argomento e il valore **true** come secondo.</span><span class="sxs-lookup"><span data-stu-id="00549-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="00549-158">Nell'esempio di codice JScript seguente viene rimosso dalla libreria il file denominato Jeanne (recuperato nell'esempio precedente):</span><span class="sxs-lookup"><span data-stu-id="00549-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="00549-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00549-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00549-160">**Informazioni sulla libreria**</span><span class="sxs-lookup"><span data-stu-id="00549-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="00549-161">**Informazioni sugli oggetti Mediacollection e media**</span><span class="sxs-lookup"><span data-stu-id="00549-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="00549-162">**Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="00549-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="00549-163">**Utilizzo della libreria**</span><span class="sxs-lookup"><span data-stu-id="00549-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




