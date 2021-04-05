---
title: Uso delle playlist automatiche per organizzare il contenuto nella libreria
description: Uso delle playlist automatiche per organizzare il contenuto nella libreria
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online Stores, playlist automatiche
- archivi online, playlist automatiche
- digitare 1 archivi online, playlist automatiche
- digitare 2 archivi online, playlist automatiche
- Windows Media Player Online Store, organizzazione del contenuto della libreria
- negozi online, organizzazione del contenuto della libreria
- digitare 1 negozi online, organizzare il contenuto della libreria
- digitare 2 archivi online, organizzare il contenuto della libreria
- Windows Media Player Online Stores, organizzazione contenuto libreria
- negozi online, organizzazione del contenuto della libreria
- digitare 1 negozi online, organizzazione del contenuto della libreria
- digitare 2 negozi online, organizzazione del contenuto della libreria
- libreria, organizzazione del contenuto
- organizzazione del contenuto della libreria
- playlist automatiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515865"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="40b5e-118">Uso delle playlist automatiche per organizzare il contenuto nella libreria</span><span class="sxs-lookup"><span data-stu-id="40b5e-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="40b5e-119">È possibile usare playlist automatiche per organizzare il contenuto Premium fornito.</span><span class="sxs-lookup"><span data-stu-id="40b5e-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="40b5e-120">Ad esempio, è possibile usare Windows Media Player per creare una playlist automatica che contiene solo il contenuto fornito con una classificazione utente di almeno quattro stelle.</span><span class="sxs-lookup"><span data-stu-id="40b5e-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="40b5e-121">È quindi possibile aggiungere la playlist automatica alla libreria in Windows Media Player in modo che venga visualizzata nel nodo musica acquistato nel nodo del server di distribuzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="40b5e-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="40b5e-122">A questo scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="40b5e-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="40b5e-123">Creare la playlist automatica.</span><span class="sxs-lookup"><span data-stu-id="40b5e-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="40b5e-124">Utilizzando Esplora risorse, passare alla playlist automatica e recuperare il file con estensione WPL.</span><span class="sxs-lookup"><span data-stu-id="40b5e-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="40b5e-125">Usando il modello a oggetti di Windows Media Player, aggiungere la playlist automatica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="40b5e-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="40b5e-126">Impostare l'attributo **WM/contentdistributor** per la playlist sul nome della chiave del server di distribuzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="40b5e-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="40b5e-127">Impostare l'attributo **SyncOnly** per la playlist su true.</span><span class="sxs-lookup"><span data-stu-id="40b5e-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="40b5e-128">Il codice di esempio JScript seguente mostra una funzione che aggiunge una playlist automatica denominata "hit preferiti" al nodo Proseware nella libreria:</span><span class="sxs-lookup"><span data-stu-id="40b5e-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="40b5e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40b5e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b5e-130">Informazioni sull'integrazione della libreria</span><span class="sxs-lookup"><span data-stu-id="40b5e-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="40b5e-131">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="40b5e-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="40b5e-132">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="40b5e-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="40b5e-133">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="40b5e-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="40b5e-134">**Playlist statiche e automatiche**</span><span class="sxs-lookup"><span data-stu-id="40b5e-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="40b5e-135">**Attributo SyncOnly**</span><span class="sxs-lookup"><span data-stu-id="40b5e-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="40b5e-136">**Attributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="40b5e-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="40b5e-137">**Utilizzo della libreria**</span><span class="sxs-lookup"><span data-stu-id="40b5e-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




