---
description: Recupero di proprietà per un singolo oggetto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recupero di proprietà per un singolo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315535"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="93d07-103">Recupero di proprietà per un singolo oggetto</span><span class="sxs-lookup"><span data-stu-id="93d07-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="93d07-104">Dopo che l'applicazione ha recuperato un identificatore di oggetto (vedere l'argomento relativo all' [enumerazione del contenuto](enumerating-content.md) ) per un determinato oggetto, può recuperare informazioni descrittive sull'oggetto chiamando i metodi nell' [**interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) e l' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="93d07-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="93d07-105">Il metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera un elenco di proprietà specificate per un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="93d07-106">L'applicazione può anche chiamare il metodo GetValues e specificare un valore **null** per il parametro pKeys per recuperare tutte le proprietà per un determinato oggetto. Tuttavia, le prestazioni di questo metodo possono risultare significativamente più lente durante il recupero di tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="93d07-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="93d07-107">Prima che l'applicazione chiami GetValues, tuttavia, deve identificare le proprietà da recuperare impostando le chiavi corrispondenti in un [**oggetto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="93d07-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="93d07-108">L'applicazione identificherà le proprietà di interesse chiamando il metodo [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) e specificando un valore PropertyKey che identifichi ogni proprietà che verrà recuperata.</span><span class="sxs-lookup"><span data-stu-id="93d07-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="93d07-109">La funzione ReadContentProperties nel modulo ContentProperties. cpp dell'applicazione di esempio illustra come sono state recuperate le cinque proprietà per un oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="93d07-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="93d07-110">Nella tabella seguente vengono descritte le proprietà e il valore REFPROPERTYKEY corrispondente.</span><span class="sxs-lookup"><span data-stu-id="93d07-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="93d07-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93d07-111">Property</span></span>                     | <span data-ttu-id="93d07-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93d07-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="93d07-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="93d07-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="93d07-114">Identificatore oggetto padre</span><span class="sxs-lookup"><span data-stu-id="93d07-114">Parent-object identifier</span></span>     | <span data-ttu-id="93d07-115">Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="93d07-116">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93d07-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="93d07-117">Nome dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="93d07-117">Object name</span></span>                  | <span data-ttu-id="93d07-118">Stringa che specifica il nome dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="93d07-119">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93d07-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="93d07-120">Identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="93d07-120">Persistent unique identifier</span></span> | <span data-ttu-id="93d07-121">Stringa che specifica un identificatore univoco per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="93d07-122">(Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="93d07-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="93d07-123">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93d07-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="93d07-124">Formato oggetto</span><span class="sxs-lookup"><span data-stu-id="93d07-124">Object format</span></span>                | <span data-ttu-id="93d07-125">Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="93d07-126">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="93d07-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="93d07-127">Tipo di contenuto Object</span><span class="sxs-lookup"><span data-stu-id="93d07-127">Object content type</span></span>          | <span data-ttu-id="93d07-128">GUID che specifica il tipo di contenuto associato a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="93d07-129">\_tipo di \_ contenuto dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93d07-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="93d07-130">Nell'estratto seguente della funzione ReadContentProperties viene illustrato il modo in cui l'applicazione di esempio utilizza l' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e il metodo [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) per identificare le proprietà recuperate.</span><span class="sxs-lookup"><span data-stu-id="93d07-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="93d07-131">Una volta che l'applicazione di esempio ha impostato le chiavi appropriate, ha chiamato il metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) per recuperare i valori specificati per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="93d07-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="93d07-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93d07-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93d07-133">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="93d07-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="93d07-134">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="93d07-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="93d07-135">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="93d07-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="93d07-136">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="93d07-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



