---
description: DeviceTopology API
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: DeviceTopology API
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 3b79def9f1cb1f5ec9342074b813e50993cbc37e7a7af2a9e0b577c730156247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406756"
---
# <a name="devicetopology-api"></a>DeviceTopology API

Vedere [l'esempio di acquisizione vocale di alta DMO Microsoft.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray)

L'API DeviceTopology offre alle applicazioni client la possibilità di attraversare le topologie hardware funzionali dei dispositivi di rendering e acquisizione audio. Tramite le interfacce e i metodi nell'API DeviceTopology, i client possono individuare le sottounità funzionali (ad esempio, il controllo del volume) che si trovano lungo i percorsi dati che conducono a e da dispositivi [endpoint audio.](audio-endpoint-devices.md) I client possono attraversare le topologie interne dei dispositivi adattatore audio e dei dispositivi endpoint audio e attraversare le connessioni che collegano un dispositivo a un altro. Per altre informazioni, vedere [Topologie dei dispositivi](device-topologies.md).

Il file di intestazione Devicetopology.h definisce le interfacce nell'API DeviceTopology.

Per accedere alle interfacce API DeviceTopology, un client ottiene innanzitutto un riferimento [**all'interfaccia IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) per un dispositivo endpoint audio seguendo questa procedura:

1.  Usando una delle tecniche descritte in [**IMMDevice Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), ottenere un riferimento all'interfaccia **IMMDevice** per un dispositivo endpoint audio.
2.  Chiamare il [**metodo IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *iid* impostato su **REFIID** IID \_ IDeviceTopology.

Il client può ottenere riferimenti ad altre interfacce nell'API DeviceTopology chiamando i metodi [**nell'interfaccia IDeviceTopology.**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)

L'API DeviceTopology implementa le interfacce seguenti.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Fornisce l'accesso a un controllo del guadagno automatico (AGC) hardware.                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Fornisce l'accesso a un controllo hardware a livello di basso.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Fornisce l'accesso a un controllo di configurazione del canale hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Fornisce l'accesso a un controllo multiplexer hardware (selettore di input).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Fornisce l'accesso a un controllo di compensazione "loudness".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Fornisce l'accesso a un controllo a livello di fascia media dell'hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Fornisce l'accesso a un controllo di disattivazione dell'audio hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Fornisce l'accesso a un controllo demultiplexer hardware (selettore di output).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Fornisce l'accesso a un controllo del contatore di picco dell'hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Fornisce l'accesso a un controllo a livello di acuto hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Fornisce l'accesso a un controllo del volume hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Rappresenta un punto di connessione tra i componenti.                                                                                                                                                                      |
| [**Interfaccia IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Rappresenta un'interfaccia di controllo su una parte (sottounità o connettore).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Rappresenta una proprietà specifica del dispositivo di un connettore o di una sottounità.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Fornisce l'accesso alla topologia di un dispositivo audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Fornisce informazioni sui formati di dati audio supportati da una connessione I/O configurata dal software (in genere un canale DMA) tra il dispositivo audio e la memoria di sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Fornisce informazioni sui jack o sui connettori interni che forniscono una connessione fisica tra un dispositivo su una scheda audio e un dispositivo endpoint esterno o interno ,ad esempio un microfono o un lettore CD. |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Rappresenta una parte (connettore o sottounità) di una topologia del dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Rappresenta un elenco di parti (connettori e sottounità).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Rappresenta un'interfaccia di controllo di sottounità generica che fornisce il controllo per canale sul livello del volume, in decibel, di un flusso audio o di una banda di frequenza in un flusso audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Rappresenta una sottounità hardware (ad esempio, un controllo a livello di volume) che si trova nel percorso dati tra un client e un dispositivo endpoint audio.                                                                             |



 

I client API DeviceTopology che richiedono la notifica degli eventi di modifica del controllo nei connettori e nelle sottounità devono implementare l'interfaccia seguente.



| Interfaccia                                            | Descrizione                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Fornisce notifiche quando lo stato di una parte (connettore o sottounità) cambia. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie dei dispositivi](device-topologies.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
