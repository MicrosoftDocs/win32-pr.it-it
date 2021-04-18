---
description: Recupero degli identificatori di oggetti funzionali per un dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recupero degli identificatori di oggetti funzionali per un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314433"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="0121d-103">Recupero degli identificatori di oggetti funzionali per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="0121d-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="0121d-104">Come indicato nell'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , i dispositivi portatili Windows possono supportare una o più categorie funzionali.</span><span class="sxs-lookup"><span data-stu-id="0121d-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="0121d-105">Una determinata categoria funzionale può supportare uno o più oggetti funzionali.</span><span class="sxs-lookup"><span data-stu-id="0121d-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="0121d-106">Ad esempio, la categoria archiviazione può supportare tre oggetti di archiviazione funzionale, ciascuno dei quali è identificato da una stringa identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="0121d-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="0121d-107">Il primo oggetto di archiviazione può quindi essere identificato dalla stringa "storage1", la seconda dalla stringa "Storage2" e la terza dalla stringa "Storage3".</span><span class="sxs-lookup"><span data-stu-id="0121d-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="0121d-108">La funzione ListFunctionalObjects nel modulo DeviceCapabilities. cpp illustra il recupero dei tipi di contenuto per le categorie funzionali supportate da un dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="0121d-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="0121d-109">L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0121d-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="0121d-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0121d-110">Interface</span></span>                                                                                      | <span data-ttu-id="0121d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0121d-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="0121d-112">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0121d-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="0121d-113">Fornisce l'accesso ai metodi di recupero della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="0121d-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="0121d-114">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="0121d-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="0121d-115">Utilizzato per enumerare e archiviare i dati della categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="0121d-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="0121d-116">Il codice trovato nella funzione ListFunctionalObjects è quasi identico al codice trovato nella funzione ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="0121d-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="0121d-117">Vedere l'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) . L'unica differenza è rappresentata dalla chiamata al metodo [**IPortableDeviceCapabilities:: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , che viene visualizzato all'interno del ciclo che scorre le categorie funzionali.</span><span class="sxs-lookup"><span data-stu-id="0121d-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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



## <a name="related-topics"></a><span data-ttu-id="0121d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0121d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0121d-119">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="0121d-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="0121d-120">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0121d-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="0121d-121">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="0121d-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="0121d-122">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="0121d-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



