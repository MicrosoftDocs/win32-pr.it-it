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
# <a name="showing-synchronization-progress"></a>Visualizzazione dello stato di avanzamento della sincronizzazione

È possibile visualizzare l'avanzamento della sincronizzazione all'utente. Nell'esempio di codice seguente viene illustrato come creare un timer per recuperare periodicamente il valore di avanzamento corrente utilizzando **IWMPSyncDevice:: Get \_ Progress**. Si noti che il valore di stato recuperato rappresenta lo stato di avanzamento dell'intera operazione di sincronizzazione per ogni dispositivo. Il recupero dello stato della sincronizzazione per singoli elementi multimediali non è supportato.

Per determinare quando avviare o arrestare il timer, gestire l'evento **DeviceSyncStateChange** . La funzione di esempio seguente illustra questo gestore eventi. Il codice visualizza anche lo stato di sincronizzazione corrente come stringa di testo usando un controllo di testo statico, denominato IDC \_ SYNCSTATE.


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



Quando il timer è in esecuzione, invia un \_ messaggio di timer WM a intervalli di un secondo. L'applicazione gestisce il \_ timer WM nel ciclo di messaggi.

La funzione di esempio seguente illustra come visualizzare lo stato di avanzamento usando sia un controllo testo statico (IDC \_ PROGSTATIC) che l'uso di un controllo Progress (IDC \_ SYNCPROG). Chiamare questa funzione in risposta al messaggio del \_ timer WM e al termine del processo di sincronizzazione, come illustrato nell'esempio precedente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Enumerazione dei dispositivi**](enumerating-devices.md)
</dt> <dt>

[**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Stato IWMPSyncDevice:: Get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**IWMPSyncDevice:: è identico**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Uso dei dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




