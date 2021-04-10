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
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="8fe7c-112">Recupero dello stato di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="8fe7c-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="8fe7c-113">Nell'esempio di codice seguente vengono definiti i controlli della finestra di dialogo seguenti:</span><span class="sxs-lookup"><span data-stu-id="8fe7c-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="8fe7c-114">ID controllo</span><span class="sxs-lookup"><span data-stu-id="8fe7c-114">Control ID</span></span>           | <span data-ttu-id="8fe7c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe7c-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8fe7c-116">\_stato di Burn IDC \_</span><span class="sxs-lookup"><span data-stu-id="8fe7c-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="8fe7c-117">Testo statico che rappresenta lo stato dell'operazione di masterizzazione del CD.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="8fe7c-118">\_stato IDC</span><span class="sxs-lookup"><span data-stu-id="8fe7c-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="8fe7c-119">Indicatore di stato con un intervallo compreso tra 0 e 100 che rappresenta lo stato di avanzamento totale.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="8fe7c-120">\_testo stato \_ IDC</span><span class="sxs-lookup"><span data-stu-id="8fe7c-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="8fe7c-121">Testo statico che rappresenta lo stato di avanzamento totale del Burn come numero compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="8fe7c-122">ora di IDC \_ disponibile \_</span><span class="sxs-lookup"><span data-stu-id="8fe7c-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="8fe7c-123">Testo statico per visualizzare l'ora disponibile sul CD, in secondi.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="8fe7c-124">\_spazio disponibile \_ IDC</span><span class="sxs-lookup"><span data-stu-id="8fe7c-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="8fe7c-125">Testo statico per visualizzare lo spazio disponibile sul CD, in byte.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="8fe7c-126">\_spazio totale \_ IDC</span><span class="sxs-lookup"><span data-stu-id="8fe7c-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="8fe7c-127">Testo statico per visualizzare la capacità totale del CD, in byte.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="8fe7c-128">È possibile monitorare lo stato di avanzamento dell'operazione di masterizzazione chiamando periodicamente [IWMPCdromBurn:: Get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) mentre è in corso il Burning del CD.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="8fe7c-129">Questo metodo recupera un valore di avanzamento per l'intera operazione di masterizzazione.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="8fe7c-130">Il valore recuperato è un numero che rappresenta la percentuale di masterizzazione completata, da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


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



<span data-ttu-id="8fe7c-131">È possibile ottenere lo stato corrente dell'operazione di masterizzazione chiamando [IWMPCdromBurn:: Get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span><span class="sxs-lookup"><span data-stu-id="8fe7c-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="8fe7c-132">Questo metodo recupera un'enumerazione che specifica l'operazione corrente eseguita.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


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



<span data-ttu-id="8fe7c-133">Per recuperare il numero di secondi di audio che il CD può mantenere, chiamare [IWMPCdromBurn:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) con "availabletime disponibile" come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="8fe7c-134">Il valore recuperato da questa funzione è rappresentato da una stringa.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-134">The value retrieved by this function is represented by a string.</span></span>


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



<span data-ttu-id="8fe7c-135">Per recuperare la quantità di spazio libero su un disco, chiamare **IWMPCdromBurn:: GetItemInfo** con "FreeSpace" come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="8fe7c-136">Il valore recuperato da questa funzione è una stringa che rappresenta il numero di byte liberi disponibili sul disco.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


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



<span data-ttu-id="8fe7c-137">Per recuperare la capacità totale di un disco, chiamare **IWMPCdromBurn:: GetItemInfo** con "TotalSpace" come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="8fe7c-138">Il valore recuperato da questa funzione è una stringa che corrisponde al numero totale di byte sul disco.</span><span class="sxs-lookup"><span data-stu-id="8fe7c-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8fe7c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fe7c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fe7c-140">**Masterizzazione di un CD**</span><span class="sxs-lookup"><span data-stu-id="8fe7c-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="8fe7c-141">**Recupero dell'interfaccia di masterizzazione CD**</span><span class="sxs-lookup"><span data-stu-id="8fe7c-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="8fe7c-142">**Avvio del processo di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="8fe7c-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="8fe7c-143">**Cancellazione di un CD riscrivibile**</span><span class="sxs-lookup"><span data-stu-id="8fe7c-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="8fe7c-144">**Recupero dello stato dell'unità e del disco**</span><span class="sxs-lookup"><span data-stu-id="8fe7c-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




