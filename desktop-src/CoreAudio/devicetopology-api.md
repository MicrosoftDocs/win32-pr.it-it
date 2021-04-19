---
description: API DeviceTopology
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: API DeviceTopology
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 472c02cd59ca0cadd922cbe398a768c97cfab73a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323888"
---
# <a name="devicetopology-api"></a>API DeviceTopology

Vedere l' [esempio di Microsoft High Quality Capture DMO](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

L'API di DeviceTopology offre alle applicazioni client la possibilità di attraversare le topologie hardware funzionali del rendering audio e dei dispositivi di acquisizione. Attraverso le interfacce e i metodi nell'API DeviceTopology, i client possono individuare le sottounità funzionali, ad esempio il controllo del volume, che si trovano lungo i percorsi dati che portano da e verso i [dispositivi dell'endpoint audio](audio-endpoint-devices.md). I client possono attraversare le topologie interne dei dispositivi della scheda audio e dei dispositivi dell'endpoint audio e scorrere le connessioni che collegano un dispositivo a un altro. Per altre informazioni, vedere [topologie di dispositivi](device-topologies.md).

Il file di intestazione Devicetopology. h definisce le interfacce nell'API DeviceTopology.

Per accedere alle interfacce API DeviceTopology, un client ottiene prima di tutto un riferimento all'interfaccia [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) per un dispositivo endpoint audio attenendosi alla procedura seguente:

1.  Utilizzando una delle tecniche descritte nell' [**interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), ottenere un riferimento all'interfaccia **IMMDevice** per un dispositivo endpoint audio.
2.  Chiamare il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *IID* impostato su **REFIID** IID \_ IDeviceTopology.

Il client può ottenere riferimenti alle altre interfacce nell'API DeviceTopology chiamando i metodi nell'interfaccia [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) .

L'API DeviceTopology implementa le interfacce seguenti.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Consente di accedere a un controllo di guadagno automatico hardware (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Consente di accedere a un controllo a livello di basso hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Consente di accedere a un controllo della configurazione del canale hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Consente di accedere a un controllo multiplexer hardware (selettore input).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Consente di accedere a un controllo di compensazione "sonorità".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Fornisce l'accesso a un controllo a livello di midrange hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Consente di accedere a un controllo di silenziamento hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Consente di accedere a un controllo Demultiplexer hardware (selettore Output).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Consente di accedere a un controllo del contatore di picco hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Fornisce l'accesso a un controllo a livello di hardware acuto.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Consente di accedere a un controllo volume hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Rappresenta un punto di connessione tra i componenti.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Rappresenta un'interfaccia di controllo su una parte (sottounità o connettore).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Rappresenta una proprietà specifica del dispositivo di un connettore o di un'unità secondaria.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Consente di accedere alla topologia di un dispositivo audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Fornisce informazioni sui formati di dati audio supportati da una connessione di I/O configurata dal software (in genere un canale DMA) tra il dispositivo audio e la memoria di sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Fornisce informazioni sulle prese o sui connettori interni che forniscono una connessione fisica tra un dispositivo in una scheda audio e un dispositivo endpoint esterno o interno, ad esempio un microfono o un lettore di CD. |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Rappresenta una parte (connettore o unità secondaria) di una topologia del dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Rappresenta un elenco di parti (connettori e sottounità).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Rappresenta un'interfaccia di controllo di unità secondaria generica che fornisce il controllo per canale sul livello del volume, in decibel, di un flusso audio o di una banda di frequenze in un flusso audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Rappresenta una sottounità hardware (ad esempio, un controllo a livello di volume) che risiede nel percorso dati tra un client e un dispositivo dell'endpoint audio.                                                                             |



 

I client dell'API DeviceTopology che richiedono la notifica di eventi di modifica del controllo in connettori e sottounità devono implementare la seguente interfaccia.



| Interfaccia                                            | Descrizione                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Fornisce notifiche quando cambia lo stato di una parte (connettore o sottounità). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie del dispositivo](device-topologies.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
