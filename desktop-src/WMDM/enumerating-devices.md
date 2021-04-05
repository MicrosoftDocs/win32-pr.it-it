---
title: Enumerazione dei dispositivi Windows Media Gestione dispositivi
description: Enumerazione dei dispositivi
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media Gestione dispositivi, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- Guida per programmatori, enumerazione dei dispositivi
- applicazioni desktop, enumerazione dei dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, enumerazione di dispositivi
- Enumerazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3584e625f54ea4e5c601f2a32865515c824cfcd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104117233"
---
# <a name="enumerating-windows-media-device-manager-devices"></a>Enumerazione dei dispositivi Windows Media Gestione dispositivi

Dopo aver autenticato un'applicazione, è possibile iniziare a enumerare i dispositivi rilevati da Windows Media Gestione dispositivi. L'enumerazione viene eseguita utilizzando un'interfaccia di enumerazione, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), ottenuta utilizzando [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) o [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices). Se supportato, usare il metodo **EnumDevices2** , perché la versione precedente ha restituito solo le interfacce legacy nei dispositivi, mentre la nuova versione restituisce sia le interfacce legacy che le nuove.

Prima di ottenere un enumeratore, è necessario decidere quale visualizzazione dell'enumerazione usare. Alcuni dispositivi espongono ogni risorsa di archiviazione come dispositivo diverso. Ad esempio, due schede di memoria flash in un dispositivo verranno enumerate come se fossero dispositivi separati. È possibile specificare che tutte le archiviazioni in un dispositivo vengono enumerate insieme come singolo dispositivo. È possibile impostare questa preferenza solo una volta nell'applicazione. Se si vuole modificarlo, è necessario arrestare l'applicazione e riavviarla. Si noti tuttavia che i dispositivi legacy ignoreranno a volte una richiesta di enumerazione di archivi di dispositivi distinti come singolo dispositivo e continuano a enumerarli separatamente.

Nei passaggi seguenti viene illustrato come enumerare i dispositivi connessi:

1.  Impostare la preferenza di enumerazione del dispositivo usando [**IWMDeviceManager3:: SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference). Se questo metodo non viene chiamato, il metodo predefinito consente di visualizzare le archiviazioni come dispositivi distinti. Per determinare se i singoli "dispositivi" sono in realtà archivi sullo stesso dispositivo, chiamare [**IWMDMDevice2:: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); le archiviazioni dello stesso dispositivo restituiscono valori identici, ad eccezione della cifra finale dopo l'ultimo segno "$".
2.  Eseguire una query per [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) o [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)e quindi chiamare [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) per ottenere l'interfaccia dell'enumeratore del dispositivo, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). (Se supportato, usare **EnumDevices2**, che è più efficiente, perché la versione precedente non può restituire i dispositivi MTP).
3.  Chiamare il metodo [**IWMDMEnumDevices:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) per recuperare uno o più dispositivi alla volta. Continuare a chiamare questo metodo finché il metodo non restituisce \_ false o un messaggio di errore. Se si recupera un solo dispositivo alla volta, non è necessario allocare una matrice in cui devono essere contenuta i dispositivi.

Poiché gli utenti possono collegare o rimuovere dispositivi dal computer mentre l'applicazione è in esecuzione, è consigliabile implementare la notifica della connessione o della rimozione del dispositivo. Questa operazione viene eseguita implementando l'interfaccia [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) e registrando tale interfaccia. Per ulteriori informazioni, vedere [Abilitazione di notifiche](enabling-notifications.md).

Il codice C++ seguente enumera i dispositivi e richiede le informazioni su ogni dispositivo.


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




