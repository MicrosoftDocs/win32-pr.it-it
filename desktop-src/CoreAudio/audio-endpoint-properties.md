---
description: Proprietà endpoint audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Proprietà endpoint audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225668"
---
# <a name="audio-endpoint-properties"></a>Proprietà endpoint audio

Il file di intestazione mmdeviceapi. h definisce diverse proprietà dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md) in Windows Vista e versioni successive. Il servizio audio di Windows imposta i valori di queste proprietà. I client possono leggere queste proprietà, ma non devono impostarle. I valori delle proprietà vengono archiviati come strutture **PROPVARIANT** .

Il metodo consigliato per leggere le proprietà di un dispositivo di input audio consiste nell'usare le API nello spazio dei nomi [**Windows. Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) . Queste API sono supportate per le app di Windows Store e le app desktop. Per le app desktop esistenti che leggono le proprietà del dispositivo usando l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , vedere [proprietà del dispositivo](device-properties.md). **IMMDevice** non è supportato per le app di Windows Store.

Per esempi di codice che illustrano come accedere alle proprietà di un dispositivo endpoint audio, vedere gli argomenti seguenti:

-   [Eventi dispositivo](device-events.md)
-   [Ruoli del dispositivo per le applicazioni DirectSound](device-roles-for-directsound-applications.md)

Per informazioni su **PROPVARIANT**, vedere la documentazione Windows SDK.

Le proprietà seguenti sono specifiche per i dispositivi endpoint audio.



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



 

Le API audio principali supportano proprietà aggiuntive che non si applicano esclusivamente ai dispositivi dell'endpoint audio. Per altre informazioni su queste proprietà aggiuntive, vedere [proprietà del dispositivo](device-properties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

