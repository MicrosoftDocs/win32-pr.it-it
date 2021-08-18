---
title: Modifica della priorità di sincronizzazione
description: Modifica della priorità di sincronizzazione
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
keywords:
- Windows Media Player, playlist di sincronizzazione
- Windows Media Player a oggetti, playlist di sincronizzazione
- modello a oggetti, playlist di sincronizzazione
- Windows Media Player Dispositivi mobili, playlist di sincronizzazione
- Windows Media Player ActiveX, playlist di sincronizzazione
- Windows Media Player Controllo ActiveX per dispositivi mobili, playlist di sincronizzazione
- ActiveX, playlist di sincronizzazione
- playlist, sincronizzazione
- playlist di metafile, sincronizzazione
- Windows playlist metafile multimediali,sincronizzazione
- dispositivi portatili, modifica delle priorità della playlist di sincronizzazione
- playlist di sincronizzazione, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1513679bcde31893cd7c4f456bc0e99404bb5dc66de37976f2053ae1559a4cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997661"
---
# <a name="changing-synchronization-priority"></a>Modifica della priorità di sincronizzazione

Il codice di esempio seguente specifica un valore di priorità per ogni elemento nel controllo ListView identificato da IDC \_ PLVIEW. Agli elementi contrassegnati con un segno di spunta viene assegnato un valore di priorità in base al relativo ordine nell'elenco. Agli elementi non controllati viene assegnato un valore di priorità pari a zero.


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interfaccia IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




