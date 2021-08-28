---
description: Il routing di flusso è la capacità di un'applicazione multimediale di passare da un flusso all'altro tra dispositivi con un'interruzione minima della riproduzione o della sessione di acquisizione.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Routing di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e76944954c969ce458175585076d23ce015ea573a86e3f89dbbcd296aff444
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018229"
---
# <a name="stream-routing"></a>Routing di flusso

*Il routing di* flusso è la capacità di un'applicazione multimediale di passare da un flusso all'altro tra dispositivi con un'interruzione minima della riproduzione o della sessione di acquisizione.

Un computer può avere più dispositivi di rendering e acquisizione. Il sistema elenca questi dispositivi nel pannello **di controllo** Suoni. Da questo elenco, un utente può impostare un dispositivo come dispositivo predefinito per ogni ruolo: riproduzione, registrazione o quattro ruoli di comunicazione (rendering della console, acquisizione della console, rendering delle comunicazioni o acquisizione delle comunicazioni). L'elenco dei dispositivi può essere modificato dinamicamente perché alcuni di questi dispositivi possono essere temporaneamente disponibili, ad esempio un visore VR USB. Quando sono disponibili più dispositivi, l'utente può modificare l'impostazione predefinita in un altro dispositivo. L'utente può anche modificare il formato di un dispositivo (frequenza di campionamento, bit per campione e così via) nella **scheda** Avanzate per le proprietà del dispositivo.

Si consideri uno scenario in cui un utente seleziona **Speakers** come dispositivo predefinito per il rendering dei flussi audio. L'utente connette quindi un visore VR USB, seleziona il visore VR come nuovo dispositivo predefinito e modifica la frequenza di campionamento del dispositivo da 44,1 kHz a 48 kHz. L'utente vuole riprodurre il flusso audio sul visore VR alla nuova frequenza di campionamento con un'interruzione minima della sessione di streaming.

In questo scenario, l'applicazione multimediale deve gestire due casi:

-   Il flusso deve essere trasferito al nuovo dispositivo predefinito con un'interruzione minima della riproduzione.
-   Il nuovo dispositivo deve riprendere la riproduzione nel nuovo formato, ovvero l'utente può modificare più della frequenza di campionamento.

In Windows Vista, per supportare questo scenario, l'applicazione multimediale doveva fornire l'implementazione per il routing dei flussi. L'applicazione era responsabile della terminazione dei flussi esistenti e del riavvio dei flussi nel nuovo dispositivo. Se l'utente ha modificato il dispositivo predefinito o il relativo formato di combinazione, tutte le sessioni associate sono state chiuse e l'applicazione ha dovuto gestire il ripristino.

In Windows 7 un'applicazione può trasferire facilmente un flusso da un dispositivo predefinito esistente a un nuovo endpoint audio predefinito. I set di API audio di alto livello, ad esempio Media Foundation, DirectSound e WAVE, implementano la funzionalità di routing dei flussi. Le applicazioni multimediali che usano questi set di API per riprodurre o acquisire un flusso dal dispositivo predefinito usano l'implementazione predefinita e non devono modificare l'applicazione. Tuttavia, se l'applicazione multimediale usa direttamente MMDeviceAPI o WASAPI, l'applicazione deve fornire l'implementazione del routing del flusso.

> [!Note]  
> MMDeviceAPI e WASAPI sono componenti principali dell'API audio che un'applicazione può usare per eseguire il rendering o acquisire un flusso in un dispositivo. MMDeviceAPI individua il nuovo dispositivo endpoint audio e WASAPI gestisce il flusso di dati audio tra un'applicazione multimediale e il dispositivo endpoint audio.

 

Per implementare la funzionalità di routing del flusso, l'applicazione deve restare in ascolto delle notifiche inviate da MMDeviceAPI e WASAPI quando:

-   Il dispositivo predefinito viene modificato dall'utente.
-   Il dispositivo predefinito esistente viene rimosso e viene aggiunto un nuovo dispositivo predefinito.
-   Il formato del dispositivo è stato modificato.

Gestendo queste notifiche, un'applicazione può eseguire le operazioni di gestione dei flussi necessarie durante il trasferimento del flusso al nuovo dispositivo predefinito. Inoltre, l'applicazione può eseguire il rendering o acquisire flussi esistenti usando il nuovo formato specificato dall'utente mentre è attiva una sessione di rendering.

Questa sezione contiene i seguenti argomenti:

-   [Recupero dell'endpoint del dispositivo per il routing di flusso](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notifiche rilevanti per il routing di flusso](relevant-device-notifications-for-stream-routing.md)
-   [Considerazioni sull'implementazione del routing dei flussi](stream-routing-implementation-considerations.md)

Gli esempi seguenti, inclusi in Windows SDK, illustrano come un'applicazione può gestire le notifiche di routing dei flussi.

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

 

 



