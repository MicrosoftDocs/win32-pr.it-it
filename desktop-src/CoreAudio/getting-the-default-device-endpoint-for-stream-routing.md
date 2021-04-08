---
description: In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Recupero dell'endpoint del dispositivo per il routing del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877850"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Recupero dell'endpoint del dispositivo per il routing del flusso

In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API (ad esempio, un'applicazione che attiva un oggetto **IDirectSound** o **IBaseFilter** su un oggetto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usano il comportamento di routing del flusso senza apportare alcuna modifica all'origine.

Le API di alto livello implementano il routing del flusso per l'endpoint del dispositivo ottenuto tramite [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Se un'applicazione esegue il flusso al dispositivo predefinito, la funzionalità di routing del flusso funziona come definito. I flussi non vengono passati al nuovo dispositivo se vengono recuperati da qualsiasi altro meccanismo anche se corrisponde al dispositivo predefinito.

Un'applicazione multimediale che usa direttamente le API audio principali (client WASAPI) può fornire un'implementazione di routing del flusso personalizzata per qualsiasi dispositivo di rendering o acquisizione. Un client WASAPI può replicare il implementazione fornito dalle API di alto livello limitandosi ai flussi aperti nei dispositivi impostati come dispositivo predefinito. Per ottenere un riferimento all'endpoint del dispositivo predefinito, il client deve chiamare [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In questa chiamata il client deve indicare se è necessario un puntatore al dispositivo predefinito di rendering o alla periferica di acquisizione predefinita specificando il parametro *dataflow* . Il client deve inoltre specificare il ruolo appropriato per l'endpoint nell'attributo **ERole** (**eConsole** o **comunicazioni elettroniche**). Non usare **eMultimedia**.

Se l'applicazione viene trascinata in qualsiasi altro dispositivo, l'applicazione può ottenere il dispositivo specificando una stringa ID endpoint (chiamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Dopo che il dispositivo è stato identificato, il client WASAPI può fornire l'implementazione per il routing del flusso gestendo le notifiche della sessione audio e del dispositivo inviate per il dispositivo. Per ulteriori informazioni su queste notifiche, vedere [notifiche rilevanti per il routing del flusso](relevant-device-notifications-for-stream-routing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing del flusso](stream-routing.md)
</dt> </dl>

 

 



