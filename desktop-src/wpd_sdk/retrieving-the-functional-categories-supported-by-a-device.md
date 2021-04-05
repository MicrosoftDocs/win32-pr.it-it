---
description: Recupero delle categorie funzionali supportate da un dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recupero delle categorie funzionali supportate da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883386"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="2f959-103">Recupero delle categorie funzionali supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="2f959-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="2f959-104">I dispositivi portatili Windows possono supportare una o più categorie funzionali.</span><span class="sxs-lookup"><span data-stu-id="2f959-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="2f959-105">Queste categorie sono descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2f959-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="2f959-106">Category</span><span class="sxs-lookup"><span data-stu-id="2f959-106">Category</span></span>                    | <span data-ttu-id="2f959-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f959-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f959-108">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="2f959-108">Audio capture</span></span>               | <span data-ttu-id="2f959-109">Il dispositivo può essere usato per registrare l'audio.</span><span class="sxs-lookup"><span data-stu-id="2f959-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="2f959-110">Informazioni sul rendering</span><span class="sxs-lookup"><span data-stu-id="2f959-110">Rendering information</span></span>       | <span data-ttu-id="2f959-111">Il dispositivo fornisce dati che descrivono i file multimediali che è in grado di eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="2f959-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="2f959-112">SMS (Short Message Service)</span><span class="sxs-lookup"><span data-stu-id="2f959-112">Short message service (SMS)</span></span> | <span data-ttu-id="2f959-113">Il dispositivo supporta la messaggistica testuale.</span><span class="sxs-lookup"><span data-stu-id="2f959-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="2f959-114">Acquisizione immagini ancora</span><span class="sxs-lookup"><span data-stu-id="2f959-114">Still image capture</span></span>         | <span data-ttu-id="2f959-115">Il dispositivo può essere usato per acquisire le immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="2f959-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="2f959-116">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="2f959-116">Storage</span></span>                     | <span data-ttu-id="2f959-117">Il dispositivo può essere usato per archiviare i file.</span><span class="sxs-lookup"><span data-stu-id="2f959-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="2f959-118">La funzione ListFunctionalCategories nel modulo DeviceCapabilities. cpp illustra il recupero delle categorie funzionali per un dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="2f959-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="2f959-119">L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2f959-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2f959-120">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="2f959-120">Interface</span></span>                                                                                      | <span data-ttu-id="2f959-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f959-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="2f959-122">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2f959-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="2f959-123">Fornisce l'accesso ai metodi di recupero della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="2f959-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="2f959-124">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2f959-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="2f959-125">Utilizzato per enumerare e archiviare i dati della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="2f959-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="2f959-126">La prima attività eseguita dall'applicazione di esempio è il recupero di un oggetto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , che viene usato per recuperare le categorie funzionali sul dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="2f959-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="2f959-127">Le categorie recuperate vengono archiviate in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2f959-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="2f959-128">Il passaggio successivo è l'enumerazione e la visualizzazione delle categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="2f959-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="2f959-129">Il primo passaggio da eseguire per l'applicazione di esempio è recuperare il numero di categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="2f959-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="2f959-130">USA quindi questo conteggio per scorrere l'oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="2f959-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2f959-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f959-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f959-132">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="2f959-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2f959-133">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2f959-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="2f959-134">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2f959-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2f959-135">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="2f959-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



