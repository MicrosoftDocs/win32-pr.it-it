---
description: Recupero dei formati di servizio supportati
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recupero dei formati di servizio supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317222"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="a8596-103">Recupero dei formati di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="a8596-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="a8596-104">L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i formati supportati da un determinato servizio Contatti chiamando i metodi delle interfacce nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a8596-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8596-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a8596-105">Interface</span></span>                                                                            | <span data-ttu-id="a8596-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8596-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="a8596-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a8596-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="a8596-108">Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere agli eventi supportati.</span><span class="sxs-lookup"><span data-stu-id="a8596-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="a8596-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a8596-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="a8596-110">Fornisce l'accesso agli eventi e agli attributi di evento supportati.</span><span class="sxs-lookup"><span data-stu-id="a8596-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="a8596-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a8596-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="a8596-112">Contiene l'elenco dei formati supportati.</span><span class="sxs-lookup"><span data-stu-id="a8596-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="a8596-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a8596-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="a8596-114">Contiene gli attributi per un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a8596-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="a8596-115">Quando l'utente sceglie l'opzione "3" dalla riga di comando, l'applicazione richiama il metodo **ListSupportedFormats** trovato nel modulo ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="a8596-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="a8596-116">Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="a8596-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="a8596-117">In WPD un formato è descritto dagli attributi che specificano il nome e, facoltativamente, il tipo MIME di un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="a8596-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="a8596-118">Questi attributi sono definiti nel file di intestazione thePortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="a8596-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="a8596-119">Per una descrizione degli attributi supportati, vedere l'argomento [attributi](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="a8596-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="a8596-120">Nel caso dell'applicazione di esempio, se WpdServiceSampleDriver è l'unico dispositivo installato, il driver restituisce due formati supportati per il servizio di contatto: "AbstractContactFormat" e "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="a8596-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="a8596-121">Questi formati corrispondono al **\_ \_ \_ \_ contatto astratto del formato oggetto WPD** e al **\_ formato oggetto \_ WPD \_ VCARD2** attributi disponibili in portabledevice. h.</span><span class="sxs-lookup"><span data-stu-id="a8596-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="a8596-122">Due metodi del modulo ServiceCapabilities. cpp supportano il recupero dei formati supportati per il servizio Contacts: **ListSupportedFormats** e **DisplayFormat**.</span><span class="sxs-lookup"><span data-stu-id="a8596-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="a8596-123">Il primo recupera l'identificatore GUID per ogni formato supportato.</span><span class="sxs-lookup"><span data-stu-id="a8596-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="a8596-124">Il secondo converte questo GUID in una stringa intuitiva.</span><span class="sxs-lookup"><span data-stu-id="a8596-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="a8596-125">Il metodo **ListSupportedFormats** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="a8596-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="a8596-126">Utilizzando questa interfaccia, vengono recuperati i formati supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) .</span><span class="sxs-lookup"><span data-stu-id="a8596-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="a8596-127">Il metodo **GetSupportedFormats** Recupera il GUID per ogni formato supportato dal servizio e copia il GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a8596-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="a8596-128">Il codice seguente usa il metodo **ListSupportedFormats** .</span><span class="sxs-lookup"><span data-stu-id="a8596-128">The following code uses the **ListSupportedFormats** method.</span></span>


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="a8596-129">Dopo che il metodo **ListSupportedFormats** Recupera il GUID per ogni formato supportato dal servizio specificato, richiama il metodo **DisplayFormat** per visualizzare il nome descrittivo dello script per ogni formato. ad esempio, "VCard2".</span><span class="sxs-lookup"><span data-stu-id="a8596-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="a8596-130">Il metodo **DisplayFormat** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare una raccolta di attributi per il GUID di formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a8596-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="a8596-131">Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e richiede che il driver restituisca un nome descrittivo per il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a8596-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="a8596-132">Il codice seguente usa il metodo **DisplayFormat** .</span><span class="sxs-lookup"><span data-stu-id="a8596-132">The following code uses the **DisplayFormat** method.</span></span>


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a8596-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8596-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8596-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a8596-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="a8596-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a8596-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="a8596-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a8596-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a8596-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="a8596-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



