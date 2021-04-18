---
description: Richiamare metodi di servizio
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Richiamare metodi di servizio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315546"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="e5a2f-103">Richiamare metodi di servizio</span><span class="sxs-lookup"><span data-stu-id="e5a2f-103">Invoking Service Methods</span></span>

<span data-ttu-id="e5a2f-104">L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può richiamare in modo sincrono i metodi supportati da un determinato servizio contatti.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="e5a2f-105">In questo esempio vengono utilizzate le interfacce seguenti</span><span class="sxs-lookup"><span data-stu-id="e5a2f-105">This sample uses the following interfaces</span></span>



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a2f-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e5a2f-106">Interface</span></span>                                                              | <span data-ttu-id="e5a2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5a2f-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="e5a2f-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e5a2f-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="e5a2f-109">Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceMethods** per richiamare i metodi su un servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="e5a2f-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="e5a2f-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="e5a2f-111">Utilizzato per richiamare un metodo del servizio.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="e5a2f-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e5a2f-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="e5a2f-113">Utilizzato per conservare i parametri del metodo in uscita e i risultati del metodo in arrivo.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="e5a2f-114">Può essere **null** se il metodo non richiede parametri o restituisce alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="e5a2f-115">Quando l'utente sceglie l'opzione "9" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethods** trovato nel modulo ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="e5a2f-116">Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio di contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="e5a2f-117">I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="e5a2f-118">Sono univoche per ogni tipo di servizio e sono rappresentate da un GUID.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="e5a2f-119">Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="e5a2f-120">Le applicazioni eseguono un metodo chiamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="e5a2f-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="e5a2f-121">I metodi del servizio non devono essere confusi con i comandi WPD.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="e5a2f-122">I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="e5a2f-123">I comandi sono predefiniti, raggruppati per categorie, ad esempio, **la \_ categoria WPD \_ comune** e sono rappresentati da una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="e5a2f-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="e5a2f-124">Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="e5a2f-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="e5a2f-125">Per ulteriori informazioni, vedere l'argomento Commands (comandi).</span><span class="sxs-lookup"><span data-stu-id="e5a2f-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="e5a2f-126">Il metodo **InvokeMethods** richiama il metodo [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="e5a2f-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="e5a2f-127">Utilizzando questa interfaccia, vengono richiamati i metodi **BeginSync** e **EndSync** chiamando il metodo [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="e5a2f-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="e5a2f-128">Ogni volta che chiama **Invoke**, l'applicazione fornisce REFGUID per il metodo richiamato.</span><span class="sxs-lookup"><span data-stu-id="e5a2f-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="e5a2f-129">Il codice seguente usa il metodo **InvokeMethods** .</span><span class="sxs-lookup"><span data-stu-id="e5a2f-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e5a2f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5a2f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a2f-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e5a2f-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="e5a2f-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="e5a2f-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="e5a2f-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="e5a2f-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



