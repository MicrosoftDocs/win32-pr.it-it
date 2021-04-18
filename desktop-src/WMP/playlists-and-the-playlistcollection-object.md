---
title: Playlist e oggetto PlaylistCollection
description: Playlist e oggetto PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlists, oggetto PlaylistCollection
- playlist di metafile, oggetto PlaylistCollection
- Playlist del metafile di Windows Media, oggetto PlaylistCollection
- PlaylistCollection (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298005"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="2b072-114">Playlist e oggetto PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="2b072-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="2b072-115">L'oggetto **PlaylistCollection** consente di accedere alle playlist nella libreria e include metodi per la creazione di nuove playlist vuote e nuove playlist da Metafile.</span><span class="sxs-lookup"><span data-stu-id="2b072-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="2b072-116">Uso delle playlist esistenti</span><span class="sxs-lookup"><span data-stu-id="2b072-116">Working with Existing Playlists</span></span>

<span data-ttu-id="2b072-117">*PlaylistCollection*. **GetAll** e *PlaylistCollection*. i metodi **GetByName** restituiscono ciascuno un oggetto **PlaylistArray** , che può contenere più playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="2b072-118">*PlaylistCollection*. il metodo **GetAll** restituisce tutte le playlist presenti nella libreria.</span><span class="sxs-lookup"><span data-stu-id="2b072-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="2b072-119">Ad esempio, è possibile chiamare questo metodo e recuperare le playlist nell'oggetto **PlaylistArray** per determinare se un determinato nome della playlist è già stato usato o per visualizzare tutte le playlist per l'utente.</span><span class="sxs-lookup"><span data-stu-id="2b072-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="2b072-120">Il codice di esempio negli [attributi della playlist](playlist-attributes.md) usa il metodo **GetAll** .</span><span class="sxs-lookup"><span data-stu-id="2b072-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="2b072-121">*PlaylistCollection*. il metodo **GetByName** restituisce tutte le playlist con un nome specificato.</span><span class="sxs-lookup"><span data-stu-id="2b072-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="2b072-122">È possibile usare questo metodo per gestire separatamente ogni playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="2b072-123">È anche possibile usare il metodo **GetByName** per recuperare una playlist univoca in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2b072-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="2b072-124">In tal caso, l'oggetto **PlaylistArray** ha un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="2b072-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="2b072-125">Nell'esempio C# riportato di seguito viene illustrata questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="2b072-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="2b072-126">Uso di nuove playlist</span><span class="sxs-lookup"><span data-stu-id="2b072-126">Working with New Playlists</span></span>

<span data-ttu-id="2b072-127">È possibile usare *PlaylistCollection*. metodo **nuova playlist** per creare una nuova playlist vuota.</span><span class="sxs-lookup"><span data-stu-id="2b072-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="2b072-128">Il metodo restituisce un riferimento al nuovo oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="2b072-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="2b072-129">È quindi possibile chiamare la *playlist*. metodo **appendItem** per aggiungere elementi multimediali alla playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="2b072-130">È anche possibile creare una nuova playlist basata su un metafile della playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="2b072-131">Per prima cosa, passare il nome della playlist e il percorso del metafile al *lettore*. metodo **nuova playlist** .</span><span class="sxs-lookup"><span data-stu-id="2b072-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="2b072-132">Tale metodo restituisce un riferimento al nuovo oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="2b072-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="2b072-133">Passare quindi il nuovo oggetto **playlist** a *PlaylistCollection*. metodo **importPlaylist** per aggiungerlo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2b072-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="2b072-134">Si noti la differenza tra *PlaylistCollection*. metodo **nuova playlist** e *lettore*. metodo **nuova playlist** .</span><span class="sxs-lookup"><span data-stu-id="2b072-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="2b072-135">Il metodo **PlaylistCollection** crea una nuova playlist vuota e la aggiunge alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2b072-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="2b072-136">Il metodo **Player** crea un nuovo oggetto **playlist** popolato ma non lo aggiunge alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2b072-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="2b072-137">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="2b072-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="2b072-138">Nell'esempio C# riportato di seguito viene illustrata l'importazione di una playlist da un metafile.</span><span class="sxs-lookup"><span data-stu-id="2b072-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="2b072-139">L'argomento *strPListName* specifica il nome della nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="2b072-140">*StrMetaFileName* specifica il nome del metafile da cui viene importata la playlist.</span><span class="sxs-lookup"><span data-stu-id="2b072-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="2b072-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b072-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b072-142">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="2b072-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="2b072-143">**Player. nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="2b072-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="2b072-144">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="2b072-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="2b072-145">**Oggetto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="2b072-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="2b072-146">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="2b072-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="2b072-147">**Playlist e elementi multimediali**</span><span class="sxs-lookup"><span data-stu-id="2b072-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




