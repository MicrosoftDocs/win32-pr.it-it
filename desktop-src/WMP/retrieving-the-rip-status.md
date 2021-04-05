---
title: Recupero dello stato di RIP
description: Recupero dello stato di RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, recupero dello stato RIP
- copia di CD, recupero dello stato di RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046348"
---
# <a name="retrieving-the-rip-status"></a>Recupero dello stato di RIP

È possibile monitorare lo stato di avanzamento dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Questo metodo recupera un valore di avanzamento per l'intera operazione di estrazione. Il valore recuperato è un numero che rappresenta la percentuale di ripping completata, da 0 a 100.

Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di estrazione. Per determinare lo stato di avanzamento di una traccia specifica, usare [IWMPMedia:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" come nome dell'attributo. Per determinare l'indice della traccia attualmente in fase di ripping, chiamare **IWMPPlaylist:: GetItemInfo** con "CurrentRipTrackIndex" come nome dell'attributo.

È possibile monitorare lo stato dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Questo metodo recupera un valore di enumerazione [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) che indica se l'operazione è in corso o è stata arrestata. È anche possibile monitorare lo stato dell'operazione di strappo gestendo l'evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . (Vedere [gestione di eventi in C++](handling-events-in-c.md)). Prestare attenzione a confrontare il puntatore **IWMPCdromRip** (fornito dall'evento) al puntatore che rappresenta l'operazione di strappo, per garantire che l'evento sia stato generato dall'operazione.

Nell'esempio di codice seguente viene illustrato come utilizzare queste funzioni per recuperare lo stato di un'operazione di estrazione.

I controlli della finestra di dialogo seguenti sono definiti per l'esempio di codice.



| ID controllo                   | Descrizione                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_traccia corrente di IDC \_          | Testo statico che rappresenta l'indice della traccia attualmente in fase di ripping.                                         |
| \_messaggio di \_ stato \_ traccia di IDC   | Testo statico che rappresenta lo stato di avanzamento della traccia attualmente ricopiata come percentuale.                      |
| \_traccia stato \_ IDC         | Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento della traccia attualmente ricopiata come percentuale. |
| \_testo di \_ stato \_ generale IDC | Testo statico che rappresenta lo stato di avanzamento del processo di strappo totale come percentuale.                             |
| \_stato di avanzamento IDC \_ generale       | Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento del processo di strappo totale come percentuale.        |
| \_stato RIP \_ IDC              | Testo statico che Visualizza l'operazione attualmente in esecuzione ("Rip", "Stopped" o "Unknown")             |



 


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

[**Copia di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di copia da CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Avvio del processo RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Selezione di elementi per l'estrazione**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




