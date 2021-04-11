---
description: In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notifiche rilevanti per il routing dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3d253ce2ec5d6e3bef025a33233a9d377ca44b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126894"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notifiche rilevanti per il routing dei flussi

In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API usano il comportamento di routing del flusso senza apportare alcuna modifica all'origine. I client WASAPI diretti possono usare le notifiche inviate dai componenti audio principali e implementare la funzionalità di routing dei flussi.

Per implementare la funzionalità di routing del flusso, un client deve restare in ascolto di due tipi di eventi: notifiche di modifica del dispositivo e notifiche di disconnessione della sessione. Nell'implementazione fornita dalle API di alto livello, questi eventi vengono inviati per gli endpoint di dispositivo predefiniti creati chiamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Per altre informazioni, vedere [ottenere l'endpoint del dispositivo per il routing del flusso](getting-the-default-device-endpoint-for-stream-routing.md).

Il componente audio principale MMDeviceAPI recapita i callback di notifica quando vengono aggiunti, rimossi o modificati dispositivi audio. Le modifiche al formato e alla sessione audio vengono segnalate come eventi tramite WASAPI.

## <a name="device-change-notifications"></a>Notifiche delle modifiche del dispositivo

MMDeviceAPI genera eventi quando vengono aggiunti, rimossi o modificati dispositivi audio. Se il client deve fornire la funzionalità di routing del flusso, deve implementare l'interfaccia [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registrarne l'implementazione con mmdeviceapi.

Per ottenere le notifiche di modifica del dispositivo, il client deve eseguire le attività seguenti:

-   Implementare l'interfaccia [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) per gestire le notifiche di modifica del dispositivo inviate da mmdeviceapi.
-   Registrare l'implementazione di [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) con MMDeviceAPI chiamando il metodo [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .

Dopo che l'implementazione del client di queste interfacce è stata registrata, il client riceve le notifiche sotto forma di callback tramite i metodi di tali interfacce. I metodi [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) vengono chiamati da MMDeviceAPI quando genera eventi a livello di endpoint (modifiche dello stato dell'endpoint, nuovi arrivi degli endpoint, eliminazioni di endpoint, modifiche di endpoint predefinite e modifiche delle proprietà dell'endpoint).

Se il client desidera fornire il routing del flusso per il dispositivo predefinito, il client deve implementare il comportamento di modifica del dispositivo quando riceve la notifica tramite il callback [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .

## <a name="audio-session-change-notifications"></a>Notifiche di modifica della sessione audio

Le modifiche della sessione audio e le modifiche di formato vengono segnalate come eventi di sessione audio tramite WASAPI. Un client WASAPI implementa l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra l'implementazione con WASAPI.

Per ottenere le notifiche di modifica della sessione audio, il client deve eseguire le attività seguenti:

-   Implementare l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per gestire le notifiche di modifica del formato inviate da WASAPI.
-   Registrare l'implementazione di [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) con WASAPI chiamando il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) .

I metodi [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) vengono chiamati da WASAPI quando si verificano modifiche alla sessione audio. Questi eventi vengono generati quando il nome visualizzato della sessione, il percorso dell'icona, il volume, il parametro di raggruppamento o lo stato cambiano.

Per implementare la funzionalità di routing del flusso, il client deve attendere la notifica di disconnessione della sessione. Quando una sessione audio viene disconnessa o viene modificato il formato di un dispositivo, WASAPI Invia le notifiche client sotto forma di callback tramite [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Con la notifica di disconnessione, WASAPI invia anche un valore che indica il motivo per cui la sessione è stata disconnessa. Questo problema può verificarsi per diversi motivi, ad esempio se il dispositivo è stato rimosso, il server è stato arrestato e così via. Per l'elenco completo dei motivi, vedere l'enumerazione **AudioSessionDisconnectReason** definita in AudioPolicy. h. Se il dispositivo predefinito viene modificato, il client deve attendere le notifiche, se non sono già state ricevute, associate a un valore **DisconnectReasonDeviceRemoval** . In risposta a tali notifiche, il client potrebbe riaprire il flusso sul nuovo dispositivo predefinito.

Poiché tutte queste operazioni sono asincrono, l'ordine in cui l'applicazione riceve le notifiche Impossibile viene stimato. Tuttavia, in genere, l'applicazione riceve il valore **AudioSessionDisconnect** prima della notifica di modifica predefinita del dispositivo.

### <a name="format-change-notifications"></a>Notifiche di modifica del formato

Le modifiche al formato audio si verificano quando viene modificato il formato del flusso. Questo problema può verificarsi quando l'utente seleziona un nuovo formato nel pannello di controllo **audio** o il nuovo dispositivo predefinito supporta un nuovo formato (ad esempio, HDMI o alcune interfacce audio professionali con una regolazione manuale della frequenza di esempio). Per notificare al client questi tipi di modifiche di formato, WASAPI invia una notifica di sessione mediante l'implementazione registrata di [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con un motivo di disconnessione di **DisconnectReasonFormatChanged**. Il client può gestire la notifica riaprendo il flusso nel nuovo formato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing del flusso](stream-routing.md)
</dt> </dl>

 

 



