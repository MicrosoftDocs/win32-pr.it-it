---
title: Ordinamento delle playlist per priorità di sincronizzazione
description: Ordinamento delle playlist per priorità di sincronizzazione
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Media Player di Windows, playlist di sincronizzazione
- Modello a oggetti di Windows Media Player, playlist di sincronizzazione
- modello a oggetti, playlist di sincronizzazione
- Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX di Windows Media Player, playlist di sincronizzazione
- Controllo ActiveX Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX, playlist di sincronizzazione
- playlist, sincronizzazione
- playlist di metafile, sincronizzazione
- Playlist di Windows Media Metafile, sincronizzazione
- dispositivi portatili, ordinamento delle playlist di sincronizzazione
- playlist di sincronizzazione, ordinamento
- playlist di sincronizzazione, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858018"
---
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="23a59-116">Ordinamento delle playlist per priorità di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="23a59-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="23a59-117">Il codice seguente esegue una semplice sequenza di playlist.</span><span class="sxs-lookup"><span data-stu-id="23a59-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="23a59-118">È possibile osservare come questa funzione viene usata nel codice di esempio nell' [enumerazione delle playlist di sincronizzazione](enumerating-synchronization-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="23a59-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="23a59-119">La funzione accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="23a59-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="23a59-120">*pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="23a59-120">*pPlaylist*.</span></span> <span data-ttu-id="23a59-121">Puntatore alla playlist di Windows Media Player da ordinare.</span><span class="sxs-lookup"><span data-stu-id="23a59-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="23a59-122">Gli elementi multimediali nella playlist devono puntare ad altre playlist, non a singoli file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="23a59-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="23a59-123">*bstrSyncAttribute*.</span><span class="sxs-lookup"><span data-stu-id="23a59-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="23a59-124">BSTR contenente il nome dell'attributo della relazione di sincronizzazione per il dispositivo corrente ("Sync01", "Sync02" e così via).</span><span class="sxs-lookup"><span data-stu-id="23a59-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="23a59-125">*plSelected*.</span><span class="sxs-lookup"><span data-stu-id="23a59-125">*plSelected*.</span></span> <span data-ttu-id="23a59-126">Puntatore a una variabile **Long** che riceve il numero di playlist di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="23a59-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="23a59-127">La funzione esamina l'attributo della relazione di sincronizzazione per ogni elemento multimediale (che rappresenta una playlist) nella playlist specificata da *pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="23a59-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="23a59-128">Se l'attributo ha un valore diverso da zero, il codice sposta l'elemento del supporto all'inizio della playlist e lo inserisce in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="23a59-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="23a59-129">Al termine, la funzione restituisce il numero di elementi multimediali (playlist di sincronizzazione) con un valore diverso da zero per l'attributo della relazione di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="23a59-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="23a59-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23a59-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a59-131">**IWMPMedia:: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="23a59-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="23a59-132">**Elemento IWMPPlaylist:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="23a59-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="23a59-133">**IWMPPlaylist:: moveItem**</span><span class="sxs-lookup"><span data-stu-id="23a59-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="23a59-134">**Gestione delle playlist di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="23a59-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="23a59-135">**Attributi di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="23a59-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




