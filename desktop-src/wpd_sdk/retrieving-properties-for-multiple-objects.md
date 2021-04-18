---
description: Recupero di proprietà per più oggetti
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recupero di proprietà per più oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317225"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="3ff9f-103">Recupero di proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="3ff9f-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="3ff9f-104">Alcuni driver di dispositivo supportano il recupero di proprietà per più oggetti in una singola chiamata di funzione. Questa operazione viene definita recupero in blocco.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="3ff9f-105">Esistono due tipi di operazioni di recupero bulk: il primo tipo recupera le proprietà per un elenco di oggetti e il secondo tipo recupera le proprietà per tutti gli oggetti di un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="3ff9f-106">Nell'esempio descritto in questa sezione viene illustrata la prima.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="3ff9f-107">L'applicazione può eseguire un recupero bulk usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="3ff9f-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="3ff9f-108">Interface</span></span>                                                                                      | <span data-ttu-id="3ff9f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff9f-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3ff9f-110">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="3ff9f-111">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="3ff9f-112">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="3ff9f-113">Utilizzato per identificare le proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="3ff9f-114">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="3ff9f-115">Utilizzato per determinare se un determinato driver supporta le operazioni bulk.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="3ff9f-116">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="3ff9f-117">Supporta l'operazione di recupero in blocco.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="3ff9f-118">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="3ff9f-119">Utilizzato per archiviare gli identificatori di oggetto per l'operazione bulk.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="3ff9f-120">La funzione ReadContentPropertiesBulk nel modulo ContentProperties. cpp dell'applicazione di esempio illustra un'operazione di recupero in blocco.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="3ff9f-121">La prima attività eseguita in questo esempio è determinare se il driver specificato supporta le operazioni bulk.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="3ff9f-122">Questa operazione viene eseguita chiamando QueryInterface sull'interfaccia IPortableDeviceProperties e verificando l'esistenza di IPortableDevicePropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



<span data-ttu-id="3ff9f-123">Se il driver supporta le operazioni bulk, il passaggio successivo consiste nel creare un'istanza dell' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e specificare le chiavi che corrispondono alle proprietà che l'applicazione recupererà.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="3ff9f-124">Per una descrizione di questo processo, vedere l'argomento [recupero delle proprietà per un singolo oggetto](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff9f-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="3ff9f-125">Una volta specificate le chiavi appropriate, l'applicazione di esempio crea un'istanza dell' [**interfaccia IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="3ff9f-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="3ff9f-126">L'applicazione utilizzerà i metodi in questa interfaccia per tenere traccia dello stato di avanzamento dell'operazione di recupero bulk asincrono.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="3ff9f-127">La funzione successiva chiamata dall'applicazione di esempio è la funzione di supporto CreateIPortableDevicePropVariantCollectionWithAllObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="3ff9f-128">Questa funzione crea un elenco di tutti gli identificatori di oggetto disponibili, ad esempio scopi.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="3ff9f-129">Un'applicazione reale limita l'elenco di identificatori a un particolare set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="3ff9f-130">Ad esempio, un'applicazione può creare un elenco di identificatori per tutti gli oggetti attualmente presenti in una determinata visualizzazione di cartelle.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="3ff9f-131">Come indicato in precedenza, la funzione helper enumera in modo ricorsivo tutti gli oggetti in un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="3ff9f-132">Restituisce questo elenco in un' [**interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene un identificatore per ogni oggetto trovato.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="3ff9f-133">La funzione helper è definita nel modulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



<span data-ttu-id="3ff9f-134">Una volta eseguiti i passaggi precedenti, l'applicazione di esempio avvia il recupero asincrono della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="3ff9f-135">Questa operazione viene eseguita eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ff9f-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="3ff9f-136">Chiamata di IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, che accoda una richiesta per il recupero della proprietà bulk.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="3ff9f-137">Si noti che anche se la richiesta viene accodata, non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="3ff9f-138">Chiamata di IPortableDevicePropertiesBulk:: Start per avviare la richiesta in coda.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="3ff9f-139">Questi passaggi sono illustrati nell'estratto di codice seguente nell'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="3ff9f-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a><span data-ttu-id="3ff9f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ff9f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ff9f-141">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="3ff9f-142">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="3ff9f-143">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="3ff9f-144">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="3ff9f-145">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="3ff9f-146">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="3ff9f-147">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="3ff9f-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



