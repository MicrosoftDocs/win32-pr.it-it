---
title: Desktop Activity Moderator
description: Desktop Activity Moderator
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- durata della batteria
- standby connesso
- sospensione
- limitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8bb3d7925633d3feca8bb6ed5af191670af681
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730719"
---
# <a name="desktop-activity-moderator"></a>Desktop Activity Moderator

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


> [!Note]  
> La diga è presente solo nei computer client Windows 8 che supportano la modalità standby connessa. La diga non è presente negli SKU del server.

 

  

> [!Note]  
> Le app di Windows Store compilate per Windows 8 non sono interessate dalla diga.

 

  
</dl>

## <a name="description"></a>Descrizione

I nostri clienti si spostano verso più piattaforme mobili, più piccole e più semplici per soddisfare le proprie esigenze di elaborazione. Nell'ambito del passaggio ai dispositivi mobili, gli utenti sono diventati sempre più interessati alla durata della batteria dei propri dispositivi. Il moderatore di attività desktop (DAM) è una delle numerose nuove funzionalità di Windows 8 progettate per garantire la durata della batteria coerente e a lungo termine per i dispositivi che supportano la modalità standby connessa.

Standby connesso si verifica quando il dispositivo è acceso, ma lo schermo è disattivato. In questo stato di alimentazione, il sistema è tecnicamente sempre "on" (per supportare scenari chiave quali posta, VoIP, social networking e messaggistica immediata con le app di Windows Store). È analogo allo stato in cui si trova uno Smart Phone quando l'utente preme il pulsante di alimentazione.

Di conseguenza, il software (incluse le app e il software del sistema operativo) deve essere ben funzionante durante la modalità standby connessa. Il DAM è stato creato per impedire l'esecuzione dell'app desktop in modo simile allo stato di sospensione (S3 nei dispositivi ACPI). Questa operazione viene eseguita tramite la sospensione o la limitazione dei processi software desktop nel sistema in seguito alla voce standby connessa. Questo consente ai sistemi che supportano la modalità di standby connessa di offrire un utilizzo ridotto ridotto delle risorse e la durata della batteria continua e coerente, consentendo allo stesso tempo alle app di Windows Store di offrire le esperienze connesse.

## <a name="details"></a>Dettagli

La diga è un driver in modalità kernel che viene caricato e inizializzato all'avvio del sistema se il sistema supporta la modalità standby connessa. Questa operazione viene determinata valutando se il campo AOAC del sistema \_ \_La struttura delle funzionalità di risparmio energia restituita da CallNtPowerInformation è impostata su true).

Quando la diga è abilitata e il processo desktop viene creato, la diga aggiunge il processo agli oggetti processo gestiti dal sistema:

-   Se il processo è stato creato nella sessione 0, DAM aggiunge il processo a un oggetto processo soggetto alla **limitazione**
-   Se il processo è stato creato in una sessione interattiva (sessione 1 o successiva), DAM aggiunge il processo a un oggetto processo soggetto alla **sospensione**

> [!Note]  
> Per Windows 8, gli oggetti processo possono essere annidati. Ciò significa che l'utilizzo degli oggetti processo da parte della diga non interferisce con l'utilizzo esistente di un'app di oggetti processo.

 

Quando la schermata è accesa, la diga è disattivata e non ha alcun effetto sui processi nel sistema. Quando il sistema si trova in modalità standby connessa, a seconda dell'attività del sistema, la diga potrebbe limitare o sospendere i processi.

-   I processi soggetti a sospensione hanno tutti i thread sospesi (non consentiti per l'esecuzione in qualsiasi circostanza); lo stato dell'app (memoria del processo) viene mantenuto
-   Processi soggetti a un ciclo di limitazione tra sospeso e non sospeso (la maggior parte del tempo viene spesa nello stato Suspended)
    -   Tenere presente che Windows potrebbe rilevare anche che si sono verificate attività critiche e potrebbe sospendere i servizi limitati per periodi di tempo più lunghi durante questa attività
    -   Si noti inoltre che, sebbene in modalità standby connessa, i sensori e le reti potrebbero non essere disponibili, i processi limitati devono essere progettati in modo da essere resilienti alle condizioni di rete insufficienti (per la maggior parte dei processi non è necessaria alcuna modifica)

Quando la sospensione della diga è impegnata o disattivata, DAM attiva il recapito di un \_ messaggio WM POWERBROADCAST a questi processi soggetti a sospensioni che hanno acconsentito al recapito dei messaggi (tramite chiamata API o shim di compatibilità, descritto più avanti). Dopo alcuni secondi di ritardo, DAM sospende il processo.

Non sono presenti notifiche quando la limitazione delle richieste di dighe è attivata o disattivata. I processi non devono essere modificati; i processi continuano a funzionare, sebbene a una velocità più lenta.

## <a name="manifestation"></a>Manifestazione

I processi vengono spesso sospesi o limitati durante lo stato di standby connesso. Per la maggior parte delle app sospese, questa operazione dovrebbe essere molto simile a una transizione di sospensione/ripresa o di ibernazione S4/resume di S3. Le manifestazioni possono includere, tra l'altro, le incoerenze in fase di esecuzione e di runtime rispetto a quella del clock, le incoerenze nel comportamento del timer o modifiche sostanziali nello stato del sistema operativo prima e dopo il completamento della sospensione.

La sospensione e la limitazione si verificano come un'unità (tutti i processi sospesi vengono sospesi e non sospesi all'unisono e tutti i processi che possono essere limitati sono limitati e non limitati), pertanto la comunicazione tra due processi sospesi o due processi limitati non costituisce un problema.

Il software che si basa sulla comunicazione tra processi potrebbe richiedere particolare attenzione:

-   **Comunicazione tra processi nella sessione 0 (limitata) e sessione 1 + (sospesa)** : gli esempi includono icone della barra o componenti dell'interfaccia utente che rappresentano lo stato del servizio corrente
-   **Comunicazione tra componenti in modalità utente (sessione 0 o 1) e driver (che non sono limitati o sospesi)** : alcuni esempi includono servizi che funzionano per conto di un driver

In questi casi, se la comunicazione tra processi non viene gestita correttamente, le app possono apparire bloccate o non rispondenti (anche se l'utente potrebbe non visualizzare direttamente questo effetto, perché lo schermo sarà disattivato in modalità standby connessa). Nella maggior parte dei casi, tuttavia, i servizi e i driver devono essere già sviluppati in modo da essere affidabili contro i problemi di comunicazione tra processi.

I fornitori che creano software per o che dipendono dal Web devono considerare il modo in cui la sospensione del processo influiscono sulle durate e sugli handshake della connessione. Inoltre, dal momento che la connettività di rete potrebbe non essere disponibile in modalità standby connessa, gli sviluppatori di processi creati nella sessione 0 devono essere particolarmente consapevoli del modo in cui le connessioni di rete intermittenti interessano il processo.

## <a name="solution"></a>Soluzione

La diga non ha alcun effetto sulle app di Windows Store. Se l'applicazione desktop è interessata dalla diga, è possibile richiedere le notifiche prima che la sospensione sia attiva, ad esempio per salvare lo stato o chiudere le connessioni di rete, usando uno dei metodi seguenti:

-   Se l'app ha una finestra (HWND) e si vuole gestire queste notifiche tramite la procedura della finestra, chiamare [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) per eseguire la registrazione per questi messaggi (o [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) per annullare la registrazione). È possibile usare \_ l'handle di finestra notifica del dispositivo \_ \_ nel parametro flags e passare il HWND della finestra in come parametro del destinatario. Il messaggio ricevuto è il \_ messaggio WM POWERBROADCAST.
-   Se l'app non ha una finestra (HWND) o si vuole un callback diretto, chiamare [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) per eseguire la registrazione per questi messaggi (o [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) per annullare la registrazione). È necessario usare \_ \_ il callback di notifica del dispositivo nel parametro flags e passare un valore di tipo PDEVICE \_ Notify \_ Subscribe \_ Parameters nel parametro del destinatario.
-   Se non è possibile ricompilare l'app, è possibile acconsentire esplicitamente a ricevere questi \_ messaggi WM POWERBROADCAST tramite [AppCompat Toolkit](../win7appqual/application-compatibility-toolkit--act-.md) (usando lo shim PromoteDAM).

Il messaggio di sospensione è WM \_ POWERBROADCAST con wParam = PBT \_ APMSUSPEND; questo messaggio viene trasmesso simultaneamente a tutti i processi prescelti nel sistema. L'app deve eseguire operazioni sul percorso di sospensione in modo rapido ed efficiente. Il timeout dopo la notifica di broadcast è globale, non per processo, quindi il processo potrebbe essere in conflitto con le risorse di sistema se il lavoro richiesto in questo percorso è esteso.

Il messaggio di ripresa è WM \_ POWERBROADCAST con wParam = PBT \_ APMRESUME; questo messaggio viene trasmesso simultaneamente a tutti i processi scelti dopo una ripresa. Il tempo relativo di recapito all'uscita del sistema dalla modalità standby connessa non è garantito.

Per le applicazioni correlate alla fotocamera, quando viene effettuata la transizione dello stato di alimentazione, durante la notifica di sospensione, le applicazioni devono rilasciare tutti i riferimenti alla fotocamera (tutti gli oggetti della pipeline di acquisizione devono essere arrestati ed eliminati).  Per evitare il possibile svuotamento della batteria, in Windows 10 RS3 + System Windows fotocamera Frame Server Service chiuderà tutte le sessioni di acquisizione se l'applicazione non gestisce correttamente la notifica di sospensione.  L'effetto collaterale è che, quando il sistema esce dallo stato standby o S3/S4, la pipeline di acquisizione dell'applicazione non è più in uno stato attivo.

## <a name="tests"></a>Test

Testare il software tra le transizioni di standby connesse.

## <a name="resources"></a>Risorse

-   [Soluzioni per la durata della batteria mobile per Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [\_funzionalità di alimentazione del sistema \_](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [CallNtPowerInformation (funzione)](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Oggetti processo](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Toolkit AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 