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
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="c2a63-109">Enumerazione dei dispositivi Windows Media Gestione dispositivi</span><span class="sxs-lookup"><span data-stu-id="c2a63-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="c2a63-110">Dopo aver autenticato un'applicazione, è possibile iniziare a enumerare i dispositivi rilevati da Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c2a63-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="c2a63-111">L'enumerazione viene eseguita utilizzando un'interfaccia di enumerazione, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), ottenuta utilizzando [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) o [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span><span class="sxs-lookup"><span data-stu-id="c2a63-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="c2a63-112">Se supportato, usare il metodo **EnumDevices2** , perché la versione precedente ha restituito solo le interfacce legacy nei dispositivi, mentre la nuova versione restituisce sia le interfacce legacy che le nuove.</span><span class="sxs-lookup"><span data-stu-id="c2a63-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="c2a63-113">Prima di ottenere un enumeratore, è necessario decidere quale visualizzazione dell'enumerazione usare.</span><span class="sxs-lookup"><span data-stu-id="c2a63-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="c2a63-114">Alcuni dispositivi espongono ogni risorsa di archiviazione come dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="c2a63-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="c2a63-115">Ad esempio, due schede di memoria flash in un dispositivo verranno enumerate come se fossero dispositivi separati.</span><span class="sxs-lookup"><span data-stu-id="c2a63-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="c2a63-116">È possibile specificare che tutte le archiviazioni in un dispositivo vengono enumerate insieme come singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2a63-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="c2a63-117">È possibile impostare questa preferenza solo una volta nell'applicazione. Se si vuole modificarlo, è necessario arrestare l'applicazione e riavviarla.</span><span class="sxs-lookup"><span data-stu-id="c2a63-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="c2a63-118">Si noti tuttavia che i dispositivi legacy ignoreranno a volte una richiesta di enumerazione di archivi di dispositivi distinti come singolo dispositivo e continuano a enumerarli separatamente.</span><span class="sxs-lookup"><span data-stu-id="c2a63-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="c2a63-119">Nei passaggi seguenti viene illustrato come enumerare i dispositivi connessi:</span><span class="sxs-lookup"><span data-stu-id="c2a63-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="c2a63-120">Impostare la preferenza di enumerazione del dispositivo usando [**IWMDeviceManager3:: SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span><span class="sxs-lookup"><span data-stu-id="c2a63-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="c2a63-121">Se questo metodo non viene chiamato, il metodo predefinito consente di visualizzare le archiviazioni come dispositivi distinti.</span><span class="sxs-lookup"><span data-stu-id="c2a63-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="c2a63-122">Per determinare se i singoli "dispositivi" sono in realtà archivi sullo stesso dispositivo, chiamare [**IWMDMDevice2:: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); le archiviazioni dello stesso dispositivo restituiscono valori identici, ad eccezione della cifra finale dopo l'ultimo segno "$".</span><span class="sxs-lookup"><span data-stu-id="c2a63-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="c2a63-123">Eseguire una query per [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) o [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)e quindi chiamare [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) per ottenere l'interfaccia dell'enumeratore del dispositivo, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span><span class="sxs-lookup"><span data-stu-id="c2a63-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="c2a63-124">(Se supportato, usare **EnumDevices2**, che è più efficiente, perché la versione precedente non può restituire i dispositivi MTP).</span><span class="sxs-lookup"><span data-stu-id="c2a63-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="c2a63-125">Chiamare il metodo [**IWMDMEnumDevices:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) per recuperare uno o più dispositivi alla volta.</span><span class="sxs-lookup"><span data-stu-id="c2a63-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="c2a63-126">Continuare a chiamare questo metodo finché il metodo non restituisce \_ false o un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c2a63-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="c2a63-127">Se si recupera un solo dispositivo alla volta, non è necessario allocare una matrice in cui devono essere contenuta i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c2a63-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="c2a63-128">Poiché gli utenti possono collegare o rimuovere dispositivi dal computer mentre l'applicazione è in esecuzione, è consigliabile implementare la notifica della connessione o della rimozione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2a63-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="c2a63-129">Questa operazione viene eseguita implementando l'interfaccia [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) e registrando tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c2a63-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="c2a63-130">Per ulteriori informazioni, vedere [Abilitazione di notifiche](enabling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c2a63-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="c2a63-131">Il codice C++ seguente enumera i dispositivi e richiede le informazioni su ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2a63-131">The following C++ code enumerates devices and requests information about each device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c2a63-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2a63-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2a63-133">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="c2a63-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




