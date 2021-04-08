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
# <a name="sorting-playlists-by-synchronization-priority"></a>Ordinamento delle playlist per priorità di sincronizzazione

Il codice seguente esegue una semplice sequenza di playlist. È possibile osservare come questa funzione viene usata nel codice di esempio nell' [enumerazione delle playlist di sincronizzazione](enumerating-synchronization-playlists.md). La funzione accetta i parametri seguenti:

-   *pPlaylist*. Puntatore alla playlist di Windows Media Player da ordinare. Gli elementi multimediali nella playlist devono puntare ad altre playlist, non a singoli file multimediali digitali.
-   *bstrSyncAttribute*. BSTR contenente il nome dell'attributo della relazione di sincronizzazione per il dispositivo corrente ("Sync01", "Sync02" e così via).
-   *plSelected*. Puntatore a una variabile **Long** che riceve il numero di playlist di sincronizzazione.

La funzione esamina l'attributo della relazione di sincronizzazione per ogni elemento multimediale (che rappresenta una playlist) nella playlist specificata da *pPlaylist*. Se l'attributo ha un valore diverso da zero, il codice sposta l'elemento del supporto all'inizio della playlist e lo inserisce in ordine di priorità.

Al termine, la funzione restituisce il numero di elementi multimediali (playlist di sincronizzazione) con un valore diverso da zero per l'attributo della relazione di sincronizzazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMPMedia:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**Elemento IWMPPlaylist:: Get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**IWMPPlaylist:: moveItem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributi di sincronizzazione**](sync-attributes.md)
</dt> </dl>

 

 




