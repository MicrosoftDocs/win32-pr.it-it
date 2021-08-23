---
title: Desktop Activity Moderator
description: Desktop Activity Moderator
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- durata della batteria
- standby connesso
- Sospensione
- limitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b465bbb377a06fdad50d04d5fcf788cb2e687fdf5db852125e4143fd971773d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815421"
---
# <a name="desktop-activity-moderator"></a>Desktop Activity Moderator

## <a name="platform"></a>Piattaforma

**Client** : Windows 8 


> [!Note]  
> La gestione delle applicazioni livello dati è presente solo in Windows 8 client che supportano lo standby connesso. La gestione delle applicazioni livello dati non è presente sugli SKU del server.

 

  

> [!Note]  
> Windows Le app dello Store Windows 8 non sono influenzate dalla gestione delle applicazioni livello dati.

 

  
</dl>

## <a name="description"></a>Descrizione

I clienti si stanno spostando verso piattaforme mobili più leggere, più piccole e più grandi per soddisfare le proprie esigenze di calcolo. Nell'ambito del passaggio ai dispositivi mobili, gli utenti sono sempre più interessati alla durata della batteria dei dispositivi. Desktop Activity Moderator (DAM) è una delle numerose nuove funzionalità di Windows 8 progettate per garantire una durata della batteria coerente e lunga per i dispositivi che supportano lo standby connesso.

Lo standby connesso si verifica quando il dispositivo è acceso, ma lo schermo è spento. In questo stato di alimentazione, il sistema è tecnicamente sempre "attivo" (per supportare scenari chiave come posta elettronica, VoIP, social networking e messaggistica istantanea con le app di Windows Store). È analogo allo stato in cui si trova uno smartphone quando l'utente preme il pulsante di alimentazione.

Di conseguenza, il software (incluse le app e il software del sistema operativo) deve essere ben comportato durante la modalità standby connessa. La gestione delle applicazioni livello dati è stata creata per eliminare l'esecuzione dell'app desktop in modo simile allo stato Sospensione (S3 nei dispositivi ACPI). A tale scopo, sospende o limita i processi del software desktop nel sistema al momento della connessione di standby. In questo modo i sistemi che supportano lo standby connesso possono offrire un utilizzo ridotto delle risorse e una durata della batteria lunga e coerente, consentendo alle app di Windows Store di offrire le esperienze connesse che si offrono.

## <a name="details"></a>Dettagli

Dam è un driver in modalità kernel che viene caricato e inizializzato all'avvio del sistema se il sistema supporta lo standby connesso. Questo è determinato dalla valutazione se il campo AOAC in SYSTEM \_ La \_ struttura POWER CAPABILITIES restituita da CallNtPowerInformation è impostata su TRUE).

Quando la gestione delle applicazioni livello dati è abilitata e viene creato il processo desktop, aggiunge il processo agli oggetti processo gestiti dal sistema:

-   Se il processo è stato creato nella sessione 0, DAM aggiunge il processo a un oggetto processo soggetto a **limitazione**
-   Se il processo è stato creato in una sessione interattiva (sessione 1 o successiva), DAM aggiunge il processo a un oggetto processo soggetto a **sospensione**

> [!Note]  
> Ad Windows 8, gli oggetti processo possono essere annidati. Ciò significa che l'utilizzo degli oggetti processo da parte dell'applicazione livello dati non interferisce con l'utilizzo esistente di oggetti processo da parte di un'app.

 

Quando la schermata è visualizzata, la gestione delle applicazioni livello dati viene disattivata e non influisce sui processi nel sistema. Quando il sistema è in standby connesso, a seconda dell'attività del sistema, DAM potrebbe limitazione o sospensione dei processi.

-   I processi soggetti a sospensione hanno tutti i thread sospesi (non è consentita l'esecuzione in alcuna circostanza); lo stato dell'app (memoria del processo) viene mantenuto
-   Processi soggetti a ciclo di limitazione tra sospeso e non sospeso (gran parte del tempo viene impiegato nello stato sospeso)
    -   Tenere presente che Windows anche rilevare che si verificano attività critiche e potrebbe annullare la sospensione dei servizi con limitazione per periodi di tempo più lunghi durante questa attività
    -   Si noti anche che, mentre è in standby connesso, i sensori e le reti potrebbero non essere disponibili, quindi i processi con limitazione devono essere progettati in modo da essere resilienti alle condizioni di rete non ottimali (per la maggior parte dei processi, ciò non richiede alcuna modifica)

Quando la sospensione DAM è attivata o disassegnata, DAM attiva il recapito di un messaggio POWERBROADCAST WM a tali processi soggetti a sospensione che hanno acconsentito esplicitamente al recapito dei messaggi (tramite shim di compatibilità o chiamata API, descritto più \_ avanti). Dopo alcuni secondi di ritardo, DAM sospende il processo.

Non vengono inviate notifiche quando la limitazione della larghezza di banda della rete DAM è inattiva o non è disponibile. Non è necessario apportare modifiche ai processi. I processi continuano a funzionare, anche se a una velocità più lenta.

## <a name="manifestation"></a>Manifestazione

I processi vengono spesso sospesi o limitate durante lo stato di standby connesso. Per la maggior parte delle app sospese, questo dovrebbe essere molto simile a una transizione di sospensione/ripresa S3 o Ibernazione/ripresa S4. Le incoerenze possono includere, ad esempio, incoerenze nel tempo di attività/runtime rispetto al tempo di esecuzione, incoerenze nel comportamento del timer o modifiche notevoli dello stato del sistema operativo prima e dopo il completamento della sospensione.

La sospensione e la limitazione si verificano come unità (tutti i processi sospendibili vengono sospesi e non sospesi all'unisono e tutti i processi che possono essere limitate sono limitate e non limitate in unisono), quindi la comunicazione tra due processi sospesi o due processi con limitazione non costituisce un problema.

Il software che si basa sulla comunicazione tra processi potrebbe richiedere particolare attenzione:

-   Comunicazione tra i processi nella sessione 0 (con limitazione) e nella sessione **1+ (sospesa):** esempi includono icone della barra delle applicazioni o componenti dell'interfaccia utente che rappresentano lo stato corrente del servizio
-   Comunicazione tra componenti in modalità utente **(sessione 0 o 1)** e driver (che non sono né limitate né sospese), ad esempio servizi che funzionano per conto di un driver

In questi casi, se la comunicazione tra processi non viene gestita correttamente, le app possono apparire bloccata o non rispondere (anche se l'utente potrebbe non vedere direttamente questo impatto, perché lo schermo si spegne quando è in standby connesso). Nella maggior parte dei casi, tuttavia, i servizi e i driver devono essere già sviluppati per essere affidabili in caso di problemi di comunicazione tra processi.

I fornitori che creano software per o dipendono dal Web devono considerare in che modo la sospensione del processo influisce sulla durata della connessione e sugli handshake. Inoltre, poiché la connettività di rete potrebbe non essere disponibile in modalità standby connesso, gli sviluppatori di processi creati nella sessione 0 devono essere particolarmente consapevoli del modo in cui le connessioni di rete intermittenti influiscono sul processo.

## <a name="solution"></a>Soluzione

Windows Le app dello Store non sono influenzate dalla gestione delle applicazioni livello dati. Se l'app desktop è influenzata dalla gestione delle applicazioni livello dati, è possibile richiedere notifiche prima dell'avvio della sospensione (ad esempio, per salvare lo stato o chiudere le connessioni di rete) usando uno dei metodi seguenti:

-   Se l'app ha una finestra (HWND) e vuoi gestire queste notifiche tramite la procedura della finestra, chiama [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) per eseguire la registrazione per questi messaggi (o [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) per annullare la registrazione). È possibile usare DEVICE NOTIFY WINDOW HANDLE nel parametro Flags e \_ passare HWND della finestra \_ come parametro \_ Recipient. Il messaggio ricevuto è il messaggio WM \_ POWERBROADCAST.
-   Se l'app non ha una finestra (HWND) o si vuole un callback diretto, chiamare [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) per eseguire la registrazione per questi messaggi (o [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) per annullare la registrazione). È necessario usare DEVICE NOTIFY CALLBACK nel parametro Flags e passare un valore di \_ \_ tipo PDEVICE NOTIFY SUBSCRIBE \_ PARAMETERS nel parametro \_ \_ Recipient.
-   Se l'app non può essere ricompilata, è possibile acconsentire esplicitamente a ricevere questi messaggi POWERBROADCAST WM tramite il \_ [toolkit AppCompat](../win7appqual/application-compatibility-toolkit--act-.md) (usando lo shim PromoteDAM).

Il messaggio di sospensione è WM \_ POWERBROADCAST con wParam=PBT APMSUSPEND. Questo messaggio viene trasmesso simultaneamente a tutti i processi con consenso esplicito \_ nel sistema. L'app deve eseguire qualsiasi operazione sul percorso di sospensione in modo rapido ed efficiente. Il timeout dopo la notifica di trasmissione è globale, non per processo, quindi il processo potrebbe essere in contesa per le risorse di sistema se il lavoro richiesto in questo percorso è esteso.

Il messaggio di ripresa è WM \_ POWERBROADCAST con wParam=PBT APMRESUME. Questo messaggio viene trasmesso simultaneamente a tutti i processi con consenso esplicito dopo un \_ ripresa. L'ora di recapito relativa all'uscita dal sistema dalla modalità standby connessa non è garantita.

Per le applicazioni correlate alla fotocamera, quando si verifica la transizione dello stato di alimentazione, durante la notifica di sospensione, le applicazioni devono rilasciare tutti i riferimenti alla fotocamera (tutti gli oggetti della pipeline di acquisizione devono essere arrestati ed eliminati).  Per evitare un possibile svuotamento della batteria, nei sistemi Windows 10 RS3+ il servizio Fotocamera Windows Frame Server chiuderà tutte le sessioni di acquisizione se l'applicazione non gestisce correttamente la notifica di sospensione.  L'effetto collaterale è che quando il sistema esce dallo stato standby o S3/S4, la pipeline di acquisizione dell'applicazione non è più in uno stato di lavoro.

## <a name="tests"></a>Test

Testare il software tra transizioni di standby connesse.

## <a name="resources"></a>Risorse

-   [Soluzioni di durata della batteria per Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [FUNZIONALITÀ DI \_ ALIMENTAZIONE \_ DEL SISTEMA](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [Funzione CallNtPowerInformation](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Oggetti processo](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Toolkit AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 