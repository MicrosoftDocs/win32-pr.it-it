---
description: Enumerazione del contenuto
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerazione del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306647"
---
# <a name="enumerating-content"></a><span data-ttu-id="ca445-103">Enumerazione del contenuto</span><span class="sxs-lookup"><span data-stu-id="ca445-103">Enumerating Content</span></span>

<span data-ttu-id="ca445-104">Il contenuto di un dispositivo (indipendentemente dal fatto che il contenuto sia una cartella, una rubrica, un video o un'immagine ancora) viene chiamato oggetto nell'API WPD.</span><span class="sxs-lookup"><span data-stu-id="ca445-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="ca445-105">A questi oggetti viene fatto riferimento dagli identificatori di oggetto e descritti dalle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca445-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="ca445-106">È possibile enumerare gli oggetti in un dispositivo chiamando i metodi nell' [**interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), l' [**interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)e l' [**interfaccia IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="ca445-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="ca445-107">Nell'applicazione di esempio viene illustrata l'enumerazione del contenuto nella funzione EnumerateAllContent trovata nel modulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="ca445-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="ca445-108">Questa funzione, a sua volta, chiama una funzione RecursiveEnumerate che esamina la gerarchia di oggetti trovati nel dispositivo selezionato e restituisce un identificatore di oggetto per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca445-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="ca445-109">Come indicato, la funzione RecursiveEnumerate recupera un identificatore di oggetto per ogni oggetto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca445-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="ca445-110">L'identificatore dell'oggetto è un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="ca445-110">The object identifier is a string value.</span></span> <span data-ttu-id="ca445-111">Quando l'applicazione recupera questo identificatore, può ottenere informazioni più descrittive sugli oggetti, ad esempio il nome dell'oggetto, l'identificatore per l'elemento padre dell'oggetto e così via.</span><span class="sxs-lookup"><span data-stu-id="ca445-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="ca445-112">Queste informazioni descrittive sono denominate proprietà o metadati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca445-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="ca445-113">L'applicazione può recuperare queste proprietà chiamando membri dell' [**interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span><span class="sxs-lookup"><span data-stu-id="ca445-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="ca445-114">La funzione EnumerateAllContent inizia con il recupero di un puntatore a un' [**interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="ca445-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="ca445-115">Recupera questo puntatore chiamando il metodo [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="ca445-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="ca445-116">Una volta recuperato il puntatore all'interfaccia IPortableDeviceContent, la funzione EnumerateAllContent chiama la funzione RecursiveEnumerate, che esamina la gerarchia di oggetti trovati nel dispositivo specificato e restituisce un identificatore di oggetto per ogni.</span><span class="sxs-lookup"><span data-stu-id="ca445-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="ca445-117">La funzione RecursiveEnumerate inizia con il recupero di un puntatore a un' [**interfaccia IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="ca445-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="ca445-118">Questa interfaccia espone i metodi utilizzati da un'applicazione per spostarsi nell'elenco di oggetti individuati in un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca445-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="ca445-119">In questo esempio, la funzione RecursiveEnumerate chiama il metodo [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) per scorrere l'elenco di oggetti.</span><span class="sxs-lookup"><span data-stu-id="ca445-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="ca445-120">Ogni chiamata al metodo [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) richiede un batch di 10 identificatori.</span><span class="sxs-lookup"><span data-stu-id="ca445-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="ca445-121">(Questo valore è specificato dal \_ numero OGGETTI \_ da \_ richiedere una costante fornita come primo argomento.</span><span class="sxs-lookup"><span data-stu-id="ca445-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ca445-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca445-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca445-123">**Interfaccia IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="ca445-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="ca445-124">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="ca445-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ca445-125">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="ca445-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="ca445-126">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="ca445-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="ca445-127">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="ca445-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



