---
title: Gestione delle playlist di sincronizzazione
description: Gestione delle playlist di sincronizzazione
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, dispositivi portatili
- Windows Media Player a oggetti, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Windows Media Player ActiveX, dispositivi portatili
- ActiveX, dispositivi portatili
- Windows Media Player Controllo ActiveX per dispositivi mobili, dispositivi portatili
- Windows Media Player Dispositivi mobili, portatili
- dispositivi portatili, gestione delle playlist di sincronizzazione
- Sincronizzazione dei dispositivi, playlist
- sincronizzazione di dispositivi, playlist
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
- playlist di sincronizzazione, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996371"
---
# <a name="managing-synchronization-playlists"></a>Gestione delle playlist di sincronizzazione

Windows Media Player 10 o versioni successive usa playlist per sincronizzare i file multimediali digitali con dispositivi portatili. Questa sezione illustra come usare le playlist di sincronizzazione.

Il codice di esempio in questa sezione usa due controlli ListView per visualizzare le informazioni. Il primo controllo ListView (IDC PLVIEW) visualizza tutte le playlist nella libreria Windows Media Player, con le playlist di \_ sincronizzazione visualizzate per prime. Le playlist di sincronizzazione per il dispositivo attualmente selezionato sono contrassegnate con un segno di spunta e sono ordinate in ordine di priorità di sincronizzazione. Tutte le altre playlist sono deselezionate. Il controllo ListView è stato configurato per la selezione singola. L'ordine delle playlist nel controllo ListView determina la priorità di sincronizzazione. Lo stato selezionato di una singola playlist determina se si tratta di una playlist di sincronizzazione per il dispositivo attualmente selezionato.

Il secondo controllo ListView (IDC \_ MEDIAVIEW) visualizza gli elementi multimediali nella playlist selezionata. Due colonne aggiuntive visualizzano il testo che indica se il file multimediale digitale è stato copiato nel dispositivo e, in caso di errore, se la copia non è riuscita perché il file multimediale digitale non è adatto.

Il codice di esempio seguente illustra come vengono inizializzati i controlli ListView:


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



La matrice di stringhe seguente contiene i nomi degli attributi di sincronizzazione usati negli esempi:


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



La variabile membro seguente contiene una playlist contenente tutte le playlist nella Windows Media Player libreria. Ogni playlist è rappresentata come elemento multimediale.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



Le sezioni seguenti forniscono codice di esempio:

-   [Enumerazione delle playlist di sincronizzazione](enumerating-synchronization-playlists.md)
-   [Ordinamento delle playlist in base alla priorità di sincronizzazione](sorting-playlists-by-synchronization-priority.md)
-   [Enumerazione degli elementi multimediali](enumerating-the-media-items.md)
-   [Determinazione dello stato di sincronizzazione della playlist](determining-playlist-synchronization-state.md)
-   [Modifica della priorità di sincronizzazione](changing-synchronization-priority.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




