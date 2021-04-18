---
description: Recupero dei tipi di contenuto supportati da un dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recupero dei tipi di contenuto supportati da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315534"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="5e409-103">Recupero dei tipi di contenuto supportati da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="5e409-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="5e409-104">Come indicato nell'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , i dispositivi portatili Windows possono supportare una o più categorie funzionali.</span><span class="sxs-lookup"><span data-stu-id="5e409-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="5e409-105">Una determinata categoria funzionale può supportare uno o più tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="5e409-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="5e409-106">Ad esempio, la categoria archiviazione può supportare tipi di contenuto di cartelle, audio e immagini.</span><span class="sxs-lookup"><span data-stu-id="5e409-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="5e409-107">Per una descrizione dei tipi di contenuto supportati da WPD, vedere l' [**argomento \_ tipo di contenuto WPD \_ \_ All**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="5e409-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="5e409-108">La funzione ListSupportedContentTypes nel modulo DeviceCapabilities. cpp illustra il recupero dei tipi di contenuto per le categorie funzionali supportate da un dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="5e409-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="5e409-109">L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5e409-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="5e409-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="5e409-110">Interface</span></span>                                                                                      | <span data-ttu-id="5e409-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e409-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="5e409-112">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5e409-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="5e409-113">Fornisce l'accesso ai metodi di recupero della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="5e409-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="5e409-114">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="5e409-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="5e409-115">Utilizzato per enumerare e archiviare i dati della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="5e409-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="5e409-116">Il codice trovato nella funzione ListSupportedContentTypes è quasi identico al codice trovato nella funzione ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="5e409-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="5e409-117">Vedere l'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) . L'unica differenza è rappresentata dalla chiamata al metodo [**IPortableDeviceCapabilities:: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , che viene visualizzato all'interno del ciclo che scorre le categorie funzionali.</span><span class="sxs-lookup"><span data-stu-id="5e409-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5e409-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e409-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e409-119">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="5e409-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="5e409-120">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5e409-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="5e409-121">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="5e409-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="5e409-122">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="5e409-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



