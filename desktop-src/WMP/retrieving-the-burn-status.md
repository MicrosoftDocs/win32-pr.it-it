---
title: Recupero dello stato di masterizzazione
description: Recupero dello stato di masterizzazione
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dello stato di masterizzazione
- masterizzazione di CD, recupero dello stato di Burn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956205"
---
# <a name="retrieving-the-burn-status"></a>Recupero dello stato di masterizzazione

Nell'esempio di codice seguente vengono definiti i controlli della finestra di dialogo seguenti:



| ID controllo           | Descrizione                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| \_stato di Burn IDC \_     | Testo statico che rappresenta lo stato dell'operazione di masterizzazione del CD.             |
| \_stato IDC        | Indicatore di stato con un intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento totale. |
| \_testo stato \_ IDC  | Testo statico che rappresenta lo stato di avanzamento totale del Burn come numero compreso tra 0 e 100. |
| ora di IDC \_ disponibile \_ | Testo statico per visualizzare l'ora disponibile sul CD, in secondi.               |
| \_spazio disponibile \_ IDC     | Testo statico per visualizzare lo spazio disponibile sul CD, in byte.                     |
| \_spazio totale \_ IDC    | Testo statico per visualizzare la capacità totale del CD, in byte.                 |



 

È possibile monitorare lo stato di avanzamento dell'operazione di masterizzazione chiamando periodicamente [IWMPCdromBurn:: Get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) mentre è in corso il Burning del CD. Questo metodo recupera un valore di avanzamento per l'intera operazione di masterizzazione. Il valore recuperato è un numero che rappresenta la percentuale di masterizzazione completata, da 0 a 100.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



È possibile ottenere lo stato corrente dell'operazione di masterizzazione chiamando [IWMPCdromBurn:: Get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate). Questo metodo recupera un'enumerazione che specifica l'operazione corrente eseguita.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Per recuperare il numero di secondi di audio che il CD può mantenere, chiamare [IWMPCdromBurn:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) con "availabletime disponibile" come primo parametro. Il valore recuperato da questa funzione è rappresentato da una stringa.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Per recuperare la quantità di spazio libero su un disco, chiamare **IWMPCdromBurn:: GetItemInfo** con "FreeSpace" come primo parametro. Il valore recuperato da questa funzione è una stringa che rappresenta il numero di byte liberi disponibili sul disco.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Per recuperare la capacità totale di un disco, chiamare **IWMPCdromBurn:: GetItemInfo** con "TotalSpace" come primo parametro. Il valore recuperato da questa funzione è una stringa che corrisponde al numero totale di byte sul disco.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Masterizzazione di un CD**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Cancellazione di un CD riscrivibile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




