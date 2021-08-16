---
description: Eventi del dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventi del dispositivo (API audio core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61538bd7d8d297b52a321f446bb11c3e1365e549a3c2947b55538730c1660c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407029"
---
# <a name="device-events-core-audio-apis"></a>Eventi del dispositivo (API audio core)

Un evento del dispositivo notifica ai client una modifica dello stato di un dispositivo [endpoint audio](audio-endpoint-devices.md) nel sistema. Di seguito sono riportati esempi di eventi del dispositivo:

-   L'utente abilita o disabilita un dispositivo endpoint audio da Gestione dispositivi o dal pannello Windows di controllo multimediale, Mmsys.cpl.
-   L'utente aggiunge una scheda audio al sistema o rimuove una scheda audio dal sistema.
-   L'utente collega un dispositivo endpoint audio a un jack audio con rilevamento della presenza di jack o rimuove un dispositivo endpoint audio da tale jack.
-   L'utente modifica [il ruolo](device-roles.md) del dispositivo assegnato a un dispositivo.
-   Il valore di una [proprietà di un dispositivo cambia.](device-properties.md)

L'aggiunta o la rimozione di un adattatore audio genera eventi del dispositivo per tutti i dispositivi endpoint audio che si connettono all'adattatore. I primi quattro elementi nell'elenco precedente sono esempi di modifiche dello stato del dispositivo. Per altre informazioni sugli stati dei dispositivi endpoint audio, vedere [Costanti DEVICE \_ STATE \_ XXX.](device-state-xxx-constants.md) Per altre informazioni sul rilevamento della presenza di jack, vedere [Dispositivi endpoint audio.](audio-endpoint-devices.md)

Un client può registrarsi per ricevere una notifica quando si verificano eventi del dispositivo. In risposta a queste notifiche, il client può modificare dinamicamente il modo in cui usa un dispositivo specifico o selezionare un dispositivo diverso da usare per uno scopo specifico.

Ad esempio, se un'applicazione riproduce una traccia audio tramite un set di altoparlanti USB e l'utente disconnette gli altoparlanti dal connettore USB, l'applicazione riceve una notifica dell'evento del dispositivo. In risposta all'evento , se l'applicazione rileva che un set di altoparlanti desktop è connesso all'adattatore audio integrato nella scheda madre del sistema, l'applicazione può riprendere la riproduzione della traccia audio tramite gli altoparlanti desktop. In questo esempio, la transizione dagli altoparlanti USB ai parlanti desktop avviene automaticamente, senza richiedere all'utente di intervenire reindirizzando in modo esplicito l'applicazione.

Per eseguire la registrazione per ricevere le notifiche del dispositivo, un client chiama [**il metodo IMMDeviceEnumerator::RegisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) Quando il client non richiede più notifiche, le annulla chiamando il metodo [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) Entrambi i metodi accettano un parametro di input, *denominato pNotify,* che è un puntatore a un'istanza [**dell'interfaccia IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)

**L'interfaccia IMMNotificationClient** viene implementata da un client. L'interfaccia contiene diversi metodi, ognuno dei quali funge da routine di callback per un particolare tipo di evento del dispositivo. Quando si verifica un evento del dispositivo in un dispositivo endpoint audio, il modulo MMDevice chiama il metodo appropriato **nell'interfaccia IMMNotificationClient** di ogni client attualmente registrato per ricevere le notifiche degli eventi del dispositivo. Queste chiamate passano una descrizione dell'evento ai client. Per altre informazioni, vedere [**Interfaccia IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)

Un client registrato per ricevere le notifiche degli eventi del dispositivo riceverà le notifiche di tutti i tipi di eventi del dispositivo che si verificano in tutti i dispositivi endpoint audio nel sistema. Se un client è interessato solo a determinati tipi di evento o a determinati dispositivi, i metodi nell'implementazione **di IMMNotificationClient** devono filtrare gli eventi in modo appropriato.

L Windows SDK fornisce esempi che includono diverse implementazioni per [**l'interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Per altre informazioni, vedere [Sdk Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md)(Esempi di SDK che usano le API audio di base).

L'esempio di codice seguente illustra una possibile implementazione **dell'interfaccia IMMNotificationClient:**


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



La classe CMMNotificationClient nell'esempio di codice precedente è un'implementazione **dell'interfaccia IMMNotificationClient.** Poiché **IMMNotificationClient** eredita da **IUnknown,** la definizione della classe contiene le implementazioni dei metodi **IUnknown** **AddRef,** **Release** e **QueryInterface.** I metodi pubblici rimanenti nella definizione della classe sono specifici **dell'interfaccia IMMNotificationClient.** Questi metodi sono:

-   **OnDefaultDeviceChanged,** che viene chiamato quando l'utente modifica il ruolo del dispositivo di un dispositivo endpoint audio.
-   **OnDeviceAdded**, che viene chiamato quando l'utente aggiunge un dispositivo endpoint audio al sistema.
-   **OnDeviceRemoved,** che viene chiamato quando l'utente rimuove un dispositivo endpoint audio dal sistema.
-   **OnDeviceStateChanged,** che viene chiamato quando lo stato del dispositivo di un dispositivo endpoint audio cambia. Per altre informazioni sugli stati dei dispositivi, vedere [Costanti \_ DEVICE STATE \_ XXX.](device-state-xxx-constants.md)
-   **OnPropertyValueChanged,** che viene chiamato quando cambia il valore di una proprietà di un dispositivo endpoint audio.

Ognuno di questi metodi accetta un parametro di input, *pwstrDeviceId*, che è un puntatore a una stringa di ID endpoint. La stringa identifica il dispositivo endpoint audio in cui si è verificato l'evento del dispositivo.

Nell'esempio di codice precedente PrintDeviceName è un metodo privato nella classe CMMNotificationClient che stampa il nome \_ descrittivo del dispositivo. \_PrintDeviceName accetta la stringa dell'ID endpoint come parametro di input. Passa la stringa al [**metodo IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) **GetDevice crea** un oggetto dispositivo endpoint per rappresentare il dispositivo e fornisce [**l'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) a tale oggetto. \_PrintDeviceName chiama quindi il metodo [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per recuperare l'interfaccia **IPropertyStore** nell'archivio delle proprietà del dispositivo. \_PrintDeviceName chiama infine il metodo **IPropertyStore::GetItem** per ottenere la proprietà del nome descrittivo del dispositivo. Per altre informazioni su **IPropertyStore,** vedere la documentazione Windows SDK.

Oltre agli eventi del dispositivo, i client possono registrarsi per ricevere notifiche di eventi di sessione audio ed eventi del volume di endpoint. Per altre informazioni, vedere [**Interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**Interfaccia IAudioEndpointVolumeCallback.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



