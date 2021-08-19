---
description: Proprietà dell'endpoint audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Proprietà dell'endpoint audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf76ef70afaed98ed04ad2ee56e83c38c14ffde1bb6e4d43b557d25769afb2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828502"
---
# <a name="audio-endpoint-properties"></a>Proprietà dell'endpoint audio

Il file di intestazione Mmdeviceapi.h definisce diverse proprietà dei dispositivi [endpoint audio](audio-endpoint-devices.md) in Windows Vista e versioni successive. Il Windows audio imposta i valori di queste proprietà. I client possono leggere queste proprietà, ma non devono impostarle. I valori delle proprietà vengono archiviati come strutture **PROPVARIANT.**

Il modo consigliato per leggere le proprietà di un dispositivo di input audio è usare le API nel [**Windows. Spazio dei nomi Devices.Enumeration.**](/uwp/api/Windows.Devices.Enumeration) Queste API sono supportate per le app Windows Store e le app desktop. Per le app desktop esistenti che leggono le proprietà del dispositivo [**usando l'interfaccia IMMDevice,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) vedere [Proprietà del dispositivo.](device-properties.md) **IMMDevice** non è supportato per le app Windows Store.

Per esempi di codice che illustrano come accedere alle proprietà di un dispositivo endpoint audio, vedere gli argomenti seguenti:

-   [Eventi del dispositivo](device-events.md)
-   [Ruoli del dispositivo per applicazioni DirectSound](device-roles-for-directsound-applications.md)

Per informazioni su **PROPVARIANT,** vedere la documentazione Windows SDK.

Le proprietà seguenti sono specifiche dei dispositivi endpoint audio.



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



 

Le API audio di base supportano proprietà aggiuntive che non si applicano esclusivamente ai dispositivi endpoint audio. Per altre informazioni su queste proprietà aggiuntive, vedere [Proprietà del dispositivo.](device-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

