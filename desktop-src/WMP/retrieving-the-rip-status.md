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
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="b3729-112">Recupero dello stato di RIP</span><span class="sxs-lookup"><span data-stu-id="b3729-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="b3729-113">È possibile monitorare lo stato di avanzamento dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="b3729-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="b3729-114">Questo metodo recupera un valore di avanzamento per l'intera operazione di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b3729-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="b3729-115">Il valore recuperato è un numero che rappresenta la percentuale di ripping completata, da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="b3729-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="b3729-116">Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b3729-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="b3729-117">Per determinare lo stato di avanzamento di una traccia specifica, usare [IWMPMedia:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" come nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="b3729-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="b3729-118">Per determinare l'indice della traccia attualmente in fase di ripping, chiamare **IWMPPlaylist:: GetItemInfo** con "CurrentRipTrackIndex" come nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="b3729-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="b3729-119">È possibile monitorare lo stato dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="b3729-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="b3729-120">Questo metodo recupera un valore di enumerazione [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) che indica se l'operazione è in corso o è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="b3729-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="b3729-121">È anche possibile monitorare lo stato dell'operazione di strappo gestendo l'evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="b3729-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="b3729-122">(Vedere [gestione di eventi in C++](handling-events-in-c.md)). Prestare attenzione a confrontare il puntatore **IWMPCdromRip** (fornito dall'evento) al puntatore che rappresenta l'operazione di strappo, per garantire che l'evento sia stato generato dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="b3729-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="b3729-123">Nell'esempio di codice seguente viene illustrato come utilizzare queste funzioni per recuperare lo stato di un'operazione di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b3729-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="b3729-124">I controlli della finestra di dialogo seguenti sono definiti per l'esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="b3729-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="b3729-125">ID controllo</span><span class="sxs-lookup"><span data-stu-id="b3729-125">Control ID</span></span>                   | <span data-ttu-id="b3729-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3729-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3729-127">\_traccia corrente di IDC \_</span><span class="sxs-lookup"><span data-stu-id="b3729-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="b3729-128">Testo statico che rappresenta l'indice della traccia attualmente in fase di ripping.</span><span class="sxs-lookup"><span data-stu-id="b3729-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="b3729-129">\_messaggio di \_ stato \_ traccia di IDC</span><span class="sxs-lookup"><span data-stu-id="b3729-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="b3729-130">Testo statico che rappresenta lo stato di avanzamento della traccia attualmente ricopiata come percentuale.</span><span class="sxs-lookup"><span data-stu-id="b3729-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="b3729-131">\_traccia stato \_ IDC</span><span class="sxs-lookup"><span data-stu-id="b3729-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="b3729-132">Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento della traccia attualmente ricopiata come percentuale.</span><span class="sxs-lookup"><span data-stu-id="b3729-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="b3729-133">\_testo di \_ stato \_ generale IDC</span><span class="sxs-lookup"><span data-stu-id="b3729-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="b3729-134">Testo statico che rappresenta lo stato di avanzamento del processo di strappo totale come percentuale.</span><span class="sxs-lookup"><span data-stu-id="b3729-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="b3729-135">\_stato di avanzamento IDC \_ generale</span><span class="sxs-lookup"><span data-stu-id="b3729-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="b3729-136">Indicatore di stato con intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento del processo di strappo totale come percentuale.</span><span class="sxs-lookup"><span data-stu-id="b3729-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="b3729-137">\_stato RIP \_ IDC</span><span class="sxs-lookup"><span data-stu-id="b3729-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="b3729-138">Testo statico che Visualizza l'operazione attualmente in esecuzione ("Rip", "Stopped" o "Unknown")</span><span class="sxs-lookup"><span data-stu-id="b3729-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


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



## <a name="related-topics"></a><span data-ttu-id="b3729-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3729-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3729-140">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="b3729-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="b3729-141">**Recupero dell'interfaccia di copia da CD**</span><span class="sxs-lookup"><span data-stu-id="b3729-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="b3729-142">**Avvio del processo RIP**</span><span class="sxs-lookup"><span data-stu-id="b3729-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="b3729-143">**Selezione di elementi per l'estrazione**</span><span class="sxs-lookup"><span data-stu-id="b3729-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




