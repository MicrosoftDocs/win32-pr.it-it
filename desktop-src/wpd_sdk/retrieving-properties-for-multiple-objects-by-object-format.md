---
description: Recupero di proprietà per più oggetti in base al formato oggetto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recupero di proprietà per più oggetti in base al formato oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485460"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="a58fc-103">Recupero di proprietà per più oggetti in base al formato oggetto</span><span class="sxs-lookup"><span data-stu-id="a58fc-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="a58fc-104">Oltre al recupero in blocco delle proprietà di una raccolta di identificatori di oggetto, un'applicazione può anche eseguire un recupero in blocco delle proprietà di tutti gli oggetti di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="a58fc-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="a58fc-105">Come nell'esempio precedente, il recupero bulk per un tipo specificato richiede che il driver di dispositivo supporti il recupero in blocco.</span><span class="sxs-lookup"><span data-stu-id="a58fc-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="a58fc-106">L'applicazione può eseguire un recupero bulk usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a58fc-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="a58fc-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a58fc-107">Interface</span></span>                                                                                      | <span data-ttu-id="a58fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a58fc-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a58fc-109">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="a58fc-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="a58fc-110">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a58fc-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="a58fc-111">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="a58fc-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="a58fc-112">Utilizzato per identificare le proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a58fc-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="a58fc-113">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="a58fc-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="a58fc-114">Utilizzato per determinare se un determinato driver supporta le operazioni bulk.</span><span class="sxs-lookup"><span data-stu-id="a58fc-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="a58fc-115">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="a58fc-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="a58fc-116">Supporta l'operazione di recupero in blocco.</span><span class="sxs-lookup"><span data-stu-id="a58fc-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="a58fc-117">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a58fc-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="a58fc-118">Utilizzato per archiviare gli identificatori di oggetto per l'operazione bulk.</span><span class="sxs-lookup"><span data-stu-id="a58fc-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="a58fc-119">La funzione ReadContentPropertiesBulkFilteringFormat nel modulo ContentProperties. cpp dell'applicazione di esempio illustra un'operazione di recupero bulk per oggetti di un tipo o formato specifico.</span><span class="sxs-lookup"><span data-stu-id="a58fc-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="a58fc-120">Il codice trovato nella funzione ReadContentPropertiesBulkFilteringFormat è quasi identico al codice trovato nella funzione ReadContentPropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="a58fc-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="a58fc-121">Per una descrizione completa di questa funzione, vedere l'argomento [recupero delle proprietà per più oggetti](retrieving-properties-for-multiple-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="a58fc-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="a58fc-122">La differenza principale si verifica quando l'operazione viene accodata.</span><span class="sxs-lookup"><span data-stu-id="a58fc-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="a58fc-123">Quando si applica il filtro in base al tipo o al formato, viene chiamato il metodo [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) anziché il metodo [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="a58fc-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="a58fc-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a58fc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a58fc-125">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="a58fc-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="a58fc-126">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="a58fc-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="a58fc-127">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="a58fc-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="a58fc-128">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="a58fc-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="a58fc-129">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="a58fc-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="a58fc-130">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a58fc-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="a58fc-131">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="a58fc-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



