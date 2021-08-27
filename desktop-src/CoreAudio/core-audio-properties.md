---
description: Questo riferimento alla programmazione per Core Audio SDK include le proprietà seguenti.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Proprietà audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2d6513798a03cbcd9092e24b37900b5eb686d5fd0c434480a933af50c02fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059001"
---
# <a name="core-audio-properties"></a>Proprietà audio principali

Questo riferimento alla programmazione per Core Audio SDK include le proprietà seguenti.

## <a name="audio-endpoint-properties"></a>Proprietà dell'endpoint audio

Core Audio SDK include diverse proprietà dei [dispositivi endpoint audio.](audio-endpoint-devices.md) Per altre informazioni, vedere [Proprietà dell'endpoint audio.](audio-endpoint-properties.md)

Le proprietà seguenti sono definite in Mmdeviceapi.h in Windows Vista e versioni successive.



| Proprietà                                                                                                            | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Associazione \_ \_ AudioEndpoint PKEY**](pkey-audioendpoint-association.md)                                          | Associa una categoria di pin di streaming del kernel (KS) a un dispositivo endpoint audio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Specifica il CLSID del provider registrato dell'estensione device-properties per il dispositivo endpoint audio.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che passa da o verso il dispositivo endpoint audio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica gli attributi fisici del dispositivo endpoint audio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Specifica la maschera di configurazione del canale per gli altoparlanti a gamma completa connessi al dispositivo endpoint audio.                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo endpoint audio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definisce la configurazione dell'altoparlante fisico per il dispositivo endpoint audio.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Specifica il formato del dispositivo, ovvero il formato utilizzato dal motore audio per il flusso in modalità condivisa che passa da o verso il dispositivo endpoint audio.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso. I valori vengono popolati dall'OEM in un file inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ supporta la modalità \_ EventDriven \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica se l'endpoint supporta la modalità guidata da eventi. I valori vengono popolati dall'OEM in un file inf.<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contiene un GUID di categoria di output per un dispositivo endpoint audio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Proprietà dispositivo

Core Audio SDK include diverse proprietà dei dispositivi [endpoint audio.](audio-endpoint-devices.md) Per altre informazioni, vedere [Proprietà del dispositivo.](device-properties.md)

Le proprietà seguenti sono definite in Functiondiscoverykeys \_ devpkey.h in Windows Vista e versioni successive.



| Proprietà                                                                         | Descrizione                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nome descrittivo della scheda audio a cui è collegato il dispositivo endpoint, ad esempio "Scheda audio XYZ".                                                                               |
| [**PKEY \_ Device \_ DeviceDesc**](pkey-device-devicedesc.md)                       | Descrizione del dispositivo endpoint, ad esempio "Speakers".                                                                                                                          |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nome descrittivo del dispositivo endpoint, ad esempio "Speakers (XYZ Audio Adapter)".                                                                                                           |
| **PKEY \_ Device \_ ContainerId**                                                    | Archivia l'identificatore del contenitore del dispositivo PnP che implementa l'endpoint audio. Per altre informazioni su questa proprietà, vedere "Device Property Reference" (Informazioni di riferimento sulle proprietà del dispositivo) nella documentazione Windows WDK. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




