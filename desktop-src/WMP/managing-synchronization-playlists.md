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
# <a name="managing-synchronization-playlists"></a>Gestione delle playlist di sincronizzazione

Windows Media Player 10 o versioni successive usa le playlist per sincronizzare i file multimediali digitali con i dispositivi portatili. Questa sezione illustra come usare le playlist di sincronizzazione.

Il codice di esempio in questa sezione usa due controlli ListView per visualizzare le informazioni. Il primo controllo ListView (IDC \_ PLVIEW) Visualizza tutte le playlist nella libreria Media Player di Windows, con le playlist di sincronizzazione visualizzate per prime. Le playlist di sincronizzazione per il dispositivo attualmente selezionato sono contrassegnate con un segno di spunta e sono ordinate in ordine di priorità di sincronizzazione. Tutte le altre playlist sono deselezionate. Il controllo ListView è stato configurato per la selezione singola. L'ordine delle playlist nel controllo ListView determina la relativa priorità di sincronizzazione. Lo stato di selezione di una singola playlist determina se si tratta di una playlist di sincronizzazione per il dispositivo attualmente selezionato.

Il secondo controllo ListView (IDC \_ MEDIAVIEW) Visualizza gli elementi multimediali nella playlist selezionata. Due colonne aggiuntive visualizzano il testo che indica se il file multimediale digitale è stato copiato nel dispositivo e, in caso di errore, se la copia non è riuscita perché il file multimediale digitale non è adatto.

Il codice di esempio seguente mostra come vengono inizializzati i controlli ListView:


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



La matrice di stringhe seguente contiene i nomi degli attributi di sincronizzazione utilizzati negli esempi:


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



La variabile membro seguente contiene una playlist contenente tutte le playlist nella libreria Media Player di Windows. Ogni playlist è rappresentata come un elemento multimediale.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



Nelle sezioni seguenti viene fornito codice di esempio:

-   [Enumerazione delle playlist di sincronizzazione](enumerating-synchronization-playlists.md)
-   [Ordinamento delle playlist per priorità di sincronizzazione](sorting-playlists-by-synchronization-priority.md)
-   [Enumerazione degli elementi multimediali](enumerating-the-media-items.md)
-   [Determinazione dello stato di sincronizzazione della playlist](determining-playlist-synchronization-state.md)
-   [Modifica della priorità di sincronizzazione](changing-synchronization-priority.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




