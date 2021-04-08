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
# <a name="establishing-a-connection"></a><span data-ttu-id="cd5af-103">Istituzione di una connessione</span><span class="sxs-lookup"><span data-stu-id="cd5af-103">Establishing a Connection</span></span>

<span data-ttu-id="cd5af-104">Quando l'utente seleziona un dispositivo, la funzione ChooseDevice chiama a sua volta il metodo [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) per stabilire una connessione tra l'applicazione e il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd5af-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="cd5af-105">Il metodo IPortableDevice:: Open accetta due argomenti:</span><span class="sxs-lookup"><span data-stu-id="cd5af-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="cd5af-106">Puntatore a una stringa con terminazione null che specifica il nome Plug and Play del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd5af-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="cd5af-107">Questa stringa viene recuperata chiamando il metodo [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .</span><span class="sxs-lookup"><span data-stu-id="cd5af-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="cd5af-108">Puntatore a un' [**interfaccia IPortableDeviceValues**](iportabledevicevalues.md) che specifica le informazioni client per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd5af-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


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



<span data-ttu-id="cd5af-109">Per Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supporta due CLSID per **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="cd5af-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="cd5af-110">**CLSID \_ PortableDevice** restituisce un puntatore **IPortableDevice** che non aggrega il gestore di marshalling a thread libero. **CLSID \_ PortableDeviceFTM** è un nuovo CLSID che restituisce un puntatore **IPortableDevice** che aggrega il gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="cd5af-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="cd5af-111">Entrambi i puntatori supportano la stessa funzionalità in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cd5af-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="cd5af-112">Le applicazioni che si trovano in Apartment a thread singolo devono usare **CLSID \_ PortableDeviceFTM** , in quanto in questo modo si elimina l'overhead del marshalling del puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cd5af-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="cd5af-113">**CLSID \_ PortableDevice** è ancora supportato per le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="cd5af-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd5af-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd5af-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd5af-115">**Selezione di un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="cd5af-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



