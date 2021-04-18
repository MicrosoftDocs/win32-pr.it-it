---
title: Enumerazione delle playlist di sincronizzazione
description: Enumerazione delle playlist di sincronizzazione
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
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
- playlist di sincronizzazione, enumerazione
- dispositivi portatili, enumerazione
- enumerazioni, playlist di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299416"
---
# <a name="enumerating-synchronization-playlists"></a>Enumerazione delle playlist di sincronizzazione

Il codice di esempio seguente crea una funzione che compila un controllo ListView con playlist. Prima vengono visualizzate le playlist di sincronizzazione. Le playlist di sincronizzazione per il dispositivo attualmente selezionato sono contrassegnate con un segno di spunta e sono ordinate in ordine di priorità di sincronizzazione. Tutte le altre playlist sono deselezionate.

Il controllo ListView è stato configurato per la selezione singola. L'ordine delle playlist nel controllo ListView determina la relativa priorità di sincronizzazione. Lo stato di selezione di una singola playlist determina se si tratta di una playlist di sincronizzazione per il dispositivo attualmente selezionato.

Il parametro *lPSIndex* specifica l'indice di relazione per il dispositivo portatile attualmente selezionato.


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



Per l'implementazione della funzione SortPlaylist, vedere [ordinamento delle playlist per priorità di sincronizzazione](sorting-playlists-by-synchronization-priority.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMPMedia:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPMediaCollection::getByAttribute**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributi di sincronizzazione**](sync-attributes.md)
</dt> </dl>

 

 




