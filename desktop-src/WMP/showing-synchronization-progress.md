---
title: Visualizzazione dello stato di avanzamento della sincronizzazione
description: Visualizzazione dello stato di avanzamento della sincronizzazione
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player, dispositivi portatili
- Modello a oggetti di Windows Media Player, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Controllo ActiveX Windows Media Player, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Controllo ActiveX Windows Media Player Mobile, dispositivi portatili
- Dispositivi portatili Windows Media Player Mobile
- dispositivi portatili, stato della sincronizzazione
- sincronizzazione dei dispositivi, visualizzazione dello stato di avanzamento
- sincronizzazione dei dispositivi, visualizzazione dello stato di avanzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858010"
---
# <a name="showing-synchronization-progress"></a><span data-ttu-id="f6f66-113">Visualizzazione dello stato di avanzamento della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="f6f66-113">Showing Synchronization Progress</span></span>

<span data-ttu-id="f6f66-114">È possibile visualizzare l'avanzamento della sincronizzazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="f6f66-114">You can display synchronization progress to the user.</span></span> <span data-ttu-id="f6f66-115">Nell'esempio di codice seguente viene illustrato come creare un timer per recuperare periodicamente il valore di avanzamento corrente utilizzando **IWMPSyncDevice:: Get \_ Progress**.</span><span class="sxs-lookup"><span data-stu-id="f6f66-115">The following example code shows how to create a timer to periodically retrieve the current progress value by using **IWMPSyncDevice::get\_progress**.</span></span> <span data-ttu-id="f6f66-116">Si noti che il valore di stato recuperato rappresenta lo stato di avanzamento dell'intera operazione di sincronizzazione per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6f66-116">Note that the progress value retrieved represents the progress for the entire synchronization operation for each device.</span></span> <span data-ttu-id="f6f66-117">Il recupero dello stato della sincronizzazione per singoli elementi multimediali non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f6f66-117">Retrieving synchronization progress for individual media items is not supported.</span></span>

<span data-ttu-id="f6f66-118">Per determinare quando avviare o arrestare il timer, gestire l'evento **DeviceSyncStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f6f66-118">To determine when to start or stop the timer, handle the **DeviceSyncStateChange** event.</span></span> <span data-ttu-id="f6f66-119">La funzione di esempio seguente illustra questo gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="f6f66-119">The following example function demonstrates such an event handler.</span></span> <span data-ttu-id="f6f66-120">Il codice visualizza anche lo stato di sincronizzazione corrente come stringa di testo usando un controllo di testo statico, denominato IDC \_ SYNCSTATE.</span><span class="sxs-lookup"><span data-stu-id="f6f66-120">The code also displays the current synchronization state as a text string using a static text control, named IDC\_SYNCSTATE.</span></span>


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



<span data-ttu-id="f6f66-121">Quando il timer è in esecuzione, invia un \_ messaggio di timer WM a intervalli di un secondo.</span><span class="sxs-lookup"><span data-stu-id="f6f66-121">When the timer is running, it sends a WM\_TIMER message at one-second intervals.</span></span> <span data-ttu-id="f6f66-122">L'applicazione gestisce il \_ timer WM nel ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="f6f66-122">The application handles WM\_TIMER in its message loop.</span></span>

<span data-ttu-id="f6f66-123">La funzione di esempio seguente illustra come visualizzare lo stato di avanzamento usando sia un controllo testo statico (IDC \_ PROGSTATIC) che l'uso di un controllo Progress (IDC \_ SYNCPROG).</span><span class="sxs-lookup"><span data-stu-id="f6f66-123">The following example function demonstrates how to show progress by using both a static text control (IDC\_PROGSTATIC), and using a progress control (IDC\_SYNCPROG).</span></span> <span data-ttu-id="f6f66-124">Chiamare questa funzione in risposta al messaggio del \_ timer WM e al termine del processo di sincronizzazione, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="f6f66-124">Call this function in response to the WM\_TIMER message and upon completion of the synchronization process, as shown in the preceding example.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6f66-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6f66-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6f66-126">**Enumerazione dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="f6f66-126">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="f6f66-127">**Interfaccia IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="f6f66-127">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="f6f66-128">**Stato IWMPSyncDevice:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="f6f66-128">**IWMPSyncDevice::get\_progress**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[<span data-ttu-id="f6f66-129">**IWMPSyncDevice:: è identico**</span><span class="sxs-lookup"><span data-stu-id="f6f66-129">**IWMPSyncDevice::isIdentical**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[<span data-ttu-id="f6f66-130">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="f6f66-130">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




