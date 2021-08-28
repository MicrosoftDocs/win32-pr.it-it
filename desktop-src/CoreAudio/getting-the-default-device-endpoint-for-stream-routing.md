---
description: In Windows 7, le API della piattaforma di alto livello che usano API audio di base come le API Media Foundation, DirectSound e Wave implementano la funzionalità di routing del flusso gestendo il passaggio del flusso da un dispositivo esistente a un nuovo endpoint audio predefinito.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Recupero dell'endpoint del dispositivo per il routing di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb45560bc8a27e4641e5d52c8fed0bee51c877dbec4d098bb5232830359f0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695391"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Recupero dell'endpoint del dispositivo per il routing di flusso

In Windows 7, le API della piattaforma di alto livello che usano API audio di base come le API Media Foundation, DirectSound e Wave implementano la funzionalità di routing del flusso gestendo il passaggio del flusso da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API (ad esempio, un'applicazione che attiva un oggetto **IDirectSound** o **IBaseFilter** in un oggetto [**IMMDevice)**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) usano il comportamento di routing del flusso senza alcuna modifica all'origine.

Le API di alto livello implementano il routing dei flussi per l'endpoint del dispositivo ottenuto tramite [**IMMDeviceEnumerator::GetDefaultAudioEndpoint.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) Se un'applicazione viene trasmessa al dispositivo predefinito, la funzionalità di routing del flusso funziona come definito. Flussi non vengono passate al nuovo dispositivo se viene recuperato da qualsiasi altro meccanismo, anche se corrisponde al dispositivo predefinito.

Un'applicazione multimediale che usa direttamente le API core audio (client WASAPI) può fornire un'implementazione personalizzata del routing dei flussi per qualsiasi dispositivo di rendering o acquisizione. Un client WASAPI può replicare l'implessimento fornito dalle API di alto livello limitarlo ai flussi aperti nei dispositivi impostati come dispositivo predefinito. Per ottenere un riferimento all'endpoint del dispositivo predefinito, il client deve chiamare [**IMMDeviceEnumerator::GetDefaultAudioEndpoint.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) In questa chiamata, il client deve indicare se richiede un puntatore al dispositivo predefinito per il rendering o al dispositivo predefinito di acquisizione specificando il *parametro dataFlow.* Il client deve anche specificare il ruolo appropriato per l'endpoint nell'attributo **ERole** (**eConsole** o **eCommunications**). Non usare **eMultimedia**.

Se l'applicazione viene trasmessa a qualsiasi altro dispositivo, l'applicazione può ottenere il dispositivo specificando una stringa di ID endpoint (chiamando [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Dopo l'identificazione del dispositivo, il client WASAPI può fornire l'implementazione per il routing del flusso gestendo le notifiche del dispositivo e della sessione audio inviate per il dispositivo. Per altre informazioni su queste notifiche, vedere [Notifiche pertinenti per il routing di flusso.](relevant-device-notifications-for-stream-routing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing di flusso](stream-routing.md)
</dt> </dl>

 

 



