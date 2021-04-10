---
title: Enumerazione dei dispositivi (WMP SDK)
description: Enumerazione dei dispositivi
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, dispositivi portatili
- Modello a oggetti di Windows Media Player, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Controllo ActiveX Windows Media Player, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Controllo ActiveX Windows Media Player Mobile, dispositivi portatili
- Dispositivi portatili Windows Media Player Mobile
- dispositivi portatili, enumerazione
- enumerazioni, dispositivi portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5025d0e0a7e99028b22cc24ebc56337ea84d2fb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956191"
---
# <a name="enumerating-devices"></a><span data-ttu-id="5650a-112">Enumerazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="5650a-112">Enumerating Devices</span></span>

<span data-ttu-id="5650a-113">Windows Media Player rappresenta dispositivi portatili tramite l'interfaccia **IWMPSyncDevice** .</span><span class="sxs-lookup"><span data-stu-id="5650a-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="5650a-114">Nell'esempio di codice seguente viene illustrata una funzione che crea una matrice di puntatori a **IWMPSyncDevice**.</span><span class="sxs-lookup"><span data-stu-id="5650a-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="5650a-115">Ogni puntatore della matrice rappresenta un dispositivo per il quale Windows Media Player dispone di informazioni archiviate.</span><span class="sxs-lookup"><span data-stu-id="5650a-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="5650a-116">Non è necessario che un dispositivo sia connesso al computer, né deve avere una relazione con l'istanza corrente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5650a-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="5650a-117">È necessario enumerare i dispositivi ogni volta che si riceve l'evento **DeviceConnect** o **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="5650a-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="5650a-118">La funzione seguente enumera i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5650a-118">The following function enumerates devices.</span></span> <span data-ttu-id="5650a-119">Il parametro *bConnectedOnly* specifica se enumerare solo i dispositivi attualmente connessi al computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5650a-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="5650a-120">È possibile usare codice simile per recuperare altri elenchi di dispositivi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="5650a-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="5650a-121">Ad esempio, è possibile usare [IWMPSyncDevice:: Get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) per creare una matrice di dispositivi per cui esiste una relazione.</span><span class="sxs-lookup"><span data-stu-id="5650a-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5650a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5650a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5650a-123">**IWMPEvents2::D eviceConnect**</span><span class="sxs-lookup"><span data-stu-id="5650a-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="5650a-124">**IWMPEvents2::D eviceDisconnect**</span><span class="sxs-lookup"><span data-stu-id="5650a-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="5650a-125">**Interfaccia IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="5650a-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="5650a-126">**IWMPSyncDevice:: Get \_ Connected**</span><span class="sxs-lookup"><span data-stu-id="5650a-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="5650a-127">**Interfaccia IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="5650a-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="5650a-128">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="5650a-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




