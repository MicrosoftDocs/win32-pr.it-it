---
description: Uso dell'interfaccia IKsControl per accedere alle proprietà audio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Uso dell'interfaccia IKsControl per accedere alle proprietà audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225698"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Uso dell'interfaccia IKsControl per accedere alle proprietà audio

In rari casi, è possibile che un'applicazione audio specializzata debba usare l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) per accedere a determinate funzionalità hardware di una scheda audio che non sono esposte dall' [API DEVICETOPOLOGY](devicetopology-api.md) o dall' [API MMDevice](mmdevice-api.md). L'interfaccia **IKsControl** rende disponibili le proprietà, gli eventi e i metodi dei dispositivi di streaming kernel (KS) per le applicazioni in modalità utente. Di interesse principale per le applicazioni audio sono le proprietà di KS. L'interfaccia **IKsControl** può essere usata in combinazione con l'API DeviceTopology e l'API MMDevice per accedere alle proprietà KS delle schede audio.

L'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) è progettata principalmente per l'uso da parte di fornitori di hardware che scrivono applicazioni del pannello di controllo per gestire l'hardware audio. **IKsControl** è meno utile per le applicazioni audio generiche che non sono collegate a dispositivi hardware specifici. Il motivo è che i fornitori di hardware implementano spesso meccanismi proprietari per accedere alle proprietà audio dei propri dispositivi. Diversamente dall'API DeviceTopology, che nasconde le anomalie dei driver specifiche dell'hardware e fornisce un'interfaccia relativamente uniforme per l'accesso alle proprietà audio, le applicazioni usano **IKsControl** per comunicare direttamente con i driver. Per ulteriori informazioni su **IKsControl**, vedere la documentazione di Windows DDK.

Come illustrato nelle [topologie di dispositivo](device-topologies.md), una sottounità nella topologia di un dispositivo adapter potrebbe supportare una o più delle interfacce di controllo specifiche della funzione visualizzate nella colonna sinistra della tabella seguente. Ogni voce nella colonna a destra della tabella è la proprietà KS che corrisponde all'interfaccia del controllo a sinistra. L'interfaccia di controllo fornisce un comodo accesso alla proprietà. La maggior parte dei driver audio utilizza le proprietà KS per rappresentare le funzionalità di elaborazione specifiche della funzione delle unità secondarie (dette anche nodi KS) nelle topologie delle schede audio. Per ulteriori informazioni sulle proprietà KS e sui nodi KS, vedere la documentazione di Windows DDK.



| Interfaccia di controllo                                          | KS (proprietà)                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ audio \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ audio \_ Bass            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_configurazione del \_ canale \_ audio KSPROPERTY |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | \_ \_ origine Mux audio \_ KSPROPERTY     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | \_ \_ sonorità audio KSPROPERTY        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ audio \_ Mid             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | \_silenziamento audio \_ KSPROPERTY            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ audio \_ demux \_ dest     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ audio \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ audio \_ acuti          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ audio \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ audio \_ dev \_ specifico   |



 

Le topologie di alcune schede audio possono contenere unità secondarie con proprietà KS non elencate nella tabella precedente. Si supponga, ad esempio, che una chiamata al metodo [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) per una determinata unità secondaria recuperi il valore GUID KSNODETYPE \_ tono. Questo GUID del sottotipo indica che l'unità secondaria supporta una o più delle proprietà KS seguenti:

-   KSPROPERTY \_ audio \_ Bass
-   KSPROPERTY \_ audio \_ Mid
-   KSPROPERTY \_ audio \_ acuti
-   KSPROPERTY \_ audio \_ Bass \_ Boost

È possibile accedere alle prime tre proprietà in questo elenco tramite le interfacce di controllo visualizzate nella tabella precedente, ma la proprietà KSPROPERTY \_ audio \_ Bass \_ Boost non ha un'interfaccia di controllo corrispondente nell'API DeviceTopology. Tuttavia, un'applicazione può usare l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) per accedere a questa proprietà, se l'unità secondaria supporta la proprietà.

I passaggi seguenti sono necessari per accedere alla \_ Proprietà KSPROPERTY audio \_ Bass \_ Boost di un'unità secondaria di sottotipo KSNODETYPE \_ Tone:

1.  Chiamare il metodo [**IConnector:: GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) o [**IDeviceTopology:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) per ottenere la stringa dell'ID dispositivo che identifica il dispositivo adapter. Questa stringa è simile a una [stringa ID endpoint](endpoint-id-strings.md), ad eccezione del fatto che identifica un dispositivo adapter anziché un dispositivo endpoint. Per ulteriori informazioni sulla differenza tra un dispositivo adattatore e un dispositivo endpoint, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).
2.  Ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adapter chiamando il metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) con la stringa ID del dispositivo. Questa interfaccia **IMMDevice** è la stessa dell'interfaccia descritta nell' **interfaccia IMMDevice**, ma rappresenta un dispositivo adapter anziché un dispositivo endpoint.
3.  Ottenere l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) sull'unità secondaria chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *IID* impostato su **REFIID** IID \_ IKsControl. Si noti che le interfacce supportate da questo metodo **Activate** , ovvero per un dispositivo adattatore, sono diverse dalle interfacce supportate dal metodo **Activate** per un dispositivo endpoint. In particolare, il metodo **Activate** per un dispositivo adapter supporta **IKsControl**.
4.  Chiamare il metodo [**IPart:: Getlocalid**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) per ottenere l'ID locale della sottounità.
5.  Costruire una richiesta di proprietà KS. L'ID del nodo KS richiesto per la richiesta è contenuto nei 16 bit meno significativi dell'ID locale ottenuto nel passaggio precedente.
6.  Inviare la richiesta di proprietà KS al driver audio chiamando il metodo [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) . Per ulteriori informazioni su questo metodo, vedere la documentazione di Windows DDK.

L'esempio di codice seguente recupera il valore della \_ Proprietà KSPROPERTY audio \_ Bass \_ Boost da un'unità secondaria di sottotipo KSNODETYPE \_ Tone:


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



Nell'esempio di codice precedente, la funzione GetBassBoost accetta i tre parametri seguenti:

-   `pEnumerator` punta all'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) di un enumeratore di endpoint audio.
-   `pPart` punta all'interfaccia [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) di un'unità secondaria che ha un sottotipo di tono KSNODETYPE \_ .
-   `pbValue` punta a una variabile **bool** in cui la funzione scrive il valore della proprietà.

Un programma chiama GetBassBoost solo dopo la chiamata a [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) e determina che il sottotipo dell'unità secondaria è KSNODETYPE \_ tono. Il valore della proprietà è **true** se è abilitata la funzionalità Bass Boost. È **false** se Bass Boost è disabilitato.

All'inizio della funzione GetBassBoost, la chiamata al metodo [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) Ottiene l'interfaccia [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) del dispositivo adattatore che contiene la \_ sottounità tono KSNODETYPE. La chiamata al metodo [**IDeviceTopology:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) recupera la stringa dell'ID dispositivo che identifica il dispositivo adapter. La chiamata al metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) accetta la stringa ID del dispositivo come parametro di input e recupera l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adapter. Successivamente, la chiamata al metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) recupera l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) dell'unità secondaria. Per ulteriori informazioni sull'interfaccia **IKsControl** , vedere la documentazione di Windows DDK.

Successivamente, l'esempio di codice precedente crea una struttura del [**\_ \_ canale audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) che descrive la proprietà Bass-Boost. Nell'esempio di codice viene passato un puntatore alla struttura al metodo [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) , che usa le informazioni nella struttura per recuperare il valore della proprietà. Per ulteriori informazioni sulla struttura **del \_ \_ canale audio KSNODEPROPERTY** e sul metodo **IKsControl:: KsProperty** , vedere la documentazione di Windows DDK.

L'hardware audio in genere assegna uno stato di incremento basso separato a ogni canale in un flusso audio. In linea di base, è possibile abilitare la funzionalità Bass Boost per alcuni canali e disabilitarli per altri. La struttura del [**\_ \_ canale audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contiene un membro del **canale** che specifica il numero del canale. Se un flusso contiene *N* canali, i canali sono numerati da 0 a *n*-1. Nell'esempio di codice precedente viene ottenuto il valore della proprietà Bass-Boost solo per il canale 0. Questa implementazione presuppone implicitamente che le proprietà Bass-Boost per tutti i canali siano impostate in modo uniforme sullo stesso stato. Quindi, la lettura della proprietà Bass-Boost per Channel 0 è sufficiente per determinare il valore della proprietà Bass-Boost per il flusso. Per coerenza con questo presupposto, una funzione corrispondente per impostare la proprietà Bass-Boost imposta tutti i canali sullo stesso valore della proprietà Bass-Boost. Si tratta di convenzioni ragionevoli, ma non tutti i fornitori di hardware le seguono necessariamente. Ad esempio, un fornitore potrebbe fornire un'applicazione del pannello di controllo che Abilita il boosting dei bassi solo per i canali che guidano gli altoparlanti a intervalli completi. Un relatore di un intervallo completo è in grado di riprodurre suoni nell'intervallo completo, da bassi a acuti. In tal caso, il valore della proprietà recuperato dall'esempio di codice precedente potrebbe non rappresentare accuratamente lo stato di Boost Bass del flusso.

I client che utilizzano le interfacce di controllo elencate nella tabella precedente possono chiamare il metodo [**IPart:: RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) per eseguire la registrazione per le notifiche quando cambia il valore di un parametro di controllo. Si noti che l'interfaccia [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) non fornisce un mezzo simile per la registrazione dei client per le notifiche in caso di modifica del valore di una proprietà. Se **IKsControl** supportava le notifiche di modifica delle proprietà, potrebbe informare un'applicazione quando un'altra applicazione ha modificato il valore di una proprietà. Tuttavia, a differenza dei controlli usati più di frequente monitorati tramite le notifiche di [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) , le proprietà gestite da **IKsControl** sono destinate principalmente all'uso da parte dei fornitori di hardware e tali proprietà sono soggette a modifiche solo dalle applicazioni del pannello di controllo scritte dai fornitori. Se un'applicazione deve rilevare le modifiche alle proprietà apportate da un'altra applicazione, può rilevare le modifiche eseguendo periodicamente il polling del valore della proprietà tramite **IKsControl**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 
