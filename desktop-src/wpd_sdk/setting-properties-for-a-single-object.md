---
description: Impostazione delle proprietà per un singolo oggetto
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Impostazione delle proprietà per un singolo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318675"
---
# <a name="setting-properties-for-a-single-object"></a><span data-ttu-id="b0b75-103">Impostazione delle proprietà per un singolo oggetto</span><span class="sxs-lookup"><span data-stu-id="b0b75-103">Setting Properties for a Single Object</span></span>

<span data-ttu-id="b0b75-104">Dopo che l'applicazione ha recuperato un identificatore di oggetto (vedere l'argomento relativo all' [enumerazione del contenuto](enumerating-content.md) ) per un determinato oggetto, può impostare le proprietà di tale oggetto chiamando i metodi nelle interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b0b75-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can set properties for that object by calling methods in the interfaces described in the following table.</span></span>



| <span data-ttu-id="b0b75-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="b0b75-105">Interface</span></span>                                                                | <span data-ttu-id="b0b75-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0b75-106">Description</span></span>                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b75-107">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b0b75-107">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="b0b75-108">Utilizzato per determinare se una determinata proprietà può essere scritta e inviare l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b0b75-108">Used to determine whether a given property can be written and to send the write operation.</span></span>                                                                  |
| [<span data-ttu-id="b0b75-109">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b0b75-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="b0b75-110">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b0b75-110">Provides access to the content-specific methods.</span></span>                                                                                                            |
| [<span data-ttu-id="b0b75-111">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b0b75-111">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="b0b75-112">Utilizzato per contenere i valori da scrivere, determinare i risultati dell'operazione di scrittura e recuperare gli attributi delle proprietà (quando si determina la funzionalità di scrittura).</span><span class="sxs-lookup"><span data-stu-id="b0b75-112">Used to hold the values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="b0b75-113">Le applicazioni impostano le proprietà su un oggetto creando innanzitutto un contenitore di proprietà che specifica i nuovi valori usando l' [**interfaccia IPortableDeviceValues**](iportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="b0b75-113">Applications set properties on an object by first creating a property bag that specifies the new values using the [**IPortableDeviceValues interface**](iportabledevicevalues.md).</span></span> <span data-ttu-id="b0b75-114">Una volta creato il contenitore delle proprietà, un'applicazione imposta tali proprietà chiamando il metodo [**IPortableDeviceProperties:: SetValue**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) .</span><span class="sxs-lookup"><span data-stu-id="b0b75-114">Once the property bag is created, an application sets those properties by calling the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) method.</span></span>

<span data-ttu-id="b0b75-115">La `WriteContentProperties` funzione nel modulo ContentProperties. cpp dell'applicazione di esempio illustra come un'applicazione può impostare una nuova proprietà nome oggetto per un oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="b0b75-115">The `WriteContentProperties` function in the sample application's ContentProperties.cpp module demonstrates how an application could set a new object-name property for a selected object.</span></span>

<span data-ttu-id="b0b75-116">La prima attività eseguita dalla `WriteContentProperties` funzione consiste nel richiedere all'utente di immettere un identificatore di oggetto per l'oggetto per cui l'applicazione scriverà il nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="b0b75-116">The first task accomplished by the `WriteContentProperties` function is to prompt the user to enter an object identifier for the object that the application will write the new name for.</span></span>


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



<span data-ttu-id="b0b75-117">Al termine di questa operazione, l'applicazione recupera l' \_ attributo della proprietà WPD \_ \_ in grado di scrivere un \_ valore per la \_ \_ proprietà nome oggetto WPD per determinare se la proprietà può essere scritta.</span><span class="sxs-lookup"><span data-stu-id="b0b75-117">After this, the application retrieves the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value for the WPD\_OBJECT\_NAME property to determine whether the property can be written.</span></span> <span data-ttu-id="b0b75-118">Si noti che l'applicazione potrebbe impostare qualsiasi proprietà per la quale WPD \_ L' \_ attributo Property \_ può \_ scrivere un valore true.</span><span class="sxs-lookup"><span data-stu-id="b0b75-118">(Note that your application could set any property for which the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value is true.)</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



<span data-ttu-id="b0b75-119">Il passaggio successivo consiste nel richiedere all'utente la nuova stringa del nome.</span><span class="sxs-lookup"><span data-stu-id="b0b75-119">The next step is to prompt the user for the new name string.</span></span> <span data-ttu-id="b0b75-120">Si noti che la chiamata al metodo [**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) crea semplicemente il contenitore delle proprietà. la proprietà effettiva non è stata ancora scritta.</span><span class="sxs-lookup"><span data-stu-id="b0b75-120">(Note that the call to the [**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md) method merely creates the property bag; the actual property has not been written yet.)</span></span>


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



<span data-ttu-id="b0b75-121">Infine, il nuovo valore, specificato dall'utente, viene applicato all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b0b75-121">Finally, the new value, specified by the user, is applied to the object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="b0b75-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0b75-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b75-123">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="b0b75-123">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b0b75-124">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b0b75-124">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="b0b75-125">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="b0b75-125">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="b0b75-126">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b0b75-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="b0b75-127">**Interfaccia IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b0b75-127">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="b0b75-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b0b75-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="b0b75-129">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="b0b75-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



