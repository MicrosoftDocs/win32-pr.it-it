---
description: Eventi dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventi dispositivo (API principali dell'audio)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304424"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="f8eda-103">Eventi dispositivo (API principali dell'audio)</span><span class="sxs-lookup"><span data-stu-id="f8eda-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="f8eda-104">Un evento del dispositivo notifica ai client una modifica dello stato di un [dispositivo dell'endpoint audio](audio-endpoint-devices.md) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f8eda-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="f8eda-105">Di seguito sono riportati alcuni esempi di eventi dispositivo:</span><span class="sxs-lookup"><span data-stu-id="f8eda-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="f8eda-106">L'utente Abilita o Disabilita un dispositivo endpoint audio da Gestione dispositivi o dal pannello di controllo multimediale di Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="f8eda-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="f8eda-107">L'utente aggiunge una scheda audio al sistema o rimuove una scheda audio dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f8eda-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="f8eda-108">L'utente inserisce un dispositivo endpoint audio in un jack audio con rilevamento della presenza di Jack o rimuove un dispositivo endpoint audio da tale Jack.</span><span class="sxs-lookup"><span data-stu-id="f8eda-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="f8eda-109">L'utente modifica il [ruolo del dispositivo](device-roles.md) assegnato a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="f8eda-110">Il valore di una [proprietà di un dispositivo](device-properties.md) viene modificato.</span><span class="sxs-lookup"><span data-stu-id="f8eda-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="f8eda-111">L'aggiunta o la rimozione di una scheda audio genera eventi del dispositivo per tutti i dispositivi dell'endpoint audio che si connettono alla scheda.</span><span class="sxs-lookup"><span data-stu-id="f8eda-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="f8eda-112">I primi quattro elementi nell'elenco precedente sono esempi di modifiche allo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="f8eda-113">Per altre informazioni sugli Stati del dispositivo dei dispositivi dell'endpoint audio, [vedere \_ costanti di stato del dispositivo \_ xxx](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8eda-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="f8eda-114">Per altre informazioni sul rilevamento della presenza di Jack, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f8eda-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="f8eda-115">Un client può registrarsi per ricevere una notifica quando si verificano eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="f8eda-116">In risposta a queste notifiche, il client può modificare dinamicamente il modo in cui usa un particolare dispositivo oppure selezionare un dispositivo diverso da usare per uno scopo specifico.</span><span class="sxs-lookup"><span data-stu-id="f8eda-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="f8eda-117">Se, ad esempio, in un'applicazione viene riprodotta una traccia audio tramite un set di altoparlanti USB e l'utente disconnette gli altoparlanti dal connettore USB, l'applicazione riceve una notifica degli eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="f8eda-118">In risposta all'evento, se l'applicazione rileva che un set di altoparlanti desktop è connesso alla scheda audio integrata sulla scheda madre del sistema, l'applicazione può riprendere la riproduzione della traccia audio attraverso gli altoparlanti del desktop.</span><span class="sxs-lookup"><span data-stu-id="f8eda-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="f8eda-119">In questo esempio, la transizione da altoparlanti USB a altoparlanti desktop viene eseguita automaticamente, senza richiedere all'utente di intervenire in modo esplicito per il reindirizzamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8eda-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="f8eda-120">Per eseguire la registrazione per ricevere le notifiche dei dispositivi, un client chiama il metodo [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="f8eda-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="f8eda-121">Quando il client non richiede più le notifiche, lo annulla chiamando il metodo [**IMMDeviceEnumerator:: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="f8eda-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="f8eda-122">Entrambi i metodi accettano un parametro di input, denominato *pNotify*, che è un puntatore a un'istanza dell'interfaccia [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .</span><span class="sxs-lookup"><span data-stu-id="f8eda-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="f8eda-123">L'interfaccia **IMMNotificationClient** viene implementata da un client.</span><span class="sxs-lookup"><span data-stu-id="f8eda-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="f8eda-124">L'interfaccia contiene diversi metodi, ognuno dei quali funge da routine di callback per un determinato tipo di evento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="f8eda-125">Quando si verifica un evento del dispositivo in un dispositivo endpoint audio, il modulo MMDevice chiama il metodo appropriato nell'interfaccia **IMMNotificationClient** di ogni client attualmente registrato per ricevere le notifiche degli eventi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="f8eda-126">Queste chiamate passano una descrizione dell'evento ai client.</span><span class="sxs-lookup"><span data-stu-id="f8eda-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="f8eda-127">Per ulteriori informazioni, vedere [**interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="f8eda-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="f8eda-128">Un client registrato per ricevere notifiche degli eventi dispositivo riceverà le notifiche di tutti i tipi di eventi del dispositivo che si verificano in tutti i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f8eda-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="f8eda-129">Se un client è interessato solo a determinati tipi di eventi o in determinati dispositivi, i metodi nell'implementazione di **IMMNotificationClient** devono filtrare gli eventi in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f8eda-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="f8eda-130">Il Windows SDK fornisce esempi che includono diverse implementazioni per l' [**interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="f8eda-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="f8eda-131">Per altre informazioni, vedere [esempi di SDK che usano le API di base di audio](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="f8eda-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="f8eda-132">Nell'esempio di codice seguente viene illustrata una possibile implementazione dell'interfaccia **IMMNotificationClient** :</span><span class="sxs-lookup"><span data-stu-id="f8eda-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="f8eda-133">La classe CMMNotificationClient nell'esempio di codice precedente è un'implementazione dell'interfaccia **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="f8eda-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="f8eda-134">Poiché **IMMNotificationClient** eredita da **IUnknown**, la definizione della classe contiene le implementazioni dei metodi **IUnknown** **AddRef**, **Release** e **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f8eda-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="f8eda-135">I metodi pubblici rimanenti nella definizione della classe sono specifici dell'interfaccia **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="f8eda-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="f8eda-136">Questi metodi sono:</span><span class="sxs-lookup"><span data-stu-id="f8eda-136">These methods are:</span></span>

-   <span data-ttu-id="f8eda-137">**OnDefaultDeviceChanged**, che viene chiamato quando l'utente modifica il ruolo del dispositivo di un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="f8eda-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="f8eda-138">**Gli**, che viene chiamato quando l'utente aggiunge un dispositivo endpoint audio al sistema.</span><span class="sxs-lookup"><span data-stu-id="f8eda-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="f8eda-139">**OnDeviceRemoved**, che viene chiamato quando l'utente rimuove un dispositivo endpoint audio dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f8eda-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="f8eda-140">**OnDeviceStateChanged**, che viene chiamato quando lo stato del dispositivo di un dispositivo dell'endpoint audio viene modificato.</span><span class="sxs-lookup"><span data-stu-id="f8eda-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="f8eda-141">Per ulteriori informazioni sugli stati dei dispositivi, vedere [ \_ \_ costanti xxx sullo stato del dispositivo](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8eda-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="f8eda-142">**OnPropertyValueChanged**, che viene chiamato quando viene modificato il valore di una proprietà di un dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="f8eda-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="f8eda-143">Ognuno di questi metodi accetta un parametro di input, *pwstrDeviceId*, che è un puntatore a una stringa ID endpoint.</span><span class="sxs-lookup"><span data-stu-id="f8eda-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="f8eda-144">La stringa identifica il dispositivo dell'endpoint audio in cui si è verificato l'evento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="f8eda-145">Nell'esempio di codice precedente, \_ PrintDeviceName è un metodo privato nella classe CMMNotificationClient che stampa il nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="f8eda-146">\_PrintDeviceName accetta la stringa ID endpoint come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="f8eda-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="f8eda-147">Passa la stringa al metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="f8eda-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="f8eda-148">**GetDevice** crea un oggetto dispositivo endpoint per rappresentare il dispositivo e fornisce l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) a tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8eda-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="f8eda-149">Successivamente, \_ PrintDeviceName chiama il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per recuperare l' **interfaccia IPropertyStore** nell'archivio delle proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="f8eda-150">Infine, \_ PrintDeviceName chiama il metodo **IPropertyStore:: GetItem** per ottenere la proprietà nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8eda-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="f8eda-151">Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f8eda-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="f8eda-152">Oltre agli eventi del dispositivo, i client possono registrarsi per ricevere notifiche degli eventi di sessione audio e degli eventi del volume di endpoint.</span><span class="sxs-lookup"><span data-stu-id="f8eda-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="f8eda-153">Per altre informazioni, vedere [**interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**interfaccia IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="f8eda-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8eda-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8eda-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8eda-155">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="f8eda-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



