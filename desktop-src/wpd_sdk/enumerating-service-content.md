---
description: Enumerazione del contenuto del servizio
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Enumerazione del contenuto del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adb949fdec9a0001583b1481ccd50ada1ef1df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226033"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="72a1c-103">Enumerazione del contenuto del servizio</span><span class="sxs-lookup"><span data-stu-id="72a1c-103">Enumerating Service Content</span></span>

<span data-ttu-id="72a1c-104">Quando l'applicazione apre un servizio, può iniziare a eseguire operazioni relative ai servizi.</span><span class="sxs-lookup"><span data-stu-id="72a1c-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="72a1c-105">Nel caso dell'applicazione WpdServicesApiSample, una di queste operazioni è l'enumerazione del contenuto per un determinato servizio di contatti.</span><span class="sxs-lookup"><span data-stu-id="72a1c-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="72a1c-106">Nella tabella seguente vengono descritte le interfacce utilizzate.</span><span class="sxs-lookup"><span data-stu-id="72a1c-106">The following table describes the interfaces used.</span></span>



|                                                                      |                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a1c-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="72a1c-107">Interface</span></span>                                                            | <span data-ttu-id="72a1c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72a1c-108">Description</span></span>                                                                                      |
| [<span data-ttu-id="72a1c-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="72a1c-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="72a1c-110">Utilizzato per recuperare l'interfaccia IPortableDeviceContent2 per accedere al contenuto nel servizio.</span><span class="sxs-lookup"><span data-stu-id="72a1c-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="72a1c-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="72a1c-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="72a1c-112">Utilizzato per recuperare l'interfaccia IEnumPortableDeviceObjectIDs per enumerare gli oggetti nel servizio.</span><span class="sxs-lookup"><span data-stu-id="72a1c-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="72a1c-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="72a1c-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="72a1c-114">Utilizzato per enumerare gli oggetti nel servizio.</span><span class="sxs-lookup"><span data-stu-id="72a1c-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="72a1c-115">Il codice di enumerazione del contenuto si trova nel modulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="72a1c-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="72a1c-116">Questo codice risiede nei metodi **EnumerateAllContent** e **RecursiveEnumerate** .</span><span class="sxs-lookup"><span data-stu-id="72a1c-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="72a1c-117">Il primo metodo chiama quest'ultimo.</span><span class="sxs-lookup"><span data-stu-id="72a1c-117">The former method calls the latter.</span></span>

<span data-ttu-id="72a1c-118">Il metodo **EnumerateContent** accetta un puntatore a un oggetto [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) come relativo parametro.</span><span class="sxs-lookup"><span data-stu-id="72a1c-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="72a1c-119">Questo oggetto corrisponde a un servizio che l'applicazione ha aperto in precedenza quando chiamava il metodo [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .</span><span class="sxs-lookup"><span data-stu-id="72a1c-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="72a1c-120">Il metodo **EnumerateContent** crea un oggetto [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) e passa questo oggetto al metodo [**IPortableDeviceService:: content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) .</span><span class="sxs-lookup"><span data-stu-id="72a1c-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="72a1c-121">Questo metodo, a sua volta, recupera il contenuto a livello di radice del servizio e quindi inizia in modo ricorsivo a recuperare il contenuto trovato sotto la radice.</span><span class="sxs-lookup"><span data-stu-id="72a1c-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="72a1c-122">Il codice seguente corrisponde al metodo **EnumerateContent** .</span><span class="sxs-lookup"><span data-stu-id="72a1c-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="72a1c-123">Il codice seguente corrisponde al metodo **RecursiveEnumerate** .</span><span class="sxs-lookup"><span data-stu-id="72a1c-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="72a1c-124">Il metodo RecursiveEnumerate crea un'istanza di un'interfaccia **IEnumPortableDeviceObjectIDs** per l'oggetto padre fornito e chiama **IEnumPortableDeviceObjectIDs:: Next**, recuperando un batch di oggetti figlio immediati.</span><span class="sxs-lookup"><span data-stu-id="72a1c-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="72a1c-125">Per ogni oggetto figlio, RecursiveEnumerate viene chiamato di nuovo per restituire gli oggetti figlio discendenti e così via.</span><span class="sxs-lookup"><span data-stu-id="72a1c-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
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



## <a name="related-topics"></a><span data-ttu-id="72a1c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72a1c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a1c-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="72a1c-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="72a1c-128">**Interfaccia IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="72a1c-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="72a1c-129">**Interfaccia IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="72a1c-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="72a1c-130">Apertura di un servizio</span><span class="sxs-lookup"><span data-stu-id="72a1c-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="72a1c-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="72a1c-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



