---
title: Enumerazione dei dispositivi (WMP SDK)
description: Questo codice di esempio mostra una funzione che enumera i dispositivi creando una matrice di puntatori che rappresentano ognuno un dispositivo.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, dispositivi portatili
- Windows Media Player a oggetti, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Windows Media Player controllo ActiveX, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Windows Media Player controllo ActiveX mobile, dispositivi portatili
- Windows Media Player Mobile, dispositivi portatili
- dispositivi portatili, enumerazione
- enumerazioni, dispositivi portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068438"
---
# <a name="enumerating-devices"></a>Enumerazione dei dispositivi

Windows Media Player rappresenta i dispositivi portatili usando **l'interfaccia IWMPSyncDevice.** Il codice di esempio seguente illustra una funzione che crea una matrice di puntatori a **IWMPSyncDevice**. Ogni puntatore nella matrice rappresenta un dispositivo per cui Windows Media Player le informazioni archiviate. Un dispositivo non deve essere connesso al computer né deve avere una relazione con l'istanza Windows Media Player corrente.

È consigliabile enumerare i dispositivi ogni volta che si riceve **l'evento DeviceConnect** o **l'evento DeviceDisconnect.**

La funzione seguente enumera i dispositivi. Il *parametro bConnectedOnly* specifica se enumerare solo i dispositivi attualmente connessi al computer dell'utente.


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



È possibile usare codice simile per recuperare altri elenchi di dispositivi di questo tipo. Ad esempio, è possibile usare lo stato [IWMPSyncDevice::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) per creare una matrice di dispositivi per cui esiste una relazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMPEvents2::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ connected**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**Interfaccia IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




