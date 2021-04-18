---
title: Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray
description: Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, oggetto playlist
- Modello a oggetti di Windows Media Player, oggetto playlist
- modello a oggetti, oggetto playlist
- Controllo ActiveX Windows Media Player, oggetto playlist
- Controllo ActiveX, oggetto playlist
- Controllo ActiveX Windows Media Player Mobile, oggetto playlist
- Windows Media Player Mobile, oggetto playlist
- Oggetto playlist
- Windows Media Player, oggetto PlaylistCollection
- Modello a oggetti di Windows Media Player, oggetto PlaylistCollection
- modello a oggetti, oggetto PlaylistCollection
- Controllo ActiveX Windows Media Player, oggetto PlaylistCollection
- Controllo ActiveX, oggetto PlaylistCollection
- Controllo ActiveX Windows Media Player Mobile, oggetto PlaylistCollection
- Windows Media Player Mobile, oggetto PlaylistCollection
- PlaylistCollection (oggetto)
- Windows Media Player, oggetto PlaylistArray
- Modello a oggetti di Windows Media Player, oggetto PlaylistArray
- modello a oggetti, oggetto PlaylistArray
- Controllo ActiveX Windows Media Player, oggetto PlaylistArray
- Controllo ActiveX, oggetto PlaylistArray
- Controllo ActiveX Windows Media Player Mobile, oggetto PlaylistArray
- Windows Media Player Mobile, oggetto PlaylistArray
- Oggetto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298225"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="e1fff-127">Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="e1fff-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="e1fff-128">Gli oggetti playlist, **PlaylistCollection** e **PlaylistArray** governano le playlist che Windows Media Player può usare per specificare l'ordine in cui verrà riprodotto **il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="e1fff-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="e1fff-129">Si ottiene l'oggetto **PlaylistCollection** dalla proprietà **PlaylistCollection** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="e1fff-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="e1fff-130">La proprietà **PlaylistCollection** restituisce l'oggetto **PlaylistCollection** .</span><span class="sxs-lookup"><span data-stu-id="e1fff-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="e1fff-131">È possibile accedere alle proprietà dell'oggetto **PlaylistCollection** solo dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="e1fff-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="e1fff-132">Ad esempio, per creare una nuova playlist, è innanzitutto necessario ottenere l'oggetto **PlaylistCollection** e quindi usare un metodo su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="e1fff-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="e1fff-133">È possibile ottenere la playlist corrente usando la proprietà **currentPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="e1fff-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="e1fff-134">Per ottenere, ad esempio, il nome della playlist corrente, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e1fff-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="e1fff-135">L'oggetto **PlaylistArray** viene restituito dai metodi **GetAll** e **GetByName** dell'oggetto **PlaylistCollection** .</span><span class="sxs-lookup"><span data-stu-id="e1fff-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="e1fff-136">Per ottenere il numero di playlist, ad esempio, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e1fff-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="e1fff-137">Per recuperare una playlist nota in base al nome, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e1fff-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="e1fff-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1fff-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1fff-139">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="e1fff-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="e1fff-140">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="e1fff-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="e1fff-141">**Oggetto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="e1fff-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="e1fff-142">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="e1fff-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




