---
title: Recupero delle proprietà degli oggetti WPD
description: L'applicazione WpdServiceApiSample illustra come un'applicazione può recuperare le proprietà dell'oggetto contenuto supportate da un determinato servizio Contatti.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404314"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="0fd82-103">Recupero delle proprietà degli oggetti WPD</span><span class="sxs-lookup"><span data-stu-id="0fd82-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="0fd82-104">I servizi contengono spesso oggetti figlio appartenenti a uno dei formati supportati da ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="0fd82-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="0fd82-105">Ad esempio, un servizio Contatti può supportare più oggetti contatto nel formato Contatto astratto.</span><span class="sxs-lookup"><span data-stu-id="0fd82-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="0fd82-106">Ogni oggetto contatto è descritto dalle proprietà correlate (nome del contatto, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="0fd82-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="0fd82-107">L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può recuperare le proprietà dell'oggetto contenuto supportate da un determinato servizio Contatti.</span><span class="sxs-lookup"><span data-stu-id="0fd82-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="0fd82-108">In questo esempio vengono utilizzate le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="0fd82-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="0fd82-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0fd82-109">Interface</span></span> | <span data-ttu-id="0fd82-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fd82-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fd82-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="0fd82-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="0fd82-112">Recupera **l'interfaccia IPortableDeviceContent2** per accedere ai metodi del servizio supportati.</span><span class="sxs-lookup"><span data-stu-id="0fd82-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="0fd82-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="0fd82-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="0fd82-114">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0fd82-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="0fd82-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0fd82-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="0fd82-116">Recupera i valori delle proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fd82-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="0fd82-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0fd82-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="0fd82-118">Contiene i valori delle proprietà letti per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fd82-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="0fd82-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="0fd82-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="0fd82-120">Contiene i parametri per un determinato metodo.</span><span class="sxs-lookup"><span data-stu-id="0fd82-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="0fd82-121">Quando l'utente sceglie l'opzione "7" nella riga di comando, l'applicazione richiama il metodo **ReadContentProperties** disponibile nel modulo ContentProperties.cpp.</span><span class="sxs-lookup"><span data-stu-id="0fd82-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="0fd82-122">Questo metodo recupera le quattro proprietà seguenti per l'oggetto contatto specificato.</span><span class="sxs-lookup"><span data-stu-id="0fd82-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="0fd82-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0fd82-123">Property</span></span>                     | <span data-ttu-id="0fd82-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fd82-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="0fd82-125">PROPERTYKEY di Servizi dispositivi</span><span class="sxs-lookup"><span data-stu-id="0fd82-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="0fd82-126">PROPERTYKEY WPD \_ equivalente</span><span class="sxs-lookup"><span data-stu-id="0fd82-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="0fd82-127">Identificatore dell'oggetto padre</span><span class="sxs-lookup"><span data-stu-id="0fd82-127">Parent-object identifier</span></span>     | <span data-ttu-id="0fd82-128">Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0fd82-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="0fd82-129">PKEY \_ GenericObj \_ ParentID</span><span class="sxs-lookup"><span data-stu-id="0fd82-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="0fd82-130">ID PADRE \_ DELL'OGGETTO WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="0fd82-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="0fd82-131">Nome dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="0fd82-131">Object name</span></span>                  | <span data-ttu-id="0fd82-132">Stringa che specifica il nome dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0fd82-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="0fd82-133">PKEY \_ GenericObj \_ Name</span><span class="sxs-lookup"><span data-stu-id="0fd82-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="0fd82-134">NOME OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="0fd82-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="0fd82-135">Identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="0fd82-135">Persistent unique identifier</span></span> | <span data-ttu-id="0fd82-136">Stringa che specifica un identificatore univoco per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0fd82-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="0fd82-137">Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fd82-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="0fd82-138">Per i servizi, deve essere una rappresentazione di stringa di un GUID.</span><span class="sxs-lookup"><span data-stu-id="0fd82-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="0fd82-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="0fd82-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="0fd82-140">\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="0fd82-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="0fd82-141">Formato oggetto</span><span class="sxs-lookup"><span data-stu-id="0fd82-141">Object format</span></span>                | <span data-ttu-id="0fd82-142">Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un determinato oggetto</span><span class="sxs-lookup"><span data-stu-id="0fd82-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="0fd82-143">PKEY \_ GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="0fd82-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="0fd82-144">FORMATO OGGETTO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="0fd82-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="0fd82-145">ID padre</span><span class="sxs-lookup"><span data-stu-id="0fd82-145">Parent ID</span></span>
-   <span data-ttu-id="0fd82-146">Nome</span><span class="sxs-lookup"><span data-stu-id="0fd82-146">Name</span></span>
-   <span data-ttu-id="0fd82-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="0fd82-147">PersistentUID</span></span>
-   <span data-ttu-id="0fd82-148">Formato</span><span class="sxs-lookup"><span data-stu-id="0fd82-148">Format</span></span>

<span data-ttu-id="0fd82-149">Si noti che prima di recuperare le proprietà del contenuto, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="0fd82-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="0fd82-150">Il codice seguente per il **metodo ReadContentProperties** illustra come l'applicazione usa l'interfaccia [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) per recuperare [**un'interfaccia IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)</span><span class="sxs-lookup"><span data-stu-id="0fd82-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="0fd82-151">Passando le proprietà PROPERTYKEYS delle proprietà richieste al metodo [**IPortableDeviceProperties::GetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **ReadContentProperties** recupera i valori richiesti e li visualizza nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="0fd82-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0fd82-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fd82-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd82-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="0fd82-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="0fd82-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0fd82-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="0fd82-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="0fd82-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



