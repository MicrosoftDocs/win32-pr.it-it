---
description: Recupero delle funzionalità di rendering supportate da un dispositivo
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Recupero delle funzionalità di rendering supportate da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349341"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="2a035-103">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="2a035-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="2a035-104">I dispositivi portatili Windows che supportano la categoria funzionale informazioni di rendering ( \_ informazioni di rendering della categoria funzionale WPD \_ \_ \_ ) restituiranno informazioni sul rendering quando vengono sottoposte a query.</span><span class="sxs-lookup"><span data-stu-id="2a035-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="2a035-105">Le informazioni di rendering descrivono i requisiti e le restrizioni imposte per le applicazioni che tentano di scrivere contenuto in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a035-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="2a035-106">La funzione ListRenderingCapabilityInformation, la funzione helper SupportsFunctionalCategory e la funzione helper ReadProfileInformationProperties nel modulo DeviceCapabilities. cpp illustrano il recupero delle funzionalità di rendering per un dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="2a035-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="2a035-107">L'applicazione può recuperare le funzionalità di rendering supportate da un dispositivo usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2a035-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2a035-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="2a035-108">Interface</span></span>                                                                                      | <span data-ttu-id="2a035-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a035-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="2a035-110">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2a035-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="2a035-111">Consente di accedere all'interfaccia IPortableDeviceProperties.</span><span class="sxs-lookup"><span data-stu-id="2a035-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="2a035-112">**Interfaccia IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="2a035-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="2a035-113">Fornisce l'accesso ai metodi specifici della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a035-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="2a035-114">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="2a035-115">Utilizzato per archiviare le chiavi di proprietà del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a035-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="2a035-116">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="2a035-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="2a035-117">Utilizzato per archiviare i valori delle proprietà per il profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a035-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="2a035-118">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2a035-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="2a035-119">Utilizzato per archiviare i valori delle proprietà per il profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a035-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="2a035-120">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="2a035-121">Utilizzato per archiviare i valori delle proprietà per il profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a035-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="2a035-122">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="2a035-123">Utilizzato per archiviare i valori delle proprietà per il profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a035-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="2a035-124">Una delle prime attività eseguite dall'applicazione di esempio consiste nel determinare se il dispositivo selezionato è in grado di elencare le funzionalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="2a035-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="2a035-125">La funzione helper SupportsFunctionalCategory determina se questo è il caso chiamando la funzione helper ListRenderingCapabilityInformation e passando \_ \_ \_ le informazioni di rendering della categoria funzionale WPD \_ come secondo argomento.</span><span class="sxs-lookup"><span data-stu-id="2a035-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="2a035-126">Se il dispositivo è in grado di elencare le funzionalità di rendering, il passaggio successivo consiste nel recuperare un oggetto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) e richiamare il metodo [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) per recuperare un identificatore di oggetto per l'oggetto di informazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="2a035-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="2a035-127">Il passaggio successivo consiste nell'archiviare l'identificatore dell'oggetto informazioni di rendering appena recuperato in una variabile di stringa (strRenderingInfoObjectID) e quindi chiamare la funzione di supporto ReadProfileInformationProperties.</span><span class="sxs-lookup"><span data-stu-id="2a035-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="2a035-128">La variabile strRenderingInfoObjectID viene passata come secondo argomento alla funzione helper.</span><span class="sxs-lookup"><span data-stu-id="2a035-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="2a035-129">Una delle prime attività eseguite dalla funzione helper consiste nel recuperare un oggetto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , che verrà usato per accedere ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="2a035-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="2a035-130">Successivamente, la funzione helper recupera un oggetto [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , che verrà usato per accedere ai metodi specifici della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a035-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="2a035-131">Il passaggio successivo consiste nel creare un oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) in cui vengono archiviate le chiavi delle proprietà per le informazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="2a035-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="2a035-132">Una volta creato l'oggetto, viene richiamato il metodo [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) per aggiungere le chiavi necessarie.</span><span class="sxs-lookup"><span data-stu-id="2a035-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="2a035-133">È necessario aggiungere queste chiavi in modo che i profili di rendering corrispondenti possano essere recuperati nei passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="2a035-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="2a035-134">Il passaggio successivo consiste nel recuperare i valori delle proprietà dal driver di dispositivo chiamando il metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) .</span><span class="sxs-lookup"><span data-stu-id="2a035-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="2a035-135">Il passaggio successivo consente di recuperare il profilo delle informazioni di rendering e di archiviarlo nell'argomento ppRenderingInfoProfiles.</span><span class="sxs-lookup"><span data-stu-id="2a035-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="2a035-136">Dopo che la funzione helper legge le \_ proprietà dei profili di informazioni di rendering WPD \_ \_ , vengono visualizzati i profili di rendering.</span><span class="sxs-lookup"><span data-stu-id="2a035-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="2a035-137">Questi profili vengono visualizzati dalla funzione helper DisplayRenderingProfile.</span><span class="sxs-lookup"><span data-stu-id="2a035-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="2a035-138">Si noti che poiché i profili di rendering sono statici, l'applicazione può scegliere di leggere i profili e archiviarli localmente, anziché accedere al dispositivo ogni volta che sono necessari i dati.</span><span class="sxs-lookup"><span data-stu-id="2a035-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a035-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a035-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a035-140">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="2a035-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2a035-141">**Interfaccia IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2a035-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="2a035-142">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2a035-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="2a035-143">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="2a035-144">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2a035-145">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="2a035-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="2a035-146">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="2a035-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



