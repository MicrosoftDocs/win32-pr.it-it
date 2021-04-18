---
title: Gestione delle playlist di sincronizzazione
description: Gestione delle playlist di sincronizzazione
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, dispositivi portatili
- Modello a oggetti di Windows Media Player, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Controllo ActiveX Windows Media Player, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Controllo ActiveX Windows Media Player Mobile, dispositivi portatili
- Dispositivi portatili Windows Media Player Mobile
- dispositivi portatili, gestione delle playlist di sincronizzazione
- sincronizzazione dei dispositivi, playlist
- sincronizzazione di dispositivi, playlist
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
- playlist di sincronizzazione, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298968"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="0a418-124">Gestione delle playlist di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0a418-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="0a418-125">Windows Media Player 10 o versioni successive usa le playlist per sincronizzare i file multimediali digitali con i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="0a418-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="0a418-126">Questa sezione illustra come usare le playlist di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0a418-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="0a418-127">Il codice di esempio in questa sezione usa due controlli ListView per visualizzare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0a418-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="0a418-128">Il primo controllo ListView (IDC \_ PLVIEW) Visualizza tutte le playlist nella libreria Media Player di Windows, con le playlist di sincronizzazione visualizzate per prime.</span><span class="sxs-lookup"><span data-stu-id="0a418-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="0a418-129">Le playlist di sincronizzazione per il dispositivo attualmente selezionato sono contrassegnate con un segno di spunta e sono ordinate in ordine di priorità di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0a418-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="0a418-130">Tutte le altre playlist sono deselezionate.</span><span class="sxs-lookup"><span data-stu-id="0a418-130">All other playlists are unchecked.</span></span> <span data-ttu-id="0a418-131">Il controllo ListView è stato configurato per la selezione singola.</span><span class="sxs-lookup"><span data-stu-id="0a418-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="0a418-132">L'ordine delle playlist nel controllo ListView determina la relativa priorità di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0a418-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="0a418-133">Lo stato di selezione di una singola playlist determina se si tratta di una playlist di sincronizzazione per il dispositivo attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0a418-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="0a418-134">Il secondo controllo ListView (IDC \_ MEDIAVIEW) Visualizza gli elementi multimediali nella playlist selezionata.</span><span class="sxs-lookup"><span data-stu-id="0a418-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="0a418-135">Due colonne aggiuntive visualizzano il testo che indica se il file multimediale digitale è stato copiato nel dispositivo e, in caso di errore, se la copia non è riuscita perché il file multimediale digitale non è adatto.</span><span class="sxs-lookup"><span data-stu-id="0a418-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="0a418-136">Il codice di esempio seguente mostra come vengono inizializzati i controlli ListView:</span><span class="sxs-lookup"><span data-stu-id="0a418-136">The following example code shows how the ListView controls are initialized:</span></span>


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



<span data-ttu-id="0a418-137">La matrice di stringhe seguente contiene i nomi degli attributi di sincronizzazione utilizzati negli esempi:</span><span class="sxs-lookup"><span data-stu-id="0a418-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



<span data-ttu-id="0a418-138">La variabile membro seguente contiene una playlist contenente tutte le playlist nella libreria Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="0a418-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="0a418-139">Ogni playlist è rappresentata come un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="0a418-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="0a418-140">Nelle sezioni seguenti viene fornito codice di esempio:</span><span class="sxs-lookup"><span data-stu-id="0a418-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="0a418-141">Enumerazione delle playlist di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0a418-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="0a418-142">Ordinamento delle playlist per priorità di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0a418-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="0a418-143">Enumerazione degli elementi multimediali</span><span class="sxs-lookup"><span data-stu-id="0a418-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="0a418-144">Determinazione dello stato di sincronizzazione della playlist</span><span class="sxs-lookup"><span data-stu-id="0a418-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="0a418-145">Modifica della priorità di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0a418-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="0a418-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a418-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a418-147">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="0a418-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




