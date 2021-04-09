---
title: Playlist e elementi multimediali
description: Playlist e elementi multimediali
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, elementi multimediali
- playlist di metafile, elementi multimediali
- Playlist Windows Media Metafile, elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955325"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="e4d0a-113">Playlist e elementi multimediali</span><span class="sxs-lookup"><span data-stu-id="e4d0a-113">Playlists and Media Items</span></span>

<span data-ttu-id="e4d0a-114">Una playlist è un set di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-114">A playlist is a set of media items.</span></span> <span data-ttu-id="e4d0a-115">Un oggetto **playlist** può modificare gli oggetti **multimediali** che rappresentano tali elementi.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="e4d0a-116">Recupero di elementi multimediali</span><span class="sxs-lookup"><span data-stu-id="e4d0a-116">Retrieving Media Items</span></span>

<span data-ttu-id="e4d0a-117">Per una playlist esistente, è possibile leggere la *playlist*. proprietà **count** per determinare il numero di elementi multimediali presenti nella playlist ed è possibile ottenere un riferimento all'oggetto **multimediale** corrispondente a un elemento specifico usando la *playlist*. proprietà **Item** .</span><span class="sxs-lookup"><span data-stu-id="e4d0a-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="e4d0a-118">Nell'esempio C# seguente viene recuperato un riferimento a un oggetto in un elemento multimediale specifico.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="e4d0a-119">(In questo argomento, la variabile *plist* è un riferimento a un oggetto **playlist** ).</span><span class="sxs-lookup"><span data-stu-id="e4d0a-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="e4d0a-120">Nell'esempio C# seguente vengono recuperati i nomi di tutti gli elementi multimediali in una playlist e inseriti in una casella di riepilogo denominata lstOutput.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="e4d0a-121">Aggiunta di elementi a una playlist</span><span class="sxs-lookup"><span data-stu-id="e4d0a-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="e4d0a-122">È possibile aggiungere un elemento multimediale alla fine di una playlist o in una posizione specifica in una playlist, usando la *playlist*. **appendItem** e *playlist*. metodi **InsertItem** .</span><span class="sxs-lookup"><span data-stu-id="e4d0a-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="e4d0a-123">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e4d0a-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="e4d0a-124">Nell'esempio C# seguente vengono illustrate entrambe le tecniche aggiungendo l'elemento multimediale corrente a una playlist denominata "BluesTest", prima alla fine e quindi all'inizio della playlist.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="e4d0a-125">Quando si crea una nuova playlist vuota utilizzando *PlaylistCollection*. metodo **nuova playlist** , è possibile aggiungere elementi multimediali chiamando ripetutamente la *playlist*. metodo **appendItem** .</span><span class="sxs-lookup"><span data-stu-id="e4d0a-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="e4d0a-126">Manipolazione di elementi multimediali in una playlist</span><span class="sxs-lookup"><span data-stu-id="e4d0a-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="e4d0a-127">È possibile modificare la posizione di un elemento multimediale nella playlist usando la *playlist*. metodo **moveItem** .</span><span class="sxs-lookup"><span data-stu-id="e4d0a-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="e4d0a-128">L'elemento viene specificato in base al relativo indice corrente, quindi viene specificato il nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="e4d0a-129">L'esempio C# seguente sposta un elemento dall'indice 5 all'indice 0 all'interno di una playlist.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="e4d0a-130">È possibile rimuovere un elemento multimediale dalla playlist usando la **playlist**. metodo **RemoveItem** .</span><span class="sxs-lookup"><span data-stu-id="e4d0a-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="e4d0a-131">Si noti che se l'elemento rimosso non è l'elemento finale nella playlist, i valori di indice degli elementi successivi cambiano.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="e4d0a-132">Nell'esempio C# seguente viene rimosso l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="e4d0a-133">Gli utenti possono modificare il contenuto di una playlist all'esterno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="e4d0a-134">Ogni volta che si modificano gli elementi in una playlist, è necessario monitorare e gestire gli eventi correlati alla playlist del controllo Media Player Windows per verificare il corretto funzionamento del codice.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="e4d0a-135">Questi eventi sono *Player*. **CurrentPlaylistChange** e *Player*. **PlaylistChange**.</span><span class="sxs-lookup"><span data-stu-id="e4d0a-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e4d0a-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4d0a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4d0a-137">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="e4d0a-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="e4d0a-138">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="e4d0a-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e4d0a-139">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="e4d0a-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




