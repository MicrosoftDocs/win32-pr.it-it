---
description: In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Considerazioni sull'implementazione del routing del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27dc1f7e3fe56d6b421ca59f528ab1a65d2261a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966175"
---
# <a name="stream-routing-implementation-considerations"></a>Considerazioni sull'implementazione del routing del flusso

In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API usano il comportamento di routing del flusso senza apportare alcuna modifica all'origine. I client WASAPI diretti possono usare le notifiche inviate dai componenti audio principali e implementare la funzionalità di routing dei flussi.

I client WASAPI diretti (le applicazioni multimediali che usano direttamente WASAPI) ricevono nuove notifiche di sessione audio e dispositivo inviate dai componenti audio di base. Il comportamento della funzionalità di routing del flusso è definito dal modo in cui l'applicazione gestisce queste notifiche.

L'API MMDevice e la sessione audio inviano notifiche sulle modifiche dello stato del dispositivo e sulle modifiche di sessione ai client WASAPI sotto forma di callback. Per ottenere queste notifiche, il client deve registrare l'implementazione di [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Per ulteriori informazioni, vedere [notifiche rilevanti per il routing del flusso](relevant-device-notifications-for-stream-routing.md).

Nello scenario dell'auricolare USB descritto in [routing del flusso](stream-routing.md), un'applicazione sta riproducendo un flusso audio e USA MMDEVICEAPI e WASAPI per eseguire il rendering del flusso sul dispositivo di rendering predefinito, **speaker**. Quando viene modificato il dispositivo predefinito, l'applicazione riceve una notifica [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) . L'applicazione riceve anche le notifiche [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) che indicano che l'utente ha rimosso il dispositivo dell'endpoint audio o che il formato del flusso è stato modificato per il dispositivo a cui è connessa la sessione audio. Al momento della ricezione delle notifiche, l'applicazione interrompe lo streaming all'endpoint speaker e riapre il flusso per il rendering sull'endpoint predefinito corrente, ovvero l'auricolare.

![diagramma del flusso di dati per le notifiche del dispositivo.](images/stream-routing.gif)

In risposta a tali notifiche, il client potrebbe riaprire il flusso sul nuovo dispositivo predefinito nel nuovo formato selezionato dall'utente.

## <a name="stream-managment"></a>Gestione flussi

Nell'elenco seguente vengono riepilogati i passaggi che un client WASAPI deve eseguire per fornire la funzionalità di cambio del flusso.

1.  Attendere la notifica di [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) pertinente. Se il dispositivo è il dispositivo predefinito, viene ricevuta la notifica [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .
2.  Se è disponibile un nuovo dispositivo, ottenere un riferimento all'endpoint del nuovo dispositivo. Chiamare [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per il nuovo dispositivo predefinito. Se il nuovo dispositivo non è il dispositivo predefinito, è possibile recuperare il dispositivo chiamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Per altre informazioni, vedere [ottenere l'endpoint del dispositivo per il routing del flusso](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Attendere la [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con il valore Reason.
    > [!Note]  
    > Poiché tutte queste operazioni sono asincrono, l'ordine in cui l'applicazione riceve le notifiche di modifica del dispositivo e disconnessione della sessione Impossibile essere stimate. L'applicazione deve implementare la gestione delle notifiche per ricevere queste notifiche in qualsiasi ordine. Tuttavia, in genere, l'applicazione riceve il valore **AudioSessionDisconnect** prima della notifica di modifica predefinita del dispositivo.

     

4.  Valutare il valore del motivo e determinare se il flusso deve essere trasferito a un altro endpoint audio o se il flusso deve essere reinizializzato con un nuovo formato.
5.  Arrestare lo streaming al dispositivo predefinito precedente se il motivo indica che il flusso deve essere reindirizzato al nuovo dispositivo predefinito.
6.  Eseguire i calcoli di mapping della posizione.
7.  Aprire il flusso sul nuovo dispositivo e trasferire tutte le informazioni sullo stato.
8.  Riprendere lo streaming sul nuovo dispositivo predefinito.
9.  Gestire la partenza del dispositivo predefinito precedente.

Per far sembrare trasparente l'operazione di cambio del flusso, è necessario eseguire il più rapidamente possibile. Ciò dipende dalle prestazioni dei componenti interessati dalla ripetizione dell'avvio del flusso nel nuovo dispositivo.

## <a name="position-mapping-considerations"></a>Considerazioni sul mapping delle posizioni

Quando l'applicazione ottiene le notifiche [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) , può indirizzare i flussi esistenti al nuovo dispositivo predefinito. Quando un flusso audio esistente viene interrotto e aperto nel nuovo dispositivo, il rendering sul nuovo dispositivo deve iniziare in corrispondenza della posizione in cui il flusso è stato interrotto sul dispositivo precedente. A tale scopo, l'applicazione deve disporre dell'ultima posizione nota del dispositivo, per calcolare la posizione iniziale nel nuovo dispositivo. Questa posizione, ad esempio, può essere usata come offset Delta per il mapping della posizione successiva. Quando viene avviato il rendering del flusso, la nuova posizione del dispositivo può essere rimappata alla posizione del dispositivo memorizzata nella cache.

I passaggi seguenti riepilogano il processo di creazione di una transizione di flusso senza problemi.

1.  Memorizzare nella cache l'ultima posizione del dispositivo del flusso sul dispositivo precedente.
2.  Arrestare il flusso del dispositivo precedente.
3.  Eseguire il mapping dei calcoli per ottenere la nuova posizione.
4.  Avviare il rendering del flusso nel nuovo dispositivo.
5.  Rilascia il flusso precedente.

Durante la transizione, l'applicazione deve assicurarsi che l'orologio non ottenga la sincronizzazione, ottenendo flussi audio e video non sincronizzati. Questo problema può verificarsi se gli esempi video continuano a essere sottoposte a rendering mentre il flusso audio viene indirizzato al nuovo dispositivo. L'applicazione deve memorizzare nella cache la posizione di clock per il calcolo di nuovo mapping e assicurarsi che non venga eseguito il rendering degli esempi video fino a quando il flusso audio non viene riaperto sul nuovo dispositivo, in modo che quando il clip riprende il rendering, i flussi audio e video sono sincronizzati. In alcuni casi, in cui il tempo di presentazione per il rendering dei fotogrammi video è basato sul clock audio, è sufficiente arrestare il flusso audio fino al completamento del cambio di flusso e non è necessaria alcuna implementazione di mapping di posizione per il flusso video per la sincronizzazione del video audio.

Se durante il rendering, [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) restituisce un errore perché il dispositivo precedente viene perso, l'applicazione non deve arrestare il flusso precedente perché l'operazione di streaming è già terminata. Per informazioni sulla gestione di questo errore, vedere [recupero da un errore di Invalid-Device](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing del flusso](stream-routing.md)
</dt> </dl>

 

 



