---
title: Informazioni sugli oggetti Mediacollection e media
description: Informazioni sugli oggetti Mediacollection e media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, oggetto Mediacollection
- Modello a oggetti di Windows Media Player, oggetto Mediacollection
- modello a oggetti, oggetto Mediacollection
- Controllo ActiveX Windows Media Player, oggetto Mediacollection
- Controllo ActiveX, oggetto Mediacollection
- Controllo ActiveX Windows Media Player Mobile, oggetto Mediacollection
- Windows Media Player Mobile, oggetto Mediacollection
- Mediacollection (oggetto)
- Windows Media Player, oggetto multimediale
- Modello a oggetti di Windows Media Player, oggetto multimediale
- modello a oggetti, oggetto multimediale
- Controllo ActiveX Windows Media Player, oggetto multimediale
- Controllo ActiveX, oggetto multimediale
- Controllo ActiveX Windows Media Player Mobile, oggetto multimediale
- Windows Media Player Mobile, oggetto multimediale
- Oggetto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298590"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="794ba-119">Informazioni sugli oggetti Mediacollection e media</span><span class="sxs-lookup"><span data-stu-id="794ba-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="794ba-120">**Mediacollection** e gli oggetti **multimediali** regolano la raccolta di supporti, che definisce le posizioni dei file multimediali digitali a cui può accedere Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="794ba-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="794ba-121">Si ottiene l'oggetto **mediacollection** dalla proprietà **mediacollection** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="794ba-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="794ba-122">La proprietà **mediacollection** restituisce l'oggetto **mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="794ba-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="794ba-123">È possibile accedere alle proprietà dell'oggetto **mediacollection** solo dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="794ba-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="794ba-124">Ad esempio, per aggiungere un oggetto **multimediale** (un brano), usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="794ba-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="794ba-125">Il file Laure. WMA è stato aggiunto alla raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="794ba-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="794ba-126">È possibile ottenere l'oggetto **multimediale** corrente usando la proprietà **currentMedia** del **lettore**.</span><span class="sxs-lookup"><span data-stu-id="794ba-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="794ba-127">Questo codice, ad esempio, ottiene la proprietà **Duration** dell'oggetto **multimediale** corrente:</span><span class="sxs-lookup"><span data-stu-id="794ba-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="794ba-128">Esistono diversi modi per ottenere un oggetto **multimediale** per poter accedere alle relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="794ba-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="794ba-129">Se ad esempio si vuole accedere alla proprietà **Duration** del supporto corrente, è possibile usare ognuna delle righe di codice seguenti.</span><span class="sxs-lookup"><span data-stu-id="794ba-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="794ba-130">Per ottenere la durata del supporto attualmente in riproduzione:</span><span class="sxs-lookup"><span data-stu-id="794ba-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="794ba-131">Per ottenere la durata del supporto corrente in una playlist:</span><span class="sxs-lookup"><span data-stu-id="794ba-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="794ba-132">Per ottenere la durata del terzo elemento multimediale in una playlist:</span><span class="sxs-lookup"><span data-stu-id="794ba-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="794ba-133">Per ottenere la durata del terzo elemento multimediale in un genere "Jazz":</span><span class="sxs-lookup"><span data-stu-id="794ba-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="794ba-134">Per ottenere la durata del terzo elemento multimediale nella seconda playlist:</span><span class="sxs-lookup"><span data-stu-id="794ba-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="794ba-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="794ba-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="794ba-136">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="794ba-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="794ba-137">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="794ba-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="794ba-138">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="794ba-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




