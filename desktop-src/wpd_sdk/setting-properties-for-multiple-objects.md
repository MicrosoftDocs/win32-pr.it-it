---
description: Impostazione delle proprietà per più oggetti
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Impostazione delle proprietà per più oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316375"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="faf32-103">Impostazione delle proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="faf32-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="faf32-104">Alcuni driver di dispositivo supportano l'impostazione di proprietà per più oggetti in una singola chiamata di funzione. questa operazione viene definita scrittura in blocco.</span><span class="sxs-lookup"><span data-stu-id="faf32-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="faf32-105">L'applicazione può eseguire una scrittura bulk usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="faf32-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="faf32-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="faf32-106">Interface</span></span>                                                                                      | <span data-ttu-id="faf32-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf32-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="faf32-108">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="faf32-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="faf32-109">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="faf32-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="faf32-110">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="faf32-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="faf32-111">Fornisce l'accesso ai metodi specifici della proprietà.</span><span class="sxs-lookup"><span data-stu-id="faf32-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="faf32-112">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="faf32-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="faf32-113">Supporta l'operazione di scrittura bulk.</span><span class="sxs-lookup"><span data-stu-id="faf32-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="faf32-114">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="faf32-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="faf32-115">Utilizzato per archiviare gli identificatori di oggetto per l'operazione bulk.</span><span class="sxs-lookup"><span data-stu-id="faf32-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="faf32-116">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="faf32-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="faf32-117">Utilizzato per identificare le proprietà da scrivere.</span><span class="sxs-lookup"><span data-stu-id="faf32-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="faf32-118">La `WriteContentPropertiesBulk` funzione nel modulo ContentProperties. cpp dell'applicazione di esempio illustra un'operazione di scrittura bulk.</span><span class="sxs-lookup"><span data-stu-id="faf32-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="faf32-119">La prima attività eseguita in questo esempio è determinare se il driver specificato supporta le operazioni bulk.</span><span class="sxs-lookup"><span data-stu-id="faf32-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="faf32-120">Questa operazione viene eseguita chiamando QueryInterface su un oggetto **IPortableDeviceProperties** e verificando l'esistenza di **IPortableDevicePropertiesBulk**.</span><span class="sxs-lookup"><span data-stu-id="faf32-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
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



<span data-ttu-id="faf32-121">L'attività successiva comporta la creazione di un oggetto **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="faf32-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="faf32-122">Si tratta dell'oggetto che contiene i valori delle proprietà che verrà scritto dall'esempio.</span><span class="sxs-lookup"><span data-stu-id="faf32-122">This is the object that contains the property values that the sample will write.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="faf32-123">Successivamente, l'esempio crea un'istanza dell' [**interfaccia IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="faf32-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="faf32-124">L'applicazione utilizzerà i metodi in questa interfaccia per tenere traccia dello stato di avanzamento dell'operazione di scrittura bulk asincrona.</span><span class="sxs-lookup"><span data-stu-id="faf32-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="faf32-125">La funzione successiva chiamata dall'applicazione di esempio è la `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` funzione di supporto.</span><span class="sxs-lookup"><span data-stu-id="faf32-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="faf32-126">Questa funzione enumera in modo ricorsivo tutti gli oggetti in un determinato dispositivo e restituisce un' [**interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene un identificatore per ogni oggetto trovato.</span><span class="sxs-lookup"><span data-stu-id="faf32-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="faf32-127">Questa funzione è definita nel modulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="faf32-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="faf32-128">L'oggetto **IPortableDevicePropVariantCollection** include una raccolta di valori **PROPVARIANT** indicizzati dello stesso VARTYPE.</span><span class="sxs-lookup"><span data-stu-id="faf32-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="faf32-129">In questo caso, questi valori contengono un identificatore di oggetto specificato per ogni oggetto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="faf32-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="faf32-130">Gli identificatori di oggetto e le rispettive proprietà Name vengono archiviati in un oggetto [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="faf32-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="faf32-131">Le proprietà Name sono organizzate in modo che al primo oggetto venga assegnata una proprietà Name di "NewName0", al secondo oggetto viene assegnata una proprietà Name di "NewName1" e così via.</span><span class="sxs-lookup"><span data-stu-id="faf32-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="faf32-132">Nell'esempio seguente viene illustrato il modo in cui l'oggetto **IPortableDeviceValuesCollection** è stato inizializzato con gli identificatori di oggetto e le nuove stringhe del nome.</span><span class="sxs-lookup"><span data-stu-id="faf32-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



<span data-ttu-id="faf32-133">Quando l'esempio crea l'oggetto **IPortableDeviceValuesCollection** che contiene le coppie di identificatori di oggetto e nomi, può iniziare l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="faf32-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="faf32-134">L'operazione di scrittura asincrona inizia quando l'esempio chiama il metodo [**IPortableDevicePropertiesBulk:: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="faf32-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="faf32-135">Questo metodo notifica al driver che un'operazione bulk sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="faf32-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="faf32-136">Successivamente, l'esempio chiama il metodo [**IPortableDeviceBulk:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) per iniziare a scrivere effettivamente i nuovi valori di nome.</span><span class="sxs-lookup"><span data-stu-id="faf32-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
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
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



<span data-ttu-id="faf32-137">Si noti che l'esempio attende un lungo periodo di tempo infinito per il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="faf32-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="faf32-138">Se si trattasse di un'applicazione di produzione, è necessario modificare il codice.</span><span class="sxs-lookup"><span data-stu-id="faf32-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faf32-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faf32-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf32-140">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="faf32-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="faf32-141">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="faf32-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="faf32-142">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="faf32-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="faf32-143">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="faf32-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="faf32-144">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="faf32-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="faf32-145">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="faf32-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



