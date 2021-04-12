---
description: Il routing del flusso è la capacità di un'applicazione multimediale di cambiare i flussi tra i dispositivi con interruzioni minime della riproduzione o della sessione di acquisizione.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Routing del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483461"
---
# <a name="stream-routing"></a>Routing del flusso

Il *routing del flusso* è la capacità di un'applicazione multimediale di cambiare i flussi tra i dispositivi con interruzioni minime della riproduzione o della sessione di acquisizione.

Un computer può avere più dispositivi di rendering e acquisizione. Il sistema elenca questi dispositivi nel pannello di controllo **suoni** . Da questo elenco, un utente può impostare un dispositivo come il dispositivo predefinito per ogni ruolo: riproduzione, registrazione o quattro ruoli di comunicazione (rendering della console, acquisizione della console, rendering della comunicazione o acquisizione delle comunicazioni). L'elenco dei dispositivi può essere modificato dinamicamente perché alcuni di questi dispositivi possono essere temporaneamente disponibili, ad esempio una cuffia USB. Quando sono disponibili più dispositivi, l'utente può modificare il valore predefinito in un dispositivo diverso. L'utente può anche modificare il formato di un dispositivo (frequenza di campionamento, BITS per esempio e così via) nella scheda **Avanzate** per le proprietà del dispositivo.

Si consideri uno scenario in cui un utente seleziona gli **altoparlanti** come dispositivo predefinito per il rendering dei flussi audio. L'utente connette quindi una cuffia USB, seleziona l'auricolare come nuovo dispositivo predefinito e modifica la frequenza di campionamento del dispositivo da 44,1 kHz a 48 kHz. L'utente vuole riprodurre il flusso audio nell'auricolare alla nuova frequenza di campionamento con un'interruzione minima della sessione di streaming.

In questo scenario, è necessario che l'applicazione multimediale gestisca due casi:

-   Il flusso deve essere trasferito al nuovo dispositivo predefinito con interruzioni minime per la riproduzione.
-   Il nuovo dispositivo deve riprendere la riproduzione nel nuovo formato (ovvero, l'utente può modificare una frequenza superiore a quella di campionamento).

In Windows Vista, per supportare questo scenario, l'applicazione multimediale doveva fornire l'implementazione per il routing del flusso. L'applicazione è stata responsabile della terminazione dei flussi esistenti e del riavvio dei flussi nel nuovo dispositivo. Se l'utente ha modificato il dispositivo predefinito o il formato di combinazione modificato, tutte le sessioni associate sono state chiuse e l'applicazione doveva gestire il ripristino.

In Windows 7, un'applicazione può trasferire facilmente un flusso da un dispositivo predefinito esistente a un nuovo endpoint audio predefinito. I set di API audio di alto livello, come Media Foundation, DirectSound e le API WAVE, implementano la funzionalità di routing dei flussi. Le applicazioni multimediali che usano questi set di API per riprodurre o acquisire un flusso dal dispositivo predefinito usano l'implementazione predefinita e non dovranno modificare l'applicazione. Tuttavia, se l'applicazione multimediale USA direttamente MMDeviceAPI o WASAPI, l'applicazione deve fornire l'implementazione del routing del flusso.

> [!Note]  
> MMDeviceAPI e WASAPI sono componenti dell'API audio Core che possono essere usati da un'applicazione per eseguire il rendering o l'acquisizione di un flusso in un dispositivo. Il MMDeviceAPI individua il nuovo dispositivo dell'endpoint audio e WASAPI gestisce il flusso di dati audio tra un'applicazione multimediale e il dispositivo dell'endpoint audio.

 

Per implementare la funzionalità di routing del flusso, l'applicazione deve restare in ascolto delle notifiche inviate da MMDeviceAPI e WASAPI nei casi seguenti:

-   Il dispositivo predefinito viene modificato dall'utente.
-   Il dispositivo predefinito esistente viene rimosso e viene aggiunto un nuovo dispositivo predefinito.
-   Il formato del dispositivo è stato modificato.

Gestendo queste notifiche, un'applicazione può eseguire le operazioni di gestione del flusso necessarie durante il trasferimento del flusso al nuovo dispositivo predefinito. Inoltre, l'applicazione può eseguire il rendering o acquisire i flussi esistenti usando il nuovo formato specificato dall'utente mentre è attiva una sessione di rendering.

Questa sezione contiene i seguenti argomenti:

-   [Recupero dell'endpoint del dispositivo per il routing del flusso](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notifiche rilevanti per il routing dei flussi](relevant-device-notifications-for-stream-routing.md)
-   [Considerazioni sull'implementazione del routing del flusso](stream-routing-implementation-considerations.md)

Negli esempi seguenti, inclusi nel Windows SDK, viene illustrato il modo in cui un'applicazione è in grado di gestire le notifiche di routing del flusso.

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> <dt>

[Informazioni sull'API MMDevice](mmdevice-api.md)
</dt> <dt>

[Informazioni su WASAPI](wasapi.md)
</dt> </dl>

 

 



