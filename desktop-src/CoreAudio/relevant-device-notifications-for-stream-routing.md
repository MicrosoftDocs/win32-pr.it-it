---
description: Informazioni sulle notifiche per il routing di flusso. Le API implementano il routing di flusso gestendo il passaggio del flusso a un nuovo endpoint audio predefinito.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notifiche pertinenti per il routing di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a843c1d8b5cfd740ada5049cb9428e7745072d
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068527"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notifiche pertinenti per il routing di flusso

In Windows 7 le API della piattaforma di alto livello che usano LE API audio di base, ad esempio le API Media Foundation, DirectSound e Wave, implementano la funzionalità di routing del flusso gestendo il passaggio del flusso da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API usano il comportamento di routing del flusso senza alcuna modifica all'origine. I client WASAPI diretti possono usare le notifiche inviate dai componenti Audio core e implementare la funzionalità di routing del flusso.

Per implementare la funzionalità di routing del flusso, un client deve restare in ascolto di due tipi di eventi: notifiche di modifica del dispositivo e notifiche di disconnessione della sessione. Nell'implementazione fornita dalle API di alto livello, questi eventi vengono inviati per gli endpoint dispositivo predefiniti creati chiamando [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Per altre informazioni, vedere [Recupero dell'endpoint del dispositivo per il routing di flusso.](getting-the-default-device-endpoint-for-stream-routing.md)

Il componente Audio principale MMDeviceAPI recapita callback di notifica quando i dispositivi audio vengono aggiunti, rimossi o modificati. Le modifiche al formato e alla sessione audio vengono segnalate come eventi tramite WASAPI.

## <a name="device-change-notifications"></a>Notifiche di modifica del dispositivo

MMDeviceAPI genera eventi quando i dispositivi audio vengono aggiunti, rimossi o modificati. Se il client deve fornire funzionalità di routing di flusso, deve implementare [**l'interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registrarne l'implementazione con MMDeviceAPI.

Per ottenere le notifiche di modifica del dispositivo, il client deve eseguire le attività seguenti:

-   Implementare [**l'interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) per gestire le notifiche di modifica del dispositivo inviate da MMDeviceAPI.
-   Registrare [**l'implementazione di IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) con MMDeviceAPI chiamando il [**metodo IMMDeviceEnumerator::RegisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback)

Dopo la registrazione dell'implementazione del client di queste interfacce, il client riceve le notifiche sotto forma di callback tramite i metodi di queste interfacce. I [**metodi IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) vengono chiamati da MMDeviceAPI quando genera eventi a livello di endpoint (modifiche dello stato dell'endpoint, nuovi arrivi di endpoint, eliminazioni di endpoint, modifiche dell'endpoint predefinite e modifiche alle proprietà dell'endpoint).

Se il client vuole fornire il routing di flusso per il dispositivo predefinito, il client deve implementare il comportamento di modifica del dispositivo quando riceve la notifica tramite il callback [**IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)

## <a name="audio-session-change-notifications"></a>Notifiche di modifica della sessione audio

Le modifiche della sessione audio e le modifiche di formato vengono segnalate come eventi di sessione audio tramite WASAPI. Un client WASAPI implementa [**l'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra l'implementazione con WASAPI.

Per ottenere le notifiche di modifica della sessione audio, il client deve eseguire le attività seguenti:

-   Implementare [**l'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per gestire le notifiche di modifica del formato inviate da WASAPI.
-   Registrare [**l'implementazione di IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) con WASAPI chiamando il [**metodo IAudioSessionControl::RegisterAudioSessionNotification.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification)

[**I metodi IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) vengono chiamati da WASAPI quando si verificano modifiche della sessione audio. Questi eventi vengono generati quando cambia il nome visualizzato, il percorso dell'icona, il volume, il parametro di raggruppamento o lo stato della sessione.

Per implementare la funzionalità di routing del flusso, il client deve attendere la notifica di disconnessione sessione. Quando una sessione audio viene disconnessa o il formato di un dispositivo viene modificato, WASAPI invia le notifiche client sotto forma di callback tramite [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Con la notifica di disconnessione, WASAPI invia anche un valore che indica il motivo per cui la sessione è stata disconnessa. Ciò può verificarsi per diversi motivi, ad esempio la rimozione del dispositivo, l'arresto del server e così via. Per l'elenco completo dei motivi, vedere **l'enumerazione AudioSessionDisconnectReason** definita in AudioPolicy.h. Se il dispositivo predefinito cambia, il client deve attendere le notifiche (se non sono già state ricevute) che sono accompagnate da un **valore DisconnectReasonDeviceRemoval.** In risposta a tali notifiche, il client potrebbe riaprire il flusso nel nuovo dispositivo predefinito.

Poiché tutte queste operazioni sono asychronous, l'ordine in cui l'applicazione riceve le notifiche non può essere previsto. Tuttavia, in genere, l'applicazione riceve il **valore AudioSessionDisconnect** prima della notifica di modifica del dispositivo predefinita.

### <a name="format-change-notifications"></a>Formattare le notifiche di modifica

Le modifiche al formato audio si verificano quando cambia il formato del flusso. Ciò può verificarsi quando l'utente  seleziona un nuovo formato nel pannello di controllo Audio o il nuovo dispositivo predefinito supporta un nuovo formato, ad esempio HDMI o alcune interfacce audio professionali con una regolazione manuale della frequenza di campionamento. Per notificare al client questi tipi di modifiche di formato, WASAPI invia una notifica di sessione dall'implementazione registrata di [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con un motivo di disconnessione **di DisconnectReasonFormatChanged.** Il client può gestire la notifica riaprendo il flusso nel nuovo formato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing di flusso](stream-routing.md)
</dt> </dl>

 

 



