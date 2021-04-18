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
# <a name="device-events-core-audio-apis"></a>Eventi dispositivo (API principali dell'audio)

Un evento del dispositivo notifica ai client una modifica dello stato di un [dispositivo dell'endpoint audio](audio-endpoint-devices.md) nel sistema. Di seguito sono riportati alcuni esempi di eventi dispositivo:

-   L'utente Abilita o Disabilita un dispositivo endpoint audio da Gestione dispositivi o dal pannello di controllo multimediale di Windows, Mmsys.cpl.
-   L'utente aggiunge una scheda audio al sistema o rimuove una scheda audio dal sistema.
-   L'utente inserisce un dispositivo endpoint audio in un jack audio con rilevamento della presenza di Jack o rimuove un dispositivo endpoint audio da tale Jack.
-   L'utente modifica il [ruolo del dispositivo](device-roles.md) assegnato a un dispositivo.
-   Il valore di una [proprietà di un dispositivo](device-properties.md) viene modificato.

L'aggiunta o la rimozione di una scheda audio genera eventi del dispositivo per tutti i dispositivi dell'endpoint audio che si connettono alla scheda. I primi quattro elementi nell'elenco precedente sono esempi di modifiche allo stato del dispositivo. Per altre informazioni sugli Stati del dispositivo dei dispositivi dell'endpoint audio, [vedere \_ costanti di stato del dispositivo \_ xxx](device-state-xxx-constants.md). Per altre informazioni sul rilevamento della presenza di Jack, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).

Un client può registrarsi per ricevere una notifica quando si verificano eventi del dispositivo. In risposta a queste notifiche, il client può modificare dinamicamente il modo in cui usa un particolare dispositivo oppure selezionare un dispositivo diverso da usare per uno scopo specifico.

Se, ad esempio, in un'applicazione viene riprodotta una traccia audio tramite un set di altoparlanti USB e l'utente disconnette gli altoparlanti dal connettore USB, l'applicazione riceve una notifica degli eventi del dispositivo. In risposta all'evento, se l'applicazione rileva che un set di altoparlanti desktop è connesso alla scheda audio integrata sulla scheda madre del sistema, l'applicazione può riprendere la riproduzione della traccia audio attraverso gli altoparlanti del desktop. In questo esempio, la transizione da altoparlanti USB a altoparlanti desktop viene eseguita automaticamente, senza richiedere all'utente di intervenire in modo esplicito per il reindirizzamento dell'applicazione.

Per eseguire la registrazione per ricevere le notifiche dei dispositivi, un client chiama il metodo [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) . Quando il client non richiede più le notifiche, lo annulla chiamando il metodo [**IMMDeviceEnumerator:: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) . Entrambi i metodi accettano un parametro di input, denominato *pNotify*, che è un puntatore a un'istanza dell'interfaccia [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .

L'interfaccia **IMMNotificationClient** viene implementata da un client. L'interfaccia contiene diversi metodi, ognuno dei quali funge da routine di callback per un determinato tipo di evento del dispositivo. Quando si verifica un evento del dispositivo in un dispositivo endpoint audio, il modulo MMDevice chiama il metodo appropriato nell'interfaccia **IMMNotificationClient** di ogni client attualmente registrato per ricevere le notifiche degli eventi dispositivo. Queste chiamate passano una descrizione dell'evento ai client. Per ulteriori informazioni, vedere [**interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).

Un client registrato per ricevere notifiche degli eventi dispositivo riceverà le notifiche di tutti i tipi di eventi del dispositivo che si verificano in tutti i dispositivi dell'endpoint audio nel sistema. Se un client è interessato solo a determinati tipi di eventi o in determinati dispositivi, i metodi nell'implementazione di **IMMNotificationClient** devono filtrare gli eventi in modo appropriato.

Il Windows SDK fornisce esempi che includono diverse implementazioni per l' [**interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Per altre informazioni, vedere [esempi di SDK che usano le API di base di audio](sdk-samples-that-use-the-core-audio-apis.md).

Nell'esempio di codice seguente viene illustrata una possibile implementazione dell'interfaccia **IMMNotificationClient** :


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



La classe CMMNotificationClient nell'esempio di codice precedente è un'implementazione dell'interfaccia **IMMNotificationClient** . Poiché **IMMNotificationClient** eredita da **IUnknown**, la definizione della classe contiene le implementazioni dei metodi **IUnknown** **AddRef**, **Release** e **QueryInterface**. I metodi pubblici rimanenti nella definizione della classe sono specifici dell'interfaccia **IMMNotificationClient** . Questi metodi sono:

-   **OnDefaultDeviceChanged**, che viene chiamato quando l'utente modifica il ruolo del dispositivo di un dispositivo endpoint audio.
-   **Gli**, che viene chiamato quando l'utente aggiunge un dispositivo endpoint audio al sistema.
-   **OnDeviceRemoved**, che viene chiamato quando l'utente rimuove un dispositivo endpoint audio dal sistema.
-   **OnDeviceStateChanged**, che viene chiamato quando lo stato del dispositivo di un dispositivo dell'endpoint audio viene modificato. Per ulteriori informazioni sugli stati dei dispositivi, vedere [ \_ \_ costanti xxx sullo stato del dispositivo](device-state-xxx-constants.md).
-   **OnPropertyValueChanged**, che viene chiamato quando viene modificato il valore di una proprietà di un dispositivo dell'endpoint audio.

Ognuno di questi metodi accetta un parametro di input, *pwstrDeviceId*, che è un puntatore a una stringa ID endpoint. La stringa identifica il dispositivo dell'endpoint audio in cui si è verificato l'evento del dispositivo.

Nell'esempio di codice precedente, \_ PrintDeviceName è un metodo privato nella classe CMMNotificationClient che stampa il nome descrittivo del dispositivo. \_PrintDeviceName accetta la stringa ID endpoint come parametro di input. Passa la stringa al metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . **GetDevice** crea un oggetto dispositivo endpoint per rappresentare il dispositivo e fornisce l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) a tale oggetto. Successivamente, \_ PrintDeviceName chiama il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per recuperare l' **interfaccia IPropertyStore** nell'archivio delle proprietà del dispositivo. Infine, \_ PrintDeviceName chiama il metodo **IPropertyStore:: GetItem** per ottenere la proprietà nome descrittivo del dispositivo. Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.

Oltre agli eventi del dispositivo, i client possono registrarsi per ricevere notifiche degli eventi di sessione audio e degli eventi del volume di endpoint. Per altre informazioni, vedere [**interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**interfaccia IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



