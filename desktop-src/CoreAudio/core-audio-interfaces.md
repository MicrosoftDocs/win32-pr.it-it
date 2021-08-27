---
description: 'Questo riferimento alla programmazione per Core Audio SDK include le interfacce seguenti:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfacce audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330bb620b48b865db3db2ab5ea5625b7859588bd8e53e1addbcd8fd8ec9bda6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109471"
---
# <a name="core-audio-interfaces"></a>Interfacce audio di base

Questo riferimento alla programmazione per Core Audio SDK include le interfacce seguenti:

## <a name="mmdevice-api"></a>MMDevice API

L Windows API MmDevice (Multimedia Device) consente ai client audio di individuare i dispositivi [endpoint audio,](audio-endpoint-devices.md)determinarne le funzionalità e creare istanze di driver per tali dispositivi. Il file di intestazione Mmdeviceapi.h definisce le interfacce nell'API MMDevice. Per altre informazioni, vedere [Informazioni sull'API MMDevice.](mmdevice-api.md)

La tabella seguente elenca le interfacce MMDevice disponibili con Core Audio SDK per Windows Vista.



| Interfaccia                                              | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Rappresenta un dispositivo audio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Rappresenta una raccolta di dispositivi audio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Fornisce metodi per enumerare i dispositivi audio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Rappresenta un dispositivo endpoint audio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornisce notifiche quando un dispositivo endpoint audio viene aggiunto o rimosso, quando lo stato o le proprietà di un dispositivo cambiano o quando viene apportata una modifica al ruolo predefinito assegnato a un dispositivo. |



 

## <a name="wasapi"></a>Wasapi

L Windows API (Audio Session API) consente alle applicazioni client di gestire il flusso di dati audio tra l'applicazione e un [dispositivo endpoint audio.](audio-endpoint-devices.md) I file di intestazione Audioclient.h e Audiopolicy.h definiscono le interfacce WASAPI. Per altre informazioni, vedere [Informazioni su WASAPI.](wasapi.md)

La tabella seguente elenca le interfacce WASAPI disponibili con Core Audio SDK per Windows Vista e versioni successive.



| Interfaccia                                                                                    | Descrizione                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Rappresenta un'operazione asincrona che attiva [un'interfaccia WASAPI](wasapi.md) e fornisce un metodo per recuperare i risultati dell'attivazione.<br/> Si applica a partire da Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Fornisce un callback per indicare che l'attivazione di [un'interfaccia WASAPI](wasapi.md) è stata completata.<br/> Si applica a partire da Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Consente a un client di leggere i dati di input da un buffer dell'endpoint di acquisizione.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Consente a un client di creare e inizializzare un flusso audio tra un'applicazione audio e il motore audio o il buffer hardware di un dispositivo endpoint audio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Consente a un client di monitorare la velocità dei dati di un flusso e la posizione corrente nel flusso.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Consente a un client di ottenere la posizione corrente del dispositivo.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Consente a un client di impostare la frequenza di campionamento di un flusso.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Consente a un client di scrivere dati di output in un buffer dell'endpoint di rendering.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Consente a un client di configurare i parametri di controllo per una sessione audio e di monitorare gli eventi nella sessione.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Consente a un client di ottenere informazioni sulla sessione audio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Consente a un client di accedere ai controlli sessione e ai controlli volume sia per sessioni audio tra processi che per sessioni audio specifiche del processo.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Gestisce tutti i sottomix, incluse l'enumerazione e la notifica dei sottomix. Fornisce anche il supporto per l'evasore delle notifiche.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Consente a un client di enumerare le sessioni audio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Consente a un client di controllare e monitorare i livelli di volume per tutti i canali in un flusso audio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Consente a un client di controllare i livelli di volume per tutti i canali nella sessione audio a cui appartiene il flusso.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Consente a un client di controllare il livello del volume master di una sessione audio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Fornisce notifiche di eventi correlati alla sessione, ad esempio modifiche al livello del volume, al nome visualizzato e allo stato della sessione.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Invia notifiche quando si verificano modifiche alla sessione. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Invia notifiche sulle modifiche di sistema in sospeso.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>DeviceTopology API

L'API DeviceTopology offre alle applicazioni client la possibilità di attraversare le topologie hardware funzionali dei dispositivi di rendering e acquisizione audio. Il file di intestazione Devicetopology.h definisce le interfacce nell'API DeviceTopology. Per altre informazioni, vedere [Topologie di dispositivi e](device-topologies.md) API [**DeviceTopology.**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)

La tabella seguente elenca le interfacce DeviceTopology disponibili con Core Audio SDK per Windows Vista e versioni successive.



| Interfaccia                                                           | Descrizione                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Fornisce l'accesso a un controllo del guadagno automatico (AGC) hardware.                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Fornisce l'accesso a un controllo hardware di livello inferiore.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Fornisce l'accesso a un controllo di configurazione del canale hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Fornisce l'accesso a un controllo multiplexer hardware (selettore di input).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Fornisce l'accesso a un controllo di compensazione "sonorità".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Fornisce l'accesso a un controllo hardware a livello di intervallo intermedio.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Fornisce l'accesso a un controllo di disattivazione dell'hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Fornisce l'accesso a un controllo del demultiplexer hardware (selettore di output).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Fornisce l'accesso a un controllo del contatore di picco dell'hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Fornisce l'accesso a un controllo a livello di acuto hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Fornisce l'accesso a un controllo del volume hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Rappresenta un punto di connessione tra componenti.                                                                                                                                                                      |
| [**Interfaccia IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Rappresenta un'interfaccia di controllo su una parte (sottounita o connettore).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Rappresenta una proprietà specifica del dispositivo di un connettore o di una sottounità.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Fornisce l'accesso alla topologia di un dispositivo audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Fornisce informazioni sui formati di dati audio supportati da una connessione I/O configurata dal software (in genere un canale DMA) tra il dispositivo audio e la memoria di sistema.                                        |
| [**IKsDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Fornisce informazioni sui jack o sui connettori interni che forniscono una connessione fisica tra un dispositivo su una scheda audio e un dispositivo endpoint esterno o interno (ad esempio, un microfono o un lettore CD). |
| [**IKsDescriptionDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Fornisce un pratico accesso alla **proprietà KSPROPERTY \_ JACK \_ DESCRIPTION2** di un connettore a un dispositivo endpoint.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Fornisce informazioni sul sink jack se il jack è supportato dall'hardware.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Rappresenta una parte (connettore o sottounità) di una topologia di dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Rappresenta un elenco di parti (connettori e sottounità).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Rappresenta un'interfaccia di controllo di sottounità generica che fornisce il controllo per canale sul livello del volume, in decibel, di un flusso audio o di una banda di frequenza in un flusso audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Rappresenta una sottounità hardware (ad esempio, un controllo a livello di volume) che si trova nel percorso dati tra un client e un dispositivo endpoint audio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Fornisce notifiche quando lo stato di una parte (connettore o sottounità) cambia.                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>EndpointVolume API

L'API EndpointVolume consente ai client specializzati di controllare e monitorare i livelli di volume dei [dispositivi endpoint audio.](audio-endpoint-devices.md) Il file di intestazione Endpointvolume.h definisce le interfacce nell'API EndpointVolume. Per altre informazioni, vedere [**Api EndpointVolume.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)

La tabella seguente elenca le interfacce EndpointVolume disponibili con Core Audio SDK per Windows Vista.



| **Interfaccia**                                                        | **Descrizione**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Rappresenta i controlli del volume nel flusso audio da o verso un dispositivo endpoint audio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Fornisce controlli del volume nel flusso audio da o verso un endpoint del dispositivo.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Rappresenta un contatore di picco nel flusso audio da o verso un dispositivo endpoint audio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornisce notifiche quando il livello del volume o lo stato di muting di un dispositivo endpoint audio cambia. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

