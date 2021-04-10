---
description: 'Questa guida di riferimento per la programmazione di Core Audio SDK include le interfacce seguenti:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfacce audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eed875bad93bed1625a175bd74b849f139a0140
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125775"
---
# <a name="core-audio-interfaces"></a>Interfacce audio principali

Questa guida di riferimento per la programmazione di Core Audio SDK include le interfacce seguenti:

## <a name="mmdevice-api"></a>API MMDevice

L'API Windows Multimedia Device (MMDevice) consente ai client audio di individuare i [dispositivi dell'endpoint audio](audio-endpoint-devices.md), determinarne le funzionalità e creare istanze di driver per tali dispositivi. Il file di intestazione mmdeviceapi. h definisce le interfacce nell'API MMDevice. Per ulteriori informazioni, vedere [informazioni sull'API MMDevice](mmdevice-api.md).

Nella tabella seguente sono elencate le interfacce MMDevice disponibili con Core Audio SDK per Windows Vista.



| Interfaccia                                              | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Rappresenta un dispositivo audio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Rappresenta una raccolta di dispositivi audio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Fornisce metodi per l'enumerazione dei dispositivi audio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Rappresenta un dispositivo endpoint audio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornisce notifiche quando viene aggiunto o rimosso un dispositivo endpoint audio, quando lo stato o le proprietà di un dispositivo cambiano oppure quando viene apportata una modifica al ruolo predefinito assegnato a un dispositivo. |



 

## <a name="wasapi"></a>WASAPI

L'API di sessione audio (WASAPI) di Windows consente alle applicazioni client di gestire il flusso di dati audio tra l'applicazione e un [dispositivo dell'endpoint audio](audio-endpoint-devices.md). I file di intestazione Audioclient. h e Audiopolicy. h definiscono le interfacce WASAPI. Per ulteriori informazioni, vedere [informazioni su WASAPI](wasapi.md).

Nella tabella seguente sono elencate le interfacce WASAPI disponibili con Core Audio SDK per Windows Vista e versioni successive.



| Interfaccia                                                                                    | Descrizione                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Rappresenta un'operazione asincrona che attiva un'interfaccia [WASAPI](wasapi.md) e fornisce un metodo per recuperare i risultati dell'attivazione.<br/> Si applica a partire da Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Fornisce un callback per indicare che l'attivazione di un'interfaccia [WASAPI](wasapi.md) è stata completata.<br/> Si applica a partire da Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Consente a un client di leggere i dati di input da un buffer dell'endpoint di acquisizione.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Consente a un client di creare e inizializzare un flusso audio tra un'applicazione audio e il motore audio o il buffer hardware di un dispositivo endpoint audio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Consente a un client di monitorare la velocità dei dati di un flusso e la posizione corrente nel flusso.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Consente a un client di ottenere la posizione corrente del dispositivo.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Consente a un client di impostare la frequenza di campionamento di un flusso.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Consente a un client di scrivere i dati di output in un buffer dell'endpoint di rendering.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Consente a un client di configurare i parametri di controllo per una sessione audio e di monitorare gli eventi nella sessione.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Consente a un client di ottenere informazioni sulla sessione audio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Consente a un client di accedere ai controlli di sessione e ai controlli volume per le sessioni audio sia tra processi che specifiche del processo.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Gestisce tutte le sottocombinazioni, incluse le enumerazioni e le notifiche delle sottocombinazioni. Fornisce inoltre il supporto per le notifiche di ducking.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Consente a un client di enumerare le sessioni audio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Consente a un client di controllare e monitorare i livelli di volume per tutti i canali in un flusso audio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Consente a un client di controllare i livelli di volume per tutti i canali della sessione audio a cui appartiene il flusso.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Consente a un client di controllare il livello del volume master di una sessione audio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Fornisce notifiche di eventi correlati alla sessione, ad esempio modifiche a livello di volume, nome visualizzato e stato sessione.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Invia notifiche quando si verificano modifiche alla sessione. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Invia notifiche sulle modifiche di ducking del sistema in sospeso.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>API DeviceTopology

L'API di DeviceTopology offre alle applicazioni client la possibilità di attraversare le topologie hardware funzionali del rendering audio e dei dispositivi di acquisizione. Il file di intestazione Devicetopology. h definisce le interfacce nell'API DeviceTopology. Per altre informazioni, vedere [topologie di dispositivi](device-topologies.md) e [**API DeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

Nella tabella seguente sono elencate le interfacce DeviceTopology disponibili con Core Audio SDK per Windows Vista e versioni successive.



| Interfaccia                                                           | Descrizione                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Consente di accedere a un controllo di guadagno automatico hardware (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Consente di accedere a un controllo a livello di basso hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Consente di accedere a un controllo della configurazione del canale hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Consente di accedere a un controllo multiplexer hardware (selettore input).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Consente di accedere a un controllo di compensazione "sonorità".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Fornisce l'accesso a un controllo a livello di midrange hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Consente di accedere a un controllo di silenziamento hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Consente di accedere a un controllo Demultiplexer hardware (selettore Output).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Consente di accedere a un controllo del contatore di picco hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Fornisce l'accesso a un controllo a livello di hardware acuto.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Consente di accedere a un controllo volume hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Rappresenta un punto di connessione tra i componenti.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Rappresenta un'interfaccia di controllo su una parte (sottounità o connettore).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Rappresenta una proprietà specifica del dispositivo di un connettore o di un'unità secondaria.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Consente di accedere alla topologia di un dispositivo audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Fornisce informazioni sui formati di dati audio supportati da una connessione di I/O configurata dal software (in genere un canale DMA) tra il dispositivo audio e la memoria di sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Fornisce informazioni sulle prese o sui connettori interni che forniscono una connessione fisica tra un dispositivo in una scheda audio e un dispositivo endpoint esterno o interno, ad esempio un microfono o un lettore di CD. |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Consente di accedere facilmente alla proprietà **KSPROPERTY \_ Jack \_ DESCRIPTION2** di un connettore a un dispositivo endpoint.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Fornisce informazioni sul sink Jack se il Jack è supportato dall'hardware.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Rappresenta una parte (connettore o unità secondaria) di una topologia del dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Rappresenta un elenco di parti (connettori e sottounità).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Rappresenta un'interfaccia di controllo di unità secondaria generica che fornisce il controllo per canale sul livello del volume, in decibel, di un flusso audio o di una banda di frequenze in un flusso audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Rappresenta una sottounità hardware (ad esempio, un controllo a livello di volume) che risiede nel percorso dati tra un client e un dispositivo dell'endpoint audio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Fornisce notifiche quando cambia lo stato di una parte (connettore o sottounità).                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>API EndpointVolume

L'API EndpointVolume consente ai client specializzati di controllare e monitorare i livelli di volume dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md). Il file di intestazione Endpointvolume. h definisce le interfacce nell'API EndpointVolume. Per altre informazioni, vedere l' [**API EndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

Nella tabella seguente sono elencate le interfacce EndpointVolume disponibili con Core Audio SDK per Windows Vista.



| **Interfaccia**                                                        | **Descrizione**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Rappresenta i controlli del volume nel flusso audio da o verso un dispositivo endpoint audio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Fornisce i controlli del volume nel flusso audio da o verso un endpoint del dispositivo.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Rappresenta un indicatore di picco nel flusso audio da o verso un dispositivo endpoint audio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornisce notifiche in caso di modifica del livello di volume o di muting di un dispositivo dell'endpoint audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

