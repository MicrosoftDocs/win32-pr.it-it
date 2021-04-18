---
description: Proprietà dispositivo
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Proprietà del dispositivo (API audio Core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304423"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="62170-103">Proprietà del dispositivo (API audio Core)</span><span class="sxs-lookup"><span data-stu-id="62170-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="62170-104">Durante il processo di enumerazione dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md), un'applicazione client può interrogare gli oggetti endpoint per le relative proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="62170-105">Le proprietà del dispositivo sono esposte nell'implementazione dell'API MMDevice dell'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="62170-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="62170-106">Dato un riferimento all'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un oggetto endpoint, un client può ottenere un riferimento all'archivio delle proprietà dell'oggetto endpoint chiamando il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .</span><span class="sxs-lookup"><span data-stu-id="62170-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="62170-107">L'oggetto archivio proprietà espone un'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="62170-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="62170-108">I due metodi principali in questa interfaccia sono **IPropertyStore:: GetValue**, che ottiene un valore della proprietà del dispositivo e **IPropertyStore:: SetValue**, che imposta un valore della proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="62170-109">Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="62170-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="62170-110">L'implementazione dell'API MMDevice dell'archivio delle proprietà è diversa dall'oggetto archivio delle proprietà della shell standard.</span><span class="sxs-lookup"><span data-stu-id="62170-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="62170-111">Per modificare il valore di una proprietà, è necessario che l'applicazione client chiami il metodo **IPropertyStore:: SetValue** .</span><span class="sxs-lookup"><span data-stu-id="62170-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="62170-112">Durante questa chiamata, i nuovi valori vengono impostati e scritti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="62170-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="62170-113">Pertanto, non è necessario che l'applicazione chiami il metodo **IPropertyStore:: commit** dopo la chiamata **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="62170-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="62170-114">L'handle per il registro di sistema viene chiuso solo quando il client rilascia il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="62170-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="62170-115">In genere, le applicazioni client di terze parti chiamano il metodo **GetValue** ma **non il metodo SetValue.**</span><span class="sxs-lookup"><span data-stu-id="62170-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="62170-116">Gestione endpoint imposta le proprietà del dispositivo di base per gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="62170-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="62170-117">Gestione endpoint è il componente di Windows Vista responsabile del rilevamento della presenza di dispositivi endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="62170-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="62170-118">Ogni \_ identificatore di proprietà pkey xxx nell'elenco seguente è una costante di tipo **PropertyKey** definito nel file di intestazione Functiondiscoverykeys \_ devpkey. h.</span><span class="sxs-lookup"><span data-stu-id="62170-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="62170-119">Tutti i dispositivi endpoint audio hanno queste tre proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="62170-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62170-120">Property</span></span>                                                                         | <span data-ttu-id="62170-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62170-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62170-122">**PKEY \_ deviceinterface \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="62170-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="62170-123">Nome descrittivo della scheda audio a cui è collegato il dispositivo dell'endpoint (ad esempio, "scheda audio XYZ").</span><span class="sxs-lookup"><span data-stu-id="62170-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="62170-124">Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="62170-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="62170-125">**\_DeviceDesc del dispositivo pkey \_**</span><span class="sxs-lookup"><span data-stu-id="62170-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="62170-126">Descrizione del dispositivo dell'endpoint (ad esempio, "Speakers").</span><span class="sxs-lookup"><span data-stu-id="62170-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="62170-127">Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene la descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="62170-128">**PKEY \_ Device \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="62170-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="62170-129">Nome descrittivo del dispositivo dell'endpoint (ad esempio, "altoparlanti (scheda audio XYZ)").</span><span class="sxs-lookup"><span data-stu-id="62170-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="62170-130">Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="62170-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="62170-131">Alcuni dispositivi dell'endpoint audio potrebbero avere proprietà aggiuntive che non vengono visualizzate nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="62170-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="62170-132">Per ulteriori informazioni sulle proprietà aggiuntive, vedere [proprietà dell'endpoint audio](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="62170-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="62170-133">Per ulteriori informazioni su **PropertyKey**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="62170-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="62170-134">Nell'esempio di codice seguente vengono stampati i nomi visualizzati di tutti i dispositivi dell'endpoint di rendering audio nel sistema:</span><span class="sxs-lookup"><span data-stu-id="62170-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="62170-135">La macro non riuscita nell'esempio di codice precedente viene definita nel file di intestazione Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="62170-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="62170-136">Nell'esempio di codice precedente, il corpo del ciclo **for** nella funzione PrintEndpointNames chiama il metodo [**IMMDevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere la [stringa dell'ID endpoint](endpoint-id-strings.md) per il dispositivo dell'endpoint audio rappresentato dall'istanza dell'interfaccia **IMMDevice** .</span><span class="sxs-lookup"><span data-stu-id="62170-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="62170-137">La stringa identifica in modo univoco il dispositivo rispetto a tutti gli altri dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="62170-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="62170-138">Un client può usare la stringa dell'ID endpoint per creare un'istanza del dispositivo dell'endpoint audio in un secondo momento o in un processo diverso chiamando il metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="62170-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="62170-139">I client devono trattare il contenuto della stringa dell'ID dell'endpoint come opaco.</span><span class="sxs-lookup"><span data-stu-id="62170-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="62170-140">Ovvero i client non devono tentare di analizzare il contenuto della stringa per ottenere informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="62170-141">Il motivo è che il formato della stringa non è definito e può cambiare da un'implementazione dell'API MMDevice a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="62170-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="62170-142">I nomi dei dispositivi descrittivi e le stringhe di ID endpoint ottenute dalla funzione PrintEndpointNames nell'esempio di codice precedente sono identici ai nomi dei dispositivi descrittivi e alle stringhe di ID endpoint fornite da DirectSound durante l'enumerazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62170-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="62170-143">Per altre informazioni, vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="62170-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="62170-144">Nell'esempio di codice precedente, la funzione PrintEndpointNames chiama la funzione **CoCreateInstance** per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="62170-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="62170-145">A meno che il programma chiamante abbia precedentemente chiamato la funzione **CoInitialize** o **CoInitializeEx** per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="62170-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="62170-146">Per ulteriori informazioni su **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="62170-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="62170-147">Per altre informazioni sulle interfacce **IMMDeviceEnumerator**, **IMMDeviceCollection** e **IMMDevice** , vedere [API MMDevice](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="62170-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62170-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62170-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62170-149">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="62170-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



