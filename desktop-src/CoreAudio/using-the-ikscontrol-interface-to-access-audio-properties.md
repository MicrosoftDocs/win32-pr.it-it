---
description: Uso dell'interfaccia IKsControl per accedere alle proprietà audio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Uso dell'interfaccia IKsControl per accedere alle proprietà audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b763b874730981907d61ed7d4d2f46f4a9b053705b2747064c2505b9c5e90b14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088226"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Uso dell'interfaccia IKsControl per accedere alle proprietà audio

In rari casi, un'applicazione audio specializzata potrebbe dover usare l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) per accedere a determinate funzionalità hardware di una scheda audio non esposte [dall'API DeviceTopology](devicetopology-api.md) o dall'API [MMDevice](mmdevice-api.md). **L'interfaccia IKsControl** rende disponibili le proprietà, gli eventi e i metodi dei dispositivi di streaming del kernel (KS) per le applicazioni in modalità utente. Di particolare interesse per le applicazioni audio sono le proprietà KS. **L'interfaccia IKsControl** può essere usata insieme all'API DeviceTopology e all'API MMDevice per accedere alle proprietà KS delle schede audio.

[**L'interfaccia IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) è destinata principalmente all'uso da parte dei fornitori di hardware che scrivono applicazioni del pannello di controllo per gestire l'hardware audio. **IKsControl è** meno utile per applicazioni audio per utilizzo generico che non sono legate a particolari dispositivi hardware. Il motivo è che i fornitori di hardware spesso implementano meccanismi proprietari per accedere alle proprietà audio dei propri dispositivi. A differenza dell'API DeviceTopology, che nasconde i dettagli dei driver specifici dell'hardware e fornisce un'interfaccia relativamente uniforme per l'accesso alle proprietà audio, le applicazioni usano **IKsControl** per comunicare direttamente con i driver. Per altre informazioni su **IKsControl,** vedere la documentazione Windows DDK.

Come descritto in [Topologie](device-topologies.md)di dispositivi , una sottounità nella topologia di un dispositivo adapter potrebbe supportare una o più interfacce di controllo specifiche della funzione visualizzate nella colonna sinistra della tabella seguente. Ogni voce nella colonna di destra della tabella è la proprietà KS che corrisponde all'interfaccia di controllo a sinistra. L'interfaccia di controllo fornisce un comodo accesso alla proprietà . La maggior parte dei driver audio usa le proprietà KS per rappresentare le funzionalità di elaborazione specifiche delle funzioni delle sottounità (note anche come nodi KS) nelle topologie delle relative schede audio. Per altre informazioni sulle proprietà KS e sui nodi KS, vedere la documentazione Windows DDK.



| Interfaccia di controllo                                          | KS - proprietà                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ AUDIO \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ AUDIO \_ BASS            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | KSPROPERTY \_ AUDIO \_ CHANNEL \_ CONFIG |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | ORIGINE \_ MUX AUDIO \_ KSPROPERTY \_     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | VOLUME AUDIO \_ KSPROPERTY \_        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ AUDIO \_ MID             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | KSPROPERTY \_ AUDIO \_ MUTE            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ AUDIO \_ DEMUX \_ DEST     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ AUDIO \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ AUDIO \_ TREBLE          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ AUDIO \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ AUDIO \_ DEV \_ SPECIFIC   |



 

Le topologie di alcune schede audio possono contenere sottounità con proprietà KS non elencate nella tabella precedente. Si supponga, ad esempio, che una chiamata al metodo [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) per una determinata sottounità recuperi il valore GUID KSNODETYPE \_ TONE. Questo GUID del sottotipo indica che la sottounità supporta una o più delle proprietà KS seguenti:

-   KSPROPERTY \_ AUDIO \_ BASS
-   KSPROPERTY \_ AUDIO \_ MID
-   KSPROPERTY \_ AUDIO \_ TREBLE
-   KSPROPERTY \_ AUDIO \_ BASS \_ BOOST

Le prime tre proprietà di questo elenco sono accessibili tramite le interfacce di controllo visualizzate nella tabella precedente, ma la proprietà KSPROPERTY AUDIO BASS BOOST non ha un'interfaccia di controllo corrispondente \_ \_ nell'API \_ DeviceTopology. Tuttavia, un'applicazione può usare [**l'interfaccia IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) per accedere a questa proprietà, se la sottounità supporta la proprietà .

I passaggi seguenti sono necessari per accedere alla proprietà KSPROPERTY \_ AUDIO BASS BOOST di una sottounità di \_ \_ sottotipo KSNODETYPE \_ TONE:

1.  Chiamare il [**metodo IConnector::GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) o [**IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) per ottenere la stringa id dispositivo che identifica il dispositivo adapter. Questa stringa è simile a una stringa [di ID endpoint,](endpoint-id-strings.md)ad eccezione del fatto che identifica un dispositivo adapter anziché un dispositivo endpoint. Per altre informazioni sulla differenza tra un dispositivo adapter e un dispositivo endpoint, vedere [Dispositivi endpoint audio](audio-endpoint-devices.md).
2.  Ottenere [**l'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adapter chiamando il metodo [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) con la stringa ID dispositivo. Questa **interfaccia IMMDevice** è la stessa dell'interfaccia descritta in **IMMDevice Interface**, ma rappresenta un dispositivo adapter anziché un dispositivo endpoint.
3.  Ottenere [**l'interfaccia IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) nella sottounità chiamando il metodo [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *iid* impostato su **REFIID** \_ IID IKsControl. Si noti che le interfacce supportate da questo metodo **Activate,** che è per un dispositivo adapter, sono diverse dalle interfacce supportate dal **metodo Activate** per un dispositivo endpoint. In particolare, il **metodo Activate** per un dispositivo adapter supporta **IKsControl**.
4.  Chiamare il [**metodo IPart::GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) per ottenere l'ID locale della sottounità.
5.  Costruire una richiesta di proprietà KS. L'ID nodo KS richiesto per la richiesta è contenuto nei 16 bit meno significativi dell'ID locale ottenuto nel passaggio precedente.
6.  Inviare la richiesta di proprietà KS al driver audio chiamando il [**metodo IKsControl::KsProperty.**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) Per altre informazioni su questo metodo, vedere la documentazione Windows DDK.

L'esempio di codice seguente recupera il valore della proprietà KSPROPERTY AUDIO BASS BOOST da una \_ \_ sottounità di \_ sottotipo KSNODETYPE \_ TONE:


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



Nell'esempio di codice precedente la funzione GetBassBoost accetta i tre parametri seguenti:

-   `pEnumerator` punta [**all'interfaccia IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) di un enumeratore dell'endpoint audio.
-   `pPart` punta [**all'interfaccia IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) di una sottounità con sottotipo KSNODETYPE \_ TONE.
-   `pbValue` punta a una **variabile BOOL** in cui la funzione scrive il valore della proprietà.

Un programma chiama GetBassBoost solo dopo aver chiamato [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) e determina che il sottotipo della sottounità è KSNODETYPE \_ TONE. Il valore della proprietà è **TRUE se** la boost dei bassi è abilitata. È FALSE **se la** boost dei bassi è disabilitata.

All'inizio della funzione GetBassBoost, la chiamata al metodo [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) ottiene [**l'interfaccia IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) del dispositivo adapter che contiene la sottounità KSNODETYPE \_ TONE. La [**chiamata al metodo IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) recupera la stringa id dispositivo che identifica il dispositivo adapter. La chiamata al metodo [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) accetta la stringa ID dispositivo come parametro di input e recupera l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adapter. La chiamata al [**metodo IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) recupera quindi l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) della sottounità. Per altre informazioni **sull'interfaccia IKsControl,** vedere la documentazione Windows DDK.

Successivamente, l'esempio di codice precedente crea una [**struttura KSNODEPROPERTY \_ AUDIO \_ CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) che descrive la proprietà bass-boost. L'esempio di codice passa un puntatore alla struttura al metodo [**IKsControl::KsProperty,**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) che usa le informazioni nella struttura per recuperare il valore della proprietà. Per altre informazioni sulla struttura **KSNODEPROPERTY \_ AUDIO \_ CHANNEL** e sul metodo **IKsControl::KsProperty,** vedere la documentazione Windows DDK.

L'hardware audio assegna in genere uno stato bass-boost separato a ogni canale in un flusso audio. In linea di principio, la boost dei bassi può essere abilitata per alcuni canali e disabilitata per altri. La [**struttura KSNODEPROPERTY \_ AUDIO \_ CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contiene un membro **Channel** che specifica il numero di canale. Se un flusso contiene *N* canali, i canali sono numerati da 0 a *N*- 1. L'esempio di codice precedente ottiene il valore della proprietà bass-boost solo per il canale 0. Questa implementazione presuppone implicitamente che le proprietà bass-boost per tutti i canali siano impostate in modo uniforme sullo stesso stato. Pertanto, la lettura della proprietà bass-boost per il canale 0 è sufficiente per determinare il valore della proprietà bass-boost per il flusso. Per coerenza con questo presupposto, una funzione corrispondente per impostare la proprietà bass-boost imposta tutti i canali sullo stesso valore della proprietà bass-boost. Si tratta di convenzioni ragionevoli, ma non tutti i fornitori di hardware le seguono necessariamente. Ad esempio, un fornitore potrebbe fornire un'applicazione del pannello di controllo che abilita la boost dei bassi solo per i canali che guidano altoparlanti a gamma completa. Un altoparlante a gamma completa è in grado di riprodurre suoni per l'intera gamma, dal basso all'acuto. In tal caso, il valore della proprietà recuperato dall'esempio di codice precedente potrebbe non rappresentare in modo accurato lo stato bass-boost del flusso.

I client che usano le interfacce di controllo elencate nella tabella precedente possono chiamare il metodo [**IPart::RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) per la registrazione per le notifiche quando cambia il valore di un parametro di controllo. Si noti che [**l'interfaccia IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) non offre un modo simile per la registrazione dei client per le notifiche quando cambia il valore di una proprietà. Se **IKsControl supporta** le notifiche di modifica delle proprietà, può informare un'applicazione quando un'altra applicazione modifica un valore di proprietà. Tuttavia, a differenza dei controlli usati più comunemente monitorati tramite notifiche [**IPart,**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) le proprietà gestite da **IKsControl** sono destinate principalmente all'uso da parte dei fornitori di hardware e tali proprietà possono essere modificate solo dalle applicazioni del pannello di controllo scritte dai fornitori. Se un'applicazione deve rilevare le modifiche apportate alle proprietà da un'altra applicazione, può rilevare le modifiche effettuando periodicamente il polling del valore della proprietà tramite **IKsControl**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 
