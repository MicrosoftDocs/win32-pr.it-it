---
description: Informazioni sulle considerazioni sull'implementazione per il routing di flusso. Le API implementano il routing di flusso gestendo il passaggio del flusso a un nuovo endpoint audio predefinito.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Considerazioni sull'implementazione del routing di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd753fe027c92ffac9f5a41cea589b600d7f26
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068037"
---
# <a name="stream-routing-implementation-considerations"></a>Considerazioni sull'implementazione del routing di flusso

In Windows 7 le API della piattaforma di alto livello che usano LE API audio di base, ad esempio le API Media Foundation, DirectSound e Wave, implementano la funzionalità di routing del flusso gestendo il passaggio del flusso da un dispositivo esistente a un nuovo endpoint audio predefinito. Le applicazioni multimediali che usano queste API usano il comportamento di routing del flusso senza alcuna modifica all'origine. I client WASAPI diretti possono usare le notifiche inviate dai componenti Audio core e implementare la funzionalità di routing del flusso.

I client WASAPI diretti (applicazioni multimediali che usano direttamente WASAPI) ricevono nuove notifiche di sessione audio e dispositivo inviate dai componenti Core Audio. Il comportamento della funzionalità di routing del flusso è definito dal modo in cui l'applicazione gestisce queste notifiche.

L'API MMDevice e la sessione audio inviano notifiche relative alle modifiche dello stato del dispositivo e alle modifiche della sessione ai client WASAPI sotto forma di callback. Per ottenere queste notifiche, il client deve registrare l'implementazione di [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Per altre informazioni, vedere [Notifiche rilevanti per il routing di flusso.](relevant-device-notifications-for-stream-routing.md)

Nello scenario di visore USB descritto in [Routing](stream-routing.md)di flusso, un'applicazione sta riproducendo un flusso audio e usa MMDeviceAPI e WASAPI per eseguire il rendering del flusso nel dispositivo di rendering predefinito, **Speaker**. Quando il dispositivo predefinito viene modificato, l'applicazione riceve una [**notifica IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) L'applicazione riceve anche notifiche [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) che indicano che l'utente ha rimosso il dispositivo endpoint audio o che il formato del flusso è stato modificato per il dispositivo a cui è connessa la sessione audio. Alla ricezione delle notifiche, l'applicazione interrompe lo streaming all'endpoint del parlante e riapre il flusso per il rendering nell'endpoint predefinito corrente, il visore.

![diagramma del flusso di dati per le notifiche dei dispositivi.](images/stream-routing.gif)

In risposta a tali notifiche, il client potrebbe riaprire il flusso nel nuovo dispositivo predefinito nel nuovo formato selezionato dall'utente.

## <a name="stream-managment"></a>Stream Managment

L'elenco seguente riepiloga i passaggi che un client WASAPI deve eseguire per fornire la funzionalità di cambio di flusso.

1.  Attendere la notifica [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) pertinente. Se il dispositivo è il dispositivo predefinito, viene ricevuta la [**notifica IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)
2.  Se è disponibile un nuovo dispositivo, ottenere un riferimento all'endpoint del nuovo dispositivo. Chiamare [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per il nuovo dispositivo predefinito. Se il nuovo dispositivo non è il dispositivo predefinito, è possibile recuperare il dispositivo chiamando [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Per altre informazioni, vedere [Recupero dell'endpoint del dispositivo per il routing di flusso.](getting-the-default-device-endpoint-for-stream-routing.md)
3.  Attendere che [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con il valore del motivo.
    > [!Note]  
    > Poiché tutte queste operazioni sono asychronous, l'ordine in cui l'applicazione riceve notifiche di cambio dispositivo e disconnessione sessione non può essere stimata. L'applicazione deve implementare la gestione delle notifiche per ricevere queste notifiche in qualsiasi ordine. Tuttavia, in genere, l'applicazione riceve il **valore AudioSessionDisconnect** prima della notifica di modifica del dispositivo predefinita.

     

4.  Valutare il valore del motivo e determinare se il flusso deve essere trasferito a un altro endpoint audio o se il flusso deve essere reinizializzato con un nuovo formato.
5.  Interrompere lo streaming al dispositivo predefinito precedente se il motivo indica che il flusso deve essere nuovamente instradato al nuovo dispositivo predefinito.
6.  Eseguire calcoli di mapping delle posizioni.
7.  Aprire il flusso nel nuovo dispositivo e trasferire tutte le informazioni sullo stato.
8.  Riprendere lo streaming nel nuovo dispositivo predefinito.
9.  Gestire la partenza del dispositivo predefinito precedente.

Per rendere l'operazione di commutazione del flusso facile, è necessario eseguire il più rapidamente possibile. Ciò dipende dalle prestazioni dei componenti coinvolti nella reinizializzazione del flusso nel nuovo dispositivo.

## <a name="position-mapping-considerations"></a>Considerazioni sul mapping delle posizioni

Quando l'applicazione riceve le notifiche [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) può instradare i flussi esistenti al nuovo dispositivo predefinito. Quando un flusso audio esistente viene interrotto e aperto nel nuovo dispositivo, il rendering nel nuovo dispositivo deve iniziare dalla posizione in cui il flusso è stato arrestato nel dispositivo precedente. A tale scopo, l'applicazione deve avere l'ultima posizione del dispositivo nota, per calcolare la posizione iniziale nel nuovo dispositivo. Ad esempio, questa posizione può essere usata come offset differenziale per il successivo mapping della posizione. Quando il flusso avvia il rendering, è possibile modificare il mapping della nuova posizione del dispositivo alla posizione del dispositivo memorizzata nella cache.

I passaggi seguenti riepilogano il processo di transizione di un flusso facile.

1.  Memorizzare nella cache l'ultima posizione del dispositivo del flusso nel dispositivo precedente.
2.  Arrestare il flusso nel dispositivo precedente.
3.  Eseguire calcoli di nuovo mapping per ottenere la nuova posizione.
4.  Avviare il rendering del flusso nel nuovo dispositivo.
5.  Rilasciare il flusso precedente.

Durante la transizione, l'applicazione deve garantire che l'orologio non eserciti la sincronizzazione, determinando flussi audio e video non sincronizzati. Ciò può verificarsi se il rendering degli esempi video continua mentre il flusso audio viene instradato al nuovo dispositivo. L'applicazione deve memorizzare nella cache la posizione dell'orologio per il calcolo del nuovo mapping e assicurarsi che il rendering degli esempi video non sia eseguito fino alla riapertura del flusso audio nel nuovo dispositivo, in modo che quando il clip riprende il rendering, i flussi audio e video siano sincronizzati. In alcuni casi, in cui il tempo di presentazione per il rendering dei fotogrammi video è basato sull'orologio audio, è sufficiente arrestare il flusso audio fino al completamento del passaggio del flusso e non sono necessarie altre implementazioni del mapping della posizione per il flusso video per la sincronizzazione video audio.

Se durante il rendering, [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) restituisce un errore perché il dispositivo precedente viene perso, l'applicazione non deve arrestare il flusso precedente perché l'operazione di streaming è già terminata. Per informazioni sulla gestione di questo errore, vedere [Ripristino da un](recovering-from-an-invalid-device-error.md)errore Invalid-Device errore .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> <dt>

[Routing di flusso](stream-routing.md)
</dt> </dl>

 

 



