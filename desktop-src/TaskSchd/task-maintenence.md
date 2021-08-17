---
title: Manutenzione automatica (Utilità di pianificazione)
description: L'attività di manutenzione si riferisce a un'applicazione o a un processo che consente di mantenere l'integrità e le prestazioni di Windows PC.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43fe72159ac5fd14c2dcc80126e572fa1475ed52ffd5710b74621cf00ad40a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139304"
---
# <a name="automatic-maintenance"></a>Manutenzione automatica

L'attività di manutenzione si riferisce a un'applicazione o a un processo che consente di mantenere l'integrità e le prestazioni di Windows PC. La manutenzione include la Windows del sistema operativo e delle applicazioni, il controllo della sicurezza e l'esecuzione di analisi della presenza di malware. Windows La gestione automatica (WAM) è un set di miglioramenti apportati all'API Utilità di pianificazione che è possibile usare per collegare le applicazioni alla pianificazione Windows manutenzione. In particolare, WAM consente di aggiungere attività che richiedono una pianificazione regolare, ma che non hanno requisiti di tempo esatti. WAM si basa invece sul sistema operativo per scegliere l'ora appropriata per attivare l'attività nel corso della giornata. Il sistema sceglie questi orari in base all'impatto minimo sull'utente, sulle prestazioni del PC e sull'efficienza energetica.

## <a name="how-scheduled-maintenance-works"></a>Funzionamento della manutenzione pianificata

Utilità di pianificazione attività di manutenzione sono attività opportunistiche eseguite quando il computer è inattivo e alimentato da CA. Uno degli obiettivi principali delle attività di manutenzione è ridurre al minimo l'impatto sul PC pianificando la manutenzione solo quando il PC è collegato all'alimentazione CA e inattivo (ovvero quando non si usa o si è allontanato dal computer). L'idea di manutenzione oggi è che la macchina funzioni con la minima interruzione per l'utente. Di conseguenza, l'ora di manutenzione precedente **&mdash;** (di cui si parla più avanti nella sezione Riattivazione giornaliera della manutenzione automatica più avanti in questo argomento) è stata migliorata per poter sfruttare questi periodi di inattività. Anche se l'ora di manutenzione può ancora essere sfruttata, l'esecuzione della manutenzione opportunistica è migliore per l'integrità del sistema.

L'attività potrebbe essere affamata se un computer non dedica molto tempo sia all'inattività che all'alimentazione CA. Assicurarsi che lo scenario fornirà comunque valore all'utente, anche se è ritardato. Se l'utente usa attivamente il computer, il sistema rinvia la manutenzione fino a un secondo momento. Il sistema sospende anche qualsiasi attività di manutenzione in esecuzione se l'utente torna a usare il PC.

Il sistema riavvia un'attività di manutenzione sospesa durante il periodo di inattività successivo. Tuttavia, il sistema non sospende alcuna attività contrassegnata come critica. Al contrario, il sistema consente il completamento di un'attività critica, indipendentemente dall'azione dell'utente.

A causa della natura della pianificazione, alcune attività pianificate potrebbero non essere completate: forse sono presenti troppi eventi pianificati per rientrare nella finestra di manutenzione di 1 ora o forse il computer non è stato semplicemente acceso. In questi casi, è possibile definire un'attività con una scadenza. Una scadenza è definita come un intervallo di tempo ricorrente in cui il sistema deve eseguire correttamente l'attività almeno una volta.

Se un'attività non raggiunge una scadenza, l'utilità di pianificazione della manutenzione continuerà a tentare di eseguire l'attività durante la finestra di manutenzione. Inoltre, l'utilità di pianificazione non si limiterà al normale limite di 1 ora. L'utilità di pianificazione estende invece la durata della finestra di manutenzione per completare l'attività posticipata.

Dopo che il sistema ha completato l'attività (anche con un codice di errore), il tentativo viene considerato riuscito. Dopo un tentativo riuscito, l'utilità di pianificazione reimposta la normale pianificazione di manutenzione e tenterà l'attività durante il periodo successivo.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Riattivazione &mdash; giornaliera della manutenzione automatica

Nella Windows 7 un'attività di manutenzione viene eseguita esclusivamente durante l'ora di *manutenzione,* per impostazione predefinita alle 3:00 e configurabile tramite Criteri di gruppo. Il computer si riattiva dalla modalità standby, esegue attività di manutenzione e torna alla sospensione. Questa sessione giornaliera è stata limitata a una durata massima di 1 ora per tentativo. In questo modo il sistema può eseguire la manutenzione ogni giorno, a partire dalle 3:00 per impostazione predefinita. Si noti che l'utente può pianificare nuovamente l'ora in cui viene attivata la manutenzione configurando queste impostazioni.

Con l'avvento dei portatili e la grande attenzione alla durata della batteria, i computer non sono più configurati per consentire la riattivazione S3 nella maggior parte dei casi e, in genere, doze-to-S4 (ibernazione) appena possibile, per risparmiare batteria. In risposta a queste modifiche, Utilità di pianificazione (> Win7) esegue attività di manutenzione ogni volta che sono dovute e il computer è inattivo e alimentato da CA.

Questa impostazione può essere configurata in Pannello di controllo.

Aprire **Pannello di controllo**  >  **sistema e sicurezza**  >  **Sicurezza e manutenzione**  >  **Manutenzione automatica**.

Quindi, in base alla configurazione dei computer e delle attività, il comportamento di riattivazione giornaliera potrebbe non verificarsi oggi come previsto a causa di questa nuova configurazione. È prima di tutto possibile determinare se il computer supporta S3 o CS (Connected Standby).
A tale scopo, aprire un prompt di Power Shell con privilegi elevati ed eseguire il comando seguente.

```console
powercfg /a
```

Ora di manutenzione, se il computer è configurato correttamente, funziona ancora, ma in caso contrario,
  - Controllare le impostazioni del BIOS per le impostazioni di riattivazione. 
  - Controllare se l'opzione Consenti timer di riattivazione è abilitata in Opzioni risparmio energia.
    Passare **a** Pannello di controllo hardware e audio Opzioni risparmio energia Modifica piano Impostazioni impostazioni avanzate di risparmio energia > fare clic su Sospensione  >    >    >    >     >  **Consenti timer riattivazione.**
  - Controllare se l'attività pianificata è configurata con quanto segue.
      * MaintenanceSettings: l'attività deve essere configurata con Periodo, Scadenza.
      * Abilitato: l'attività deve essere abilitata.
      * WakeToRun: l'attività deve essere autorizzata a riattivare il computer.
  - Per la pianificazione delle riattivazioni da CS, il computer deve essere in grado di AOAC.
  - Per la pianificazione delle riattivazioni nei computer S3,
      * Controllare se la macchina è passata a S3 con l'alimentazione CA.
      * Nel sistema deve essere **abilitata la riattivazione** Criteri di gruppo manutenzione.
 
Connected Standby è lo stato del sistema che può essere immesso da un sistema conforme a AOAC.

Vedere le differenze tra Modern Standby e S3 nell'argomento [Modern Standby vs S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definizione di un'Manutenzione automatica personalizzata

È possibile convertire qualsiasi attività Utilità di pianificazione in un'attività di manutenzione. A tale scopo, è necessario verificare che l'applicazione possa essere sospesa. È quindi necessario estendere la definizione dell'attività con i [**nuovi elementi MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) [**e AllowStartOnDemand.**](taskschedulerschema-allowstartondemand-settingstype-element.md)

Il problema principale della creazione di un'attività di manutenzione è garantire che il sistema possa sospendere e riavviare l'attività. È probabile che il sistema sospende un'attività di manutenzione più volte. Pertanto, è necessario assicurarsi che l'applicazione sia in grado di salvare il proprio stato e quindi riprendere in un momento arbitrario. Ciò garantisce che il sistema non eserciti ripetutamente la stessa parte dell'attività.

Dopo aver garantito che l'applicazione può essere sospesa e ripresa normalmente, è possibile usare gli elementi **MaintenanceSettings** e **AllowStartOnDemand** per definire la pianificazione. **MaintenanceSettings** viene definito in base al periodo, alla scadenza e all'esclusività.

-   Il **periodo** è obbligatorio e definisce la frequenza con cui deve verificarsi l'attività. In genere, questo valore viene definito in termini di ciclo di più giorni, ad esempio "una volta ogni 5 giorni". Un periodo deve essere di almeno un giorno, vale a dire che non è possibile pianificare un'attività in modo che si verifichi più volte al giorno.
-   La **scadenza è** facoltativa e definisce per quanto tempo l'utilità di pianificazione può non riuscire a completare l'attività prima di inviare una notifica all'utente o di eseguire una manutenzione di emergenza. La scadenza deve essere più lunga del periodo, vale a dire che il sistema deve avere la possibilità di tentare l'attività almeno una volta prima di inviare una notifica all'utente.
-   Inoltre, un'attività di manutenzione può essere definita facoltativamente come *esclusiva.* Un'attività esclusiva viene eseguita separatamente da altre attività di manutenzione. In genere, un'attività esclusiva usa una grande quantità di risorse, ad esempio una grande quantità di tempo di CPU o l'accesso esclusivo a un database. Il sistema completa tutte le attività di manutenzione non esclusive prima di avviare un'attività esclusiva. Pertanto, è necessario dichiarare un'attività come esclusiva solo quando necessario.

Al contrario, **AllowStartOnDemand** indica semplicemente che il sistema o l'utente può avviare l'attività in qualsiasi momento. Ciò consente al sistema di avviare l'attività durante la manutenzione regolare. In caso contrario, è necessario impostare un trigger univoco per l'attività.
