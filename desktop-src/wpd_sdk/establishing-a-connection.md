---
description: Istituzione di una connessione
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Istituzione di una connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058330"
---
# <a name="establishing-a-connection"></a>Istituzione di una connessione

Quando l'utente seleziona un dispositivo, la funzione ChooseDevice chiama a sua volta il metodo [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) per stabilire una connessione tra l'applicazione e il dispositivo. Il metodo IPortableDevice:: Open accetta due argomenti:

-   Puntatore a una stringa con terminazione null che specifica il nome Plug and Play del dispositivo. Questa stringa viene recuperata chiamando il metodo [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .
-   Puntatore a un' [**interfaccia IPortableDeviceValues**](iportabledevicevalues.md) che specifica le informazioni client per l'applicazione.


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



Per Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supporta due CLSID per **CoCreateInstance**. **CLSID \_ PortableDevice** restituisce un puntatore **IPortableDevice** che non aggrega il gestore di marshalling a thread libero. **CLSID \_ PortableDeviceFTM** è un nuovo CLSID che restituisce un puntatore **IPortableDevice** che aggrega il gestore di marshalling a thread libero. Entrambi i puntatori supportano la stessa funzionalità in caso contrario.

Le applicazioni che si trovano in Apartment a thread singolo devono usare **CLSID \_ PortableDeviceFTM** , in quanto in questo modo si elimina l'overhead del marshalling del puntatore di interfaccia. **CLSID \_ PortableDevice** è ancora supportato per le applicazioni legacy.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Selezione di un dispositivo**](selecting-a-device.md)
</dt> </dl>

 

 



