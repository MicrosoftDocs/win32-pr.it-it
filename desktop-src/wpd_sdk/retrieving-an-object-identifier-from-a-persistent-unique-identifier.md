---
description: Recupero di un identificatore di oggetto da un identificatore univoco permanente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recupero di un ID oggetto da un ID univoco persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315537"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="afaef-103">Recupero di un ID oggetto da un ID univoco persistente</span><span class="sxs-lookup"><span data-stu-id="afaef-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="afaef-104">Gli identificatori di oggetto devono essere univoci solo per una determinata sessione del dispositivo. Se l'utente stabilisce una nuova connessione, gli identificatori di una sessione precedente potrebbero non corrispondere agli identificatori per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="afaef-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="afaef-105">Per risolvere questo problema, l'API WPD supporta gli identificatori univoci permanenti (PUID), che vengono mantenuti tra le sessioni del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="afaef-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="afaef-106">In alcuni dispositivi i PUID vengono archiviati in modo nativo con un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="afaef-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="afaef-107">Altri possono generare il PUID in base a un hash dei dati oggetto selezionati.</span><span class="sxs-lookup"><span data-stu-id="afaef-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="afaef-108">Altri possono trattare gli identificatori di oggetto come PUID, in quanto possono garantire che questi identificatori non cambiano mai.</span><span class="sxs-lookup"><span data-stu-id="afaef-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="afaef-109">La funzione GetObjectIdentifierFromPersistentUniqueIdentifier nel modulo ContentProperties. cpp illustra il recupero di un identificatore di oggetto per un determinato PUID.</span><span class="sxs-lookup"><span data-stu-id="afaef-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="afaef-110">L'applicazione può recuperare un identificatore di oggetto per un PUID corrispondente usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="afaef-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="afaef-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="afaef-111">Interface</span></span>                                                                                      | <span data-ttu-id="afaef-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afaef-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afaef-113">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="afaef-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="afaef-114">Fornisce l'accesso al metodo di recupero.</span><span class="sxs-lookup"><span data-stu-id="afaef-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="afaef-115">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="afaef-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="afaef-116">Utilizzato per archiviare sia l'identificatore di oggetto sia l'identificatore univoco permanente corrispondente (PUID).</span><span class="sxs-lookup"><span data-stu-id="afaef-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="afaef-117">La prima attività eseguita dall'applicazione di esempio è ottenere un PUID dall'utente.</span><span class="sxs-lookup"><span data-stu-id="afaef-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="afaef-118">Successivamente, l'applicazione di esempio recupera un oggetto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , che verrà usato per richiamare il metodo [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="afaef-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="afaef-119">Successivamente, viene creato un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che conterrà il PUID fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="afaef-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="afaef-120">Una volta eseguiti i tre passaggi precedenti, l'esempio è pronto per recuperare l'identificatore di oggetto che corrisponde al PUID fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="afaef-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="afaef-121">Questa operazione viene eseguita chiamando il metodo [**IPortableDeviceContent:: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="afaef-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="afaef-122">Prima di chiamare questo metodo, l'esempio Inizializza una struttura PROPVARIANT, scrive il PUID fornito dall'utente in questa struttura e lo aggiunge all'oggetto IPortableDevicePropVariantCollection in corrispondenza del quale punta pPersistentUniqueIDs.</span><span class="sxs-lookup"><span data-stu-id="afaef-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="afaef-123">Questo puntatore viene passato come primo argomento al metodo GetObjectIDsFromPersistentUniqueIDs.</span><span class="sxs-lookup"><span data-stu-id="afaef-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="afaef-124">Il secondo argomento di GetObjectIDsFromPersistentUniqueIDs è un oggetto IPortableDevicePropVariantCollection che riceve l'identificatore dell'oggetto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="afaef-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="afaef-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afaef-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afaef-126">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="afaef-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="afaef-127">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="afaef-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="afaef-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="afaef-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="afaef-129">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="afaef-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



