---
title: Recupero dello stato rip
description: Recupero dello stato rip
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, ripping CD
- Windows Media Player a oggetti, ripping cd
- modello a oggetti, ripping CD
- Windows Media Player ActiveX controllo, ripping CD
- ActiveX controllo, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping cd
- Windows Media Player Dispositivi mobili, ripping di CD
- Ripping cd, recupero dello stato di rip
- ripping di CD, recupero dello stato di rip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3210fa9e0db5f9260989d7bebb3650770cec7626892bc20546a6b602fb98955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570192"
---
# <a name="retrieving-the-rip-status"></a>Recupero dello stato rip

È possibile monitorare lo stato dell'operazione di ripping chiamando periodicamente [IWMPCdromRip::get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Questo metodo recupera un valore di stato per l'intera operazione di ripping. Il valore recuperato è un numero che rappresenta la percentuale di ripping completato, da 0 a 100.

Il valore di avanzamento rappresenta la percentuale completata dell'intero processo di ripping. Per determinare lo stato di avanzamento di una traccia specifica, usare [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" come nome dell'attributo. Per determinare l'indice della traccia attualmente in corso di decompressione, chiamare **IWMPPlaylist::getItemInfo** con "CurrentRipTrackIndex" come nome dell'attributo.

È possibile monitorare lo stato dell'operazione di ripping chiamando periodicamente [IWMPCdromRip::get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Questo metodo recupera un valore [di enumerazione WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) che indica se l'operazione è in corso o arrestata. È anche possibile monitorare lo stato dell'operazione di ripping gestendo l'evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) Vedere [Gestione degli eventi in C++.](handling-events-in-c.md) Fare attenzione a confrontare il puntatore **IWMPCdromRip** (fornito dall'evento) con il puntatore che rappresenta l'operazione di depping, per assicurarsi che l'evento sia stato generato dall'operazione.

Nell'esempio di codice seguente viene illustrato come usare queste funzioni per recuperare lo stato di un'operazione di depping.

I controlli finestra di dialogo seguenti sono definiti per l'esempio di codice.



| ID controllo                   | Descrizione                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| TRACCIA \_ CORRENTE IDC \_          | Testo statico che rappresenta l'indice della traccia attualmente decompressa.                                         |
| TESTO DI AVANZAMENTO TRACCIA IDC \_ \_ \_   | Testo statico che rappresenta lo stato di avanzamento della traccia attualmente decompressa come percentuale.                      |
| TRACCIA DELLO \_ STATO DI AVANZAMENTO \_ IDC         | Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento della traccia attualmente decompressa come percentuale. |
| TESTO DI STATO COMPLESSIVO IDC \_ \_ \_ | Testo statico che rappresenta lo stato di avanzamento del processo di depping totale come percentuale.                             |
| IDC \_ PROGRESS \_ OVERALL       | Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento del processo di ripping totale come percentuale.        |
| STATO \_ RIP \_ IDC              | Testo statico che visualizza l'operazione attualmente in esecuzione ("Ripping", "Stopped" o "Unknown")             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ripping di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di copia da CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Avvio del processo Rip**](starting-the-rip-process.md)
</dt> <dt>

[**Selezione degli elementi per il ripping**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




