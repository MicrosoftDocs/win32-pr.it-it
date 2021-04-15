---
title: Playlist statiche e automatiche
description: Playlist statiche e automatiche
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, statiche
- playlist di metafile, statiche
- Playlist Windows Media Metafile, statiche
- playlist statiche
- playlist automatiche
- playlist, auto
- playlist di metafile, auto
- Playlist Windows Media Metafile, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395474"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="3f2b5-118">Playlist statiche e automatiche</span><span class="sxs-lookup"><span data-stu-id="3f2b5-118">Static and Auto Playlists</span></span>

<span data-ttu-id="3f2b5-119">Sono disponibili due tipi di playlist:</span><span class="sxs-lookup"><span data-stu-id="3f2b5-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="3f2b5-120">Playlist statiche, che includono elementi multimediali specifici</span><span class="sxs-lookup"><span data-stu-id="3f2b5-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="3f2b5-121">Playlist automatiche, che eseguono ricerche nella libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="3f2b5-122">Una playlist automatica è il risultato di una query di database.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="3f2b5-123">Per importare una playlist statica da un metafile, chiamare prima il *lettore*. **nuova playlist** per creare un oggetto **playlist** basato sui dati nel metafile, quindi passare l'oggetto a *PlaylistCollection*. **importPlaylist** aggiungere la playlist alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="3f2b5-124">Per importare una playlist automatica da un metafile, usare *mediacollection*. **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="3f2b5-125">Per ulteriori informazioni, vedere [playlist e l'oggetto mediacollection](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="3f2b5-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="3f2b5-126">Per importare una playlist statica da un metafile di playlist automatico, usare *Player*. **nuova playlist** e *PlaylistCollection*. **importPlaylist** come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="3f2b5-127">La playlist automatica verrà eseguita una volta e una playlist statica verrà creata in base al risultato di tale esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="3f2b5-128">L'uso di una playlist automatica per eseguire query sulla libreria dell'utente non è supportato per le pagine Web a cui gli utenti accedono tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="3f2b5-129">Il codice di esempio C# seguente illustra l'importazione di un metafile di playlist automatico come playlist statica.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="3f2b5-130">Per eseguire questo esempio, creare una playlist automatica usando l'interfaccia utente della libreria e quindi includere il percorso corretto per il metafile della playlist automatica in questo codice.</span><span class="sxs-lookup"><span data-stu-id="3f2b5-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="3f2b5-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f2b5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f2b5-132">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="3f2b5-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




