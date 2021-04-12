---
description: Questa guida di riferimento per la programmazione di Core Audio SDK include le proprietà seguenti.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Proprietà audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522890"
---
# <a name="core-audio-properties"></a>Proprietà audio principali

Questa guida di riferimento per la programmazione di Core Audio SDK include le proprietà seguenti.

## <a name="audio-endpoint-properties"></a>Proprietà endpoint audio

Core Audio SDK include diverse proprietà dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md). Per altre informazioni, vedere [proprietà dell'endpoint audio](audio-endpoint-properties.md).

Le proprietà seguenti sono definite in mmdeviceapi. h in Windows Vista e versioni successive.



| Proprietà                                                                                                            | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Associazione pkey AudioEndpoint \_**](pkey-audioendpoint-association.md)                                          | Associa una categoria di pin di streaming kernel (KS) a un dispositivo endpoint audio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Specifica il CLSID del provider registrato dell'estensione delle proprietà del dispositivo per il dispositivo dell'endpoint audio.                                              |
| [**PKEY \_ AudioEndpoint \_ Disabilita \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che scorre verso o dal dispositivo dell'endpoint audio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica gli attributi fisici del dispositivo dell'endpoint audio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Specifica la maschera di configurazione del canale per gli altoparlanti con intervallo completo connessi al dispositivo dell'endpoint audio.                                         |
| [**\_GUID AUDIOENDPOINT \_ pkey**](pkey-audioendpoint-guid.md)                                                        | Fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo dell'endpoint audio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definisce la configurazione dell'altoparlante fisico per il dispositivo dell'endpoint audio.                                                                                     |
| [**PKEY \_ Audioengine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Specifica il formato del dispositivo, che è il formato usato dal motore audio per il flusso in modalità condivisa che passa da o verso il dispositivo dell'endpoint audio.       |
| [**PKEY \_ Audioengine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso. I valori vengono popolati dall'OEM in un file con estensione inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ supporta \_ la \_ modalità EventDriven**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica se l'endpoint supporta la modalità guidata dagli eventi. I valori vengono popolati dall'OEM in un file con estensione inf.<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contiene un GUID della categoria di output per un dispositivo endpoint audio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Proprietà dispositivo

Core Audio SDK include diverse proprietà dei dispositivi per l' [endpoint audio](audio-endpoint-devices.md). Per altre informazioni, vedere [proprietà del dispositivo](device-properties.md).

Le proprietà seguenti sono definite in Functiondiscoverykeys \_ devpkey. h in Windows Vista e versioni successive.



| Proprietà                                                                         | Descrizione                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ deviceinterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nome descrittivo della scheda audio a cui è collegato il dispositivo dell'endpoint (ad esempio, "scheda audio XYZ").                                                                               |
| [**\_DeviceDesc del dispositivo pkey \_**](pkey-device-devicedesc.md)                       | Descrizione del dispositivo dell'endpoint (ad esempio, "Speakers").                                                                                                                          |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nome descrittivo del dispositivo dell'endpoint (ad esempio, "altoparlanti (scheda audio XYZ)").                                                                                                           |
| **\_ContainerId del dispositivo pkey \_**                                                    | Archivia l'identificatore del contenitore del dispositivo PnP che implementa l'endpoint audio. Per ulteriori informazioni su questa proprietà, vedere "riferimento alle proprietà dei dispositivi" nella documentazione di Windows WDK. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




