---
title: Recupero delle proprietà dell'oggetto WPD
description: Recupero delle proprietà dell'oggetto
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c6eba4435b23ef5c637feaca7c2d4ab6b160e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057984"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="42dce-103">Recupero delle proprietà dell'oggetto WPD</span><span class="sxs-lookup"><span data-stu-id="42dce-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="42dce-104">I servizi spesso contengono oggetti figlio che appartengono a uno dei formati supportati da ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="42dce-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="42dce-105">Un servizio contatti, ad esempio, può supportare più oggetti contatto del formato di contatto astratto.</span><span class="sxs-lookup"><span data-stu-id="42dce-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="42dce-106">Ogni oggetto contatto è descritto da proprietà correlate (nome contatto, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="42dce-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="42dce-107">L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può recuperare le proprietà Content-Object supportate da un determinato servizio contatti.</span><span class="sxs-lookup"><span data-stu-id="42dce-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="42dce-108">In questo esempio vengono utilizzate le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="42dce-108">This sample uses the following interfaces.</span></span>



|                                                                      |                                                                                              |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42dce-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="42dce-109">Interface</span></span>                                                            | <span data-ttu-id="42dce-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42dce-110">Description</span></span>                                                                                  |
| [<span data-ttu-id="42dce-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="42dce-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="42dce-112">Recupera l'interfaccia **IPortableDeviceContent2** per accedere ai metodi del servizio supportati.</span><span class="sxs-lookup"><span data-stu-id="42dce-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="42dce-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="42dce-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="42dce-114">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="42dce-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="42dce-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="42dce-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="42dce-116">Recupera i valori della proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42dce-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="42dce-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="42dce-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="42dce-118">Include i valori della proprietà letti per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42dce-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="42dce-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="42dce-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="42dce-120">Contiene i parametri per un determinato metodo.</span><span class="sxs-lookup"><span data-stu-id="42dce-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="42dce-121">Quando l'utente sceglie l'opzione "7" nella riga di comando, l'applicazione richiama il metodo **ReadContentProperties** trovato nel modulo ContentProperties. cpp.</span><span class="sxs-lookup"><span data-stu-id="42dce-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="42dce-122">Questo metodo recupera le quattro proprietà seguenti per l'oggetto contatto specificato.</span><span class="sxs-lookup"><span data-stu-id="42dce-122">This method retrieves the following four properties for the specified contact object.</span></span>



|                              |                                                                                                                                                                                                                  |                                 |                                     |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="42dce-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42dce-123">Property</span></span>                     | <span data-ttu-id="42dce-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42dce-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="42dce-125">Servizi per dispositivi PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="42dce-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="42dce-126">PropertyKey WPD equivalente \_</span><span class="sxs-lookup"><span data-stu-id="42dce-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
| <span data-ttu-id="42dce-127">Identificatore oggetto padre</span><span class="sxs-lookup"><span data-stu-id="42dce-127">Parent-object identifier</span></span>     | <span data-ttu-id="42dce-128">Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="42dce-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="42dce-129">PKEY \_ GenericObj \_ parentID</span><span class="sxs-lookup"><span data-stu-id="42dce-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="42dce-130">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="42dce-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="42dce-131">Nome dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="42dce-131">Object name</span></span>                  | <span data-ttu-id="42dce-132">Stringa che specifica il nome dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="42dce-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="42dce-133">\_Nome GENERICOBJ \_ pkey</span><span class="sxs-lookup"><span data-stu-id="42dce-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="42dce-134">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="42dce-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="42dce-135">Identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="42dce-135">Persistent unique identifier</span></span> | <span data-ttu-id="42dce-136">Stringa che specifica un identificatore univoco per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="42dce-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="42dce-137">Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42dce-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="42dce-138">Per i servizi, deve essere una rappresentazione in forma di stringa di un GUID.</span><span class="sxs-lookup"><span data-stu-id="42dce-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="42dce-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="42dce-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="42dce-140">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="42dce-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="42dce-141">Formato oggetto</span><span class="sxs-lookup"><span data-stu-id="42dce-141">Object format</span></span>                | <span data-ttu-id="42dce-142">Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="42dce-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="42dce-143">PKEY \_ GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="42dce-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="42dce-144">\_formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="42dce-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="42dce-145">ID padre</span><span class="sxs-lookup"><span data-stu-id="42dce-145">Parent ID</span></span>
-   <span data-ttu-id="42dce-146">Nome</span><span class="sxs-lookup"><span data-stu-id="42dce-146">Name</span></span>
-   <span data-ttu-id="42dce-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="42dce-147">PersistentUID</span></span>
-   <span data-ttu-id="42dce-148">Formato</span><span class="sxs-lookup"><span data-stu-id="42dce-148">Format</span></span>

<span data-ttu-id="42dce-149">Si noti che prima di recuperare le proprietà del contenuto, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="42dce-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="42dce-150">Il codice seguente per il metodo **ReadContentProperties** illustra in che modo l'applicazione usa l'interfaccia [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) per recuperare un'interfaccia [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="42dce-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="42dce-151">Passando il PROPERTYKEYS delle proprietà richieste al metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** recupera i valori richiesti e li Visualizza nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="42dce-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="42dce-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42dce-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42dce-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="42dce-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="42dce-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="42dce-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="42dce-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="42dce-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



