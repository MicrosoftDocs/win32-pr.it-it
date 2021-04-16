---
description: Recupero degli eventi supportati da un dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recupero degli eventi supportati da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530252"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="1c80f-103">Recupero degli eventi supportati da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="1c80f-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="1c80f-104">Alcuni driver WPD supportano la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="1c80f-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="1c80f-105">Ciò significa che un'applicazione può eseguire la registrazione con il driver per ricevere una notifica quando si verifica un'azione specifica.</span><span class="sxs-lookup"><span data-stu-id="1c80f-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="1c80f-106">Ad esempio, un'applicazione può registrarsi per ricevere una notifica quando un oggetto viene aggiunto o rimosso.</span><span class="sxs-lookup"><span data-stu-id="1c80f-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="1c80f-107">Sono disponibili dieci eventi predefiniti che possono essere monitorati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c80f-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="1c80f-108">descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1c80f-108">They are described in the following table.</span></span>



| <span data-ttu-id="1c80f-109">Event</span><span class="sxs-lookup"><span data-stu-id="1c80f-109">Event</span></span>                       | <span data-ttu-id="1c80f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c80f-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c80f-111">Funzionalità del dispositivo aggiornate</span><span class="sxs-lookup"><span data-stu-id="1c80f-111">Device capabilities updated</span></span> | <span data-ttu-id="1c80f-112">Si verifica quando le funzionalità del dispositivo sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="1c80f-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="1c80f-113">Dispositivo rimosso</span><span class="sxs-lookup"><span data-stu-id="1c80f-113">Device removed</span></span>              | <span data-ttu-id="1c80f-114">Si verifica quando il dispositivo viene scollegato.</span><span class="sxs-lookup"><span data-stu-id="1c80f-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="1c80f-115">Reimpostazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1c80f-115">Device reset</span></span>                | <span data-ttu-id="1c80f-116">Si verifica quando il dispositivo è stato reimpostato.</span><span class="sxs-lookup"><span data-stu-id="1c80f-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="1c80f-117">Oggetto aggiunto</span><span class="sxs-lookup"><span data-stu-id="1c80f-117">Object added</span></span>                | <span data-ttu-id="1c80f-118">Si verifica dopo che un nuovo oggetto diventa disponibile nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c80f-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="1c80f-119">Oggetto rimosso</span><span class="sxs-lookup"><span data-stu-id="1c80f-119">Object removed</span></span>              | <span data-ttu-id="1c80f-120">Si verifica dopo che un oggetto è stato rimosso dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c80f-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="1c80f-121">Trasferimento oggetti richiesto</span><span class="sxs-lookup"><span data-stu-id="1c80f-121">Object transfer requested</span></span>   | <span data-ttu-id="1c80f-122">Indica che è stata effettuata una richiesta di trasferimento di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c80f-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="1c80f-123">Oggetto aggiornato</span><span class="sxs-lookup"><span data-stu-id="1c80f-123">Object updated</span></span>              | <span data-ttu-id="1c80f-124">Si verifica dopo l'aggiornamento di un oggetto o dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="1c80f-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="1c80f-125">(I client connessi devono aggiornare la visualizzazione dell'oggetto specificato).</span><span class="sxs-lookup"><span data-stu-id="1c80f-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="1c80f-126">Formato di archiviazione in corso</span><span class="sxs-lookup"><span data-stu-id="1c80f-126">Storage format in progress</span></span>  | <span data-ttu-id="1c80f-127">Si verifica quando viene formattata l'archiviazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c80f-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="1c80f-128">Per un elenco delle costanti associate a questi eventi, vedere l'argomento relativo alle [costanti di evento](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="1c80f-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="1c80f-129">La funzione ListSupportedEvents nel modulo DeviceCapabilities. cpp illustra il recupero degli eventi supportati da un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c80f-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="1c80f-130">L'applicazione può recuperare gli identificatori per gli eventi supportati da un dispositivo usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1c80f-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="1c80f-131">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="1c80f-131">Interface</span></span>                                                                                      | <span data-ttu-id="1c80f-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c80f-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="1c80f-133">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1c80f-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="1c80f-134">Fornisce l'accesso ai metodi di recupero degli eventi supportati.</span><span class="sxs-lookup"><span data-stu-id="1c80f-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="1c80f-135">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1c80f-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="1c80f-136">Utilizzato per enumerare e archiviare i dati della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="1c80f-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="1c80f-137">La prima attività eseguita dall'applicazione di esempio è il recupero di un oggetto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , che viene usato per recuperare gli eventi supportati dal dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="1c80f-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="1c80f-138">Gli eventi supportati vengono recuperati chiamando il metodo [**IPortableDeviceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="1c80f-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="1c80f-139">Questo metodo recupera una raccolta di identificatori di evento per il dispositivo specificato e li archivia in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) a cui punta l'argomento pEvents.</span><span class="sxs-lookup"><span data-stu-id="1c80f-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="1c80f-140">Il passaggio successivo consiste nel recuperare il conteggio degli eventi supportati in modo che l'applicazione possa scorrere l'oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) e recuperare l'identificatore per ogni.</span><span class="sxs-lookup"><span data-stu-id="1c80f-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="1c80f-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c80f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c80f-142">**Costanti evento**</span><span class="sxs-lookup"><span data-stu-id="1c80f-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="1c80f-143">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="1c80f-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="1c80f-144">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1c80f-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="1c80f-145">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1c80f-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="1c80f-146">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="1c80f-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



