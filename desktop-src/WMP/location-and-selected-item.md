---
title: Posizione e elemento selezionato
description: Posizione e elemento selezionato
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player Online Stores, località
- negozi online, località
- digitare 1 negozi online, località
- Windows Media Player Online Stores, percorsi di libreria
- archivi online, percorsi di libreria
- digitare 1 archivi online, percorsi di libreria
- Windows Media Player Online Stores, elementi selezionati
- archivi online, elementi selezionati
- digitare 1 archivi online, elementi selezionati
- Windows Media Player Library, posizioni
- Libreria Media Player di Windows, elementi selezionati
- libreria, località
- libreria, elementi selezionati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221343"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="5976a-116">Posizione e elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-116">Location and Selected Item</span></span>

<span data-ttu-id="5976a-117">Windows Media Player usa i cinque elementi seguenti per caratterizzare la visualizzazione corrente del contenuto del negozio online:</span><span class="sxs-lookup"><span data-stu-id="5976a-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="5976a-118">attività</span><span class="sxs-lookup"><span data-stu-id="5976a-118">task</span></span>
-   <span data-ttu-id="5976a-119">tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-119">library location type</span></span>
-   <span data-ttu-id="5976a-120">ID percorso libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-120">library location ID</span></span>
-   <span data-ttu-id="5976a-121">tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-121">selected item type</span></span>
-   <span data-ttu-id="5976a-122">ID elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-122">selected item ID</span></span>

<span data-ttu-id="5976a-123">In genere, è possibile considerare la vista in Windows Media Player come contenitore di elementi.</span><span class="sxs-lookup"><span data-stu-id="5976a-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="5976a-124">Il contenitore dispone di un tipo e un elemento ha un tipo.</span><span class="sxs-lookup"><span data-stu-id="5976a-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="5976a-125">Tutti gli elementi in un contenitore hanno lo stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="5976a-125">All the items in a container have the same type.</span></span> <span data-ttu-id="5976a-126">I tipi di percorso e i tipi di elemento sono entrambi specificati dalle [costanti del percorso della libreria](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5976a-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="5976a-127">Se, ad esempio, nella visualizzazione corrente viene visualizzato un singolo album, il tipo di percorso della libreria è CPAlbumID e, poiché un album contiene tracce, il tipo di elemento selezionato è CPTrackID.</span><span class="sxs-lookup"><span data-stu-id="5976a-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="5976a-128">La tabella seguente illustra il percorso e i tipi di elemento per diversi contenitori.</span><span class="sxs-lookup"><span data-stu-id="5976a-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="5976a-129">Descrizione del contenitore</span><span class="sxs-lookup"><span data-stu-id="5976a-129">Description of container</span></span>                              | <span data-ttu-id="5976a-130">Tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-130">Library location type</span></span> | <span data-ttu-id="5976a-131">Tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="5976a-132">Un album che è un contenitore di tracce</span><span class="sxs-lookup"><span data-stu-id="5976a-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="5976a-133">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="5976a-133">CPAlbumID</span></span>             | <span data-ttu-id="5976a-134">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="5976a-134">CPTrackID</span></span>          |
| <span data-ttu-id="5976a-135">Elenco che è un contenitore di tracce</span><span class="sxs-lookup"><span data-stu-id="5976a-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="5976a-136">CPListID</span><span class="sxs-lookup"><span data-stu-id="5976a-136">CPListID</span></span>              | <span data-ttu-id="5976a-137">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="5976a-137">CPTrackID</span></span>          |
| <span data-ttu-id="5976a-138">Elenco che è un contenitore di album</span><span class="sxs-lookup"><span data-stu-id="5976a-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="5976a-139">CPListID</span><span class="sxs-lookup"><span data-stu-id="5976a-139">CPListID</span></span>              | <span data-ttu-id="5976a-140">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="5976a-140">CPAlbumID</span></span>          |
| <span data-ttu-id="5976a-141">Una stazione di radio che è un contenitore di elenchi</span><span class="sxs-lookup"><span data-stu-id="5976a-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="5976a-142">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="5976a-142">CPRadioID</span></span>             | <span data-ttu-id="5976a-143">CPListID</span><span class="sxs-lookup"><span data-stu-id="5976a-143">CPListID</span></span>           |
| <span data-ttu-id="5976a-144">Il set di tutti gli album, che è un contenitore di album</span><span class="sxs-lookup"><span data-stu-id="5976a-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="5976a-145">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="5976a-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="5976a-146">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="5976a-146">CPAlbumID</span></span>          |
| <span data-ttu-id="5976a-147">Il set di tutti i generi, che è un contenitore di generi</span><span class="sxs-lookup"><span data-stu-id="5976a-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="5976a-148">AllCPGenreIDs</span><span class="sxs-lookup"><span data-stu-id="5976a-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="5976a-149">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="5976a-149">CPGenreID</span></span>          |



 

<span data-ttu-id="5976a-150">Le schede in Windows Media Player rappresentano attività diverse.</span><span class="sxs-lookup"><span data-stu-id="5976a-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="5976a-151">Il lettore Visualizza il contenuto dell'archivio online in tre riquadri attività diversi: **libreria**, **masterizzazione** e **sincronizzazione**. Il riquadro attività libreria è denominato anche riquadro attività **Sfoglia** .</span><span class="sxs-lookup"><span data-stu-id="5976a-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="5976a-152">In alcuni casi, un riquadro attività è denominato *funzionalità*, quindi è possibile che nella documentazione siano presenti termini come la funzionalità di *masterizzazione* e la funzionalità di *sincronizzazione* .</span><span class="sxs-lookup"><span data-stu-id="5976a-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="5976a-153">Gli esempi seguenti illustrano come Windows Media Player usa le cinque informazioni (attività, tipo di percorso della libreria, ID del percorso della libreria, tipo di elemento selezionato, ID elemento selezionato) per caratterizzare visualizzazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="5976a-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="5976a-154">Nel riquadro attività **Burn** , il lettore Visualizza un album come contenitore di tracce.</span><span class="sxs-lookup"><span data-stu-id="5976a-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="5976a-155">L'ID dell'album è 250.</span><span class="sxs-lookup"><span data-stu-id="5976a-155">The album has an ID of 250.</span></span> <span data-ttu-id="5976a-156">Nella visualizzazione l'elemento selezionato corrisponde alla traccia con ID 800.</span><span class="sxs-lookup"><span data-stu-id="5976a-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="5976a-157">Si noti che 800 è l'ID della traccia nel catalogo del negozio online, non il numero della traccia sull'album.</span><span class="sxs-lookup"><span data-stu-id="5976a-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="5976a-158">Elemento</span><span class="sxs-lookup"><span data-stu-id="5976a-158">Item</span></span>                  | <span data-ttu-id="5976a-159">valore</span><span class="sxs-lookup"><span data-stu-id="5976a-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="5976a-160">attività</span><span class="sxs-lookup"><span data-stu-id="5976a-160">task</span></span>                  | <span data-ttu-id="5976a-161">Bruciare</span><span class="sxs-lookup"><span data-stu-id="5976a-161">Burn</span></span>      |
| <span data-ttu-id="5976a-162">tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-162">library location type</span></span> | <span data-ttu-id="5976a-163">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="5976a-163">CPAlbumID</span></span> |
| <span data-ttu-id="5976a-164">ID percorso libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-164">library location ID</span></span>   | <span data-ttu-id="5976a-165">250</span><span class="sxs-lookup"><span data-stu-id="5976a-165">250</span></span>       |
| <span data-ttu-id="5976a-166">tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-166">selected item type</span></span>    | <span data-ttu-id="5976a-167">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="5976a-167">CPTrackID</span></span> |
| <span data-ttu-id="5976a-168">ID elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-168">selected item ID</span></span>      | <span data-ttu-id="5976a-169">800</span><span class="sxs-lookup"><span data-stu-id="5976a-169">800</span></span>       |



 

<span data-ttu-id="5976a-170">Nel riquadro attività di **sincronizzazione** , il lettore Visualizza il set di tutti gli album, che è un contenitore di album.</span><span class="sxs-lookup"><span data-stu-id="5976a-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="5976a-171">Nella visualizzazione, l'elemento selezionato è l'album con ID 300.</span><span class="sxs-lookup"><span data-stu-id="5976a-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="5976a-172">Si noti che l'ID del percorso della libreria non è applicabile a questa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5976a-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="5976a-173">Elemento</span><span class="sxs-lookup"><span data-stu-id="5976a-173">Item</span></span>                  | <span data-ttu-id="5976a-174">valore</span><span class="sxs-lookup"><span data-stu-id="5976a-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="5976a-175">attività</span><span class="sxs-lookup"><span data-stu-id="5976a-175">task</span></span>                  | <span data-ttu-id="5976a-176">Sincronizza</span><span class="sxs-lookup"><span data-stu-id="5976a-176">Sync</span></span>          |
| <span data-ttu-id="5976a-177">tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-177">library location type</span></span> | <span data-ttu-id="5976a-178">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="5976a-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="5976a-179">ID percorso libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-179">library location ID</span></span>   | <span data-ttu-id="5976a-180">N/D</span><span class="sxs-lookup"><span data-stu-id="5976a-180">N/A</span></span>           |
| <span data-ttu-id="5976a-181">tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-181">selected item type</span></span>    | <span data-ttu-id="5976a-182">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="5976a-182">CPAlbumID</span></span>     |
| <span data-ttu-id="5976a-183">ID elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-183">selected item ID</span></span>      | <span data-ttu-id="5976a-184">300</span><span class="sxs-lookup"><span data-stu-id="5976a-184">300</span></span>           |



 

<span data-ttu-id="5976a-185">Nel controllo di visualizzazione albero è selezionato il nodo radice per l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="5976a-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="5976a-186">In questo caso, non è presente alcun contenitore e, di conseguenza, non sono presenti elementi.</span><span class="sxs-lookup"><span data-stu-id="5976a-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="5976a-187">Il riquadro attività intera **libreria** Visualizza una pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="5976a-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="5976a-188">Elemento</span><span class="sxs-lookup"><span data-stu-id="5976a-188">Item</span></span>                  | <span data-ttu-id="5976a-189">valore</span><span class="sxs-lookup"><span data-stu-id="5976a-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="5976a-190">attività</span><span class="sxs-lookup"><span data-stu-id="5976a-190">task</span></span>                  | <span data-ttu-id="5976a-191">Esplora</span><span class="sxs-lookup"><span data-stu-id="5976a-191">Browse</span></span>          |
| <span data-ttu-id="5976a-192">tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-192">library location type</span></span> | <span data-ttu-id="5976a-193">RootLocation</span><span class="sxs-lookup"><span data-stu-id="5976a-193">RootLocation</span></span>    |
| <span data-ttu-id="5976a-194">ID percorso libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-194">library location ID</span></span>   | <span data-ttu-id="5976a-195">N/D</span><span class="sxs-lookup"><span data-stu-id="5976a-195">N/A</span></span>             |
| <span data-ttu-id="5976a-196">tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-196">selected item type</span></span>    | <span data-ttu-id="5976a-197">UnknownLocation</span><span class="sxs-lookup"><span data-stu-id="5976a-197">UnknownLocation</span></span> |
| <span data-ttu-id="5976a-198">ID elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-198">selected item ID</span></span>      | <span data-ttu-id="5976a-199">N/D</span><span class="sxs-lookup"><span data-stu-id="5976a-199">N/A</span></span>             |



 

<span data-ttu-id="5976a-200">Nel riquadro attività di **sincronizzazione** , il lettore Visualizza l'anno 2002 come contenitore di tracce.</span><span class="sxs-lookup"><span data-stu-id="5976a-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="5976a-201">Nella visualizzazione l'elemento selezionato corrisponde alla traccia con ID 450.</span><span class="sxs-lookup"><span data-stu-id="5976a-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="5976a-202">Elemento</span><span class="sxs-lookup"><span data-stu-id="5976a-202">Item</span></span>                  | <span data-ttu-id="5976a-203">valore</span><span class="sxs-lookup"><span data-stu-id="5976a-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="5976a-204">attività</span><span class="sxs-lookup"><span data-stu-id="5976a-204">task</span></span>                  | <span data-ttu-id="5976a-205">Sincronizza</span><span class="sxs-lookup"><span data-stu-id="5976a-205">Sync</span></span>            |
| <span data-ttu-id="5976a-206">tipo di percorso della libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-206">library location type</span></span> | <span data-ttu-id="5976a-207">ReleaseDateYear</span><span class="sxs-lookup"><span data-stu-id="5976a-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="5976a-208">ID percorso libreria</span><span class="sxs-lookup"><span data-stu-id="5976a-208">library location ID</span></span>   | <span data-ttu-id="5976a-209">2002</span><span class="sxs-lookup"><span data-stu-id="5976a-209">2002</span></span>            |
| <span data-ttu-id="5976a-210">tipo di elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-210">selected item type</span></span>    | <span data-ttu-id="5976a-211">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="5976a-211">CPTrackID</span></span>       |
| <span data-ttu-id="5976a-212">ID elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="5976a-212">selected item ID</span></span>      | <span data-ttu-id="5976a-213">450</span><span class="sxs-lookup"><span data-stu-id="5976a-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="5976a-214">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5976a-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5976a-215">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5976a-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5976a-216">**Pagine di individuazione**</span><span class="sxs-lookup"><span data-stu-id="5976a-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




