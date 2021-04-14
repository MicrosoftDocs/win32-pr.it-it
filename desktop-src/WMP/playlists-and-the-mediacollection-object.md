---
title: Playlist e oggetto Mediacollection
description: Playlist e oggetto Mediacollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, oggetto Mediacollection
- playlist di metafile, oggetto Mediacollection
- Playlist di Windows Media Metafile, oggetto Mediacollection
- Mediacollection (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395662"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="44e87-114">Playlist e oggetto Mediacollection</span><span class="sxs-lookup"><span data-stu-id="44e87-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="44e87-115">L'oggetto **mediacollection** consente di accedere a un'ampia gamma di playlist speciali e include un metodo per la creazione di una nuova playlist da un metafile.</span><span class="sxs-lookup"><span data-stu-id="44e87-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="44e87-116">I metodi seguenti recuperano playlist speciali:</span><span class="sxs-lookup"><span data-stu-id="44e87-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="44e87-117">**getAll**</span><span class="sxs-lookup"><span data-stu-id="44e87-117">**getAll**</span></span>
-   <span data-ttu-id="44e87-118">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="44e87-118">**getByAlbum**</span></span>
-   <span data-ttu-id="44e87-119">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="44e87-119">**getByAttribute**</span></span>
-   <span data-ttu-id="44e87-120">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="44e87-120">**getByAuthor**</span></span>
-   <span data-ttu-id="44e87-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="44e87-121">**getByGenre**</span></span>
-   <span data-ttu-id="44e87-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="44e87-122">**getByName**</span></span>

<span data-ttu-id="44e87-123">Come suggerisce il nome, questi metodi recuperano le playlist che contengono tutti gli elementi multimediali nella libreria che corrispondono a determinati criteri.</span><span class="sxs-lookup"><span data-stu-id="44e87-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="44e87-124">Prestare attenzione a non confondere l'elemento *mediacollection*. metodo **GetByName** con *PlaylistCollection*. metodo **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="44e87-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="44e87-125">Il metodo **mediacollection** restituisce un oggetto **playlist** contenente tutti gli elementi multimediali con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="44e87-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="44e87-126">Il metodo **PlaylistCollection** restituisce un oggetto **PlaylistArray** contenente tutte le playlist con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="44e87-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="44e87-127">È possibile usare *mediacollection*. **aggiungere** un metodo per aggiungere playlist e elementi multimediali alla libreria.</span><span class="sxs-lookup"><span data-stu-id="44e87-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="44e87-128">Per aggiungere una playlist, passare il metodo al percorso del metafile che definisce la playlist.</span><span class="sxs-lookup"><span data-stu-id="44e87-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="44e87-129">Il metodo restituisce sempre un oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="44e87-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="44e87-130">Non è possibile eseguire il cast tra oggetti **supporto** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="44e87-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="44e87-131">Per usare la playlist aggiunta, recuperare l'oggetto **playlist** con lo stesso nome dell'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="44e87-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="44e87-132">Nell'esempio C# riportato di seguito viene illustrato come recuperare i supporti per tipo utilizzando **mediacollection**. metodo **getByAttribute** .</span><span class="sxs-lookup"><span data-stu-id="44e87-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="44e87-133">Questo codice recupera i nomi di tutti gli attributi associati a un tipo specificato, nonché lo stato di lettura/scrittura o di sola lettura di tali attributi.</span><span class="sxs-lookup"><span data-stu-id="44e87-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="44e87-134">Genera un singolo file che contiene elenchi di attributi per i tipi audio, video, Radio, playlist, other, Music e Photo.</span><span class="sxs-lookup"><span data-stu-id="44e87-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="44e87-135">Nell'esempio C# riportato di seguito viene illustrato come aggiungere una playlist da un metafile alla libreria.</span><span class="sxs-lookup"><span data-stu-id="44e87-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="44e87-136">Le playlist statiche includono elementi multimediali specifici.</span><span class="sxs-lookup"><span data-stu-id="44e87-136">Static playlists include specific media items.</span></span> <span data-ttu-id="44e87-137">Le playlist automatiche eseguono ricerche nella libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi.</span><span class="sxs-lookup"><span data-stu-id="44e87-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="44e87-138">È possibile aggiungere playlist statiche e automatiche alla libreria usando *mediacollection*. **aggiungere** il metodo.</span><span class="sxs-lookup"><span data-stu-id="44e87-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="44e87-139">È anche possibile aggiungere playlist statiche usando *PlaylistCollection*. metodo **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="44e87-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44e87-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44e87-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44e87-141">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="44e87-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="44e87-142">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="44e87-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="44e87-143">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="44e87-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="44e87-144">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="44e87-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="44e87-145">**Playlist e oggetto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="44e87-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="44e87-146">**Playlist statiche e automatiche**</span><span class="sxs-lookup"><span data-stu-id="44e87-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




