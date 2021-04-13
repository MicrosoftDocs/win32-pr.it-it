---
title: Manutenzione automatica (Utilità di pianificazione)
description: L'attività di manutenzione si riferisce a un'applicazione o a un processo che consente di mantenere l'integrità e le prestazioni di un computer Windows.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2020
ms.locfileid: "104399873"
---
# <a name="automatic-maintenance"></a>Manutenzione automatica

L'attività di manutenzione si riferisce a un'applicazione o a un processo che consente di mantenere l'integrità e le prestazioni di un computer Windows. La manutenzione include l'aggiornamento del sistema operativo Windows (OS) e delle applicazioni, il controllo della sicurezza e l'esecuzione di analisi per il malware. Gestione automatica Windows (WAM) è una serie di miglioramenti apportati all'API Utilità di pianificazione che è possibile utilizzare per collegare le applicazioni alla pianificazione della manutenzione di Windows. In particolare, WAM consente di aggiungere attività che richiedono una pianificazione regolare, ma che non hanno requisiti di tempo esatti. Al contrario, WAM si basa sul sistema operativo per scegliere il momento appropriato per attivare l'attività nel corso della giornata. Il sistema sceglie tali orari in base a un effetto minimo sull'utente, sulle prestazioni del PC e sull'efficienza energetica.

## <a name="how-scheduled-maintenance-works"></a>Funzionamento della manutenzione pianificata

Utilità di pianificazione attività di manutenzione sono attività opportunistiche che vengono eseguite quando il computer è inattivo e alimentato da AC. Uno degli obiettivi principali delle attività di manutenzione è ridurre al minimo l'effetto sul computer pianificando la manutenzione solo quando il computer è collegato alla rete elettrica e inattiva (ovvero, quando non si usa o si è ricavato da, il computer). Il concetto di manutenzione odierna è che il computer funzioni con la minor interferenza per l'utente. Di conseguenza, per sfruttare i vantaggi di questi periodi di inattività, è stata migliorata l'ora di manutenzione di tipo obsoleto (si parlerà di questo aspetto nella sezione **manutenzione automatica della manutenzione &mdash; giornaliera** più avanti in questo argomento). Mentre l'ora di manutenzione può ancora essere sfruttata, l'esecuzione di una manutenzione opportunistica è migliore per l'integrità del sistema.

L'attività potrebbe non riuscire se un computer non impiega molto tempo sia inattivo che su alimentazione AC. Assicurarsi che lo scenario fornisca ancora valore all'utente, anche se è in ritardo. Se l'utente usa attivamente il computer, il sistema rinvia la manutenzione fino a un momento successivo. Il sistema sospende anche eventuali attività di manutenzione in esecuzione se l'utente torna a usare il PC.

Il sistema riavvia un'attività di manutenzione sospesa durante il periodo di inattività successivo. Tuttavia, il sistema non sospende alcuna attività contrassegnata come critica. Al contrario, il sistema consente il completamento di un'attività critica, indipendentemente dall'azione dell'utente.

A causa della natura della pianificazione, alcune attività pianificate potrebbero non essere completate: probabilmente ci sono troppi eventi pianificati per adattarsi alla finestra di manutenzione di 1 ora o forse il computer non è stato semplicemente acceso. In questi casi, è possibile definire un'attività con una scadenza. Una scadenza viene definita come un intervallo di tempo ricorrente in cui il sistema deve eseguire correttamente l'attività almeno una volta.

Se un'attività non riceve una scadenza, l'utilità di pianificazione di manutenzione continuerà a tentare di eseguire l'attività durante la finestra di manutenzione. Inoltre, l'utilità di pianificazione non si limiterà al limite di tempo di 1 ora. Al contrario, l'utilità di pianificazione estende la durata della finestra di manutenzione per completare l'attività ritardata.

Una volta che il sistema ha completato l'attività (anche con un codice di errore di errore), il tentativo viene considerato riuscito. Dopo un tentativo di esito positivo, l'utilità di pianificazione Reimposta la pianificazione di manutenzione regolare e tenterà l'attività durante il periodo successivo.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Attivazione automatica manutenzione &mdash; giornaliera

In Windows 7, un'attività di manutenzione viene eseguita esclusivamente durante l' *ora di manutenzione*, per impostazione predefinita le 3 AM e può essere configurata tramite criteri di gruppo. Il computer viene riattivato dalla modalità standby, esegue le attività di manutenzione e torna alla modalità sospensione. Questa sessione giornaliera è stata limitata a una durata massima di 1 ora per tentativo. Questo consentirebbe al sistema di eseguire la manutenzione quotidianamente, a partire dalle 3:00 per impostazione predefinita. Si noti che l'utente può ripianificare l'ora di attivazione della manutenzione tramite la configurazione di queste impostazioni.

Con l'avvento dei portatili e il grande interesse per la durata della batteria, i computer non sono più configurati per consentire la riattivazione S3 nella maggior parte dei casi e, in genere, di sospensione (ibernazione) non appena possibile, per risparmiare la batteria. In risposta a queste modifiche, Utilità di pianificazione (> Win7) esegue le attività di manutenzione quando sono dovute e il computer è inattivo e alimentato da AC.

Questa impostazione può essere configurata nel pannello di controllo.

Aprire il **Pannello**  >  **di controllo sistema e** sicurezza  >  **e manutenzione** manutenzione  >  **automatica**.

Quindi, a seconda del modo in cui vengono configurati i computer e le attività, il comportamento di riattivazione giornaliera potrebbe non verificarsi come previsto a causa di questa nuova configurazione. È possibile determinare prima di tutto se il computer è compatibile con S3 o se è in grado di supportare CS (Connected standby).
Questa operazione può essere eseguita aprendo un prompt di Power Shell con privilegi elevati ed eseguendo il comando seguente.

```console
powercfg /a
```

Ora di manutenzione, se il computer è configurato correttamente, funziona comunque, ma in caso contrario
  - Controllare le impostazioni del BIOS per le impostazioni di riattivazione. 
  - Controllare se l'opzione Consenti timer di riattivazione è abilitata in Opzioni risparmio energia.
    Passare a **Pannello di controllo**  >  **hardware e suoni**  >  **Opzioni risparmio energia** modificare  >  **impostazioni piano**  >  **Modifica impostazioni risparmio energia avanzate** > fare clic su **sospensione**  >  **Consenti timer di riattivazione**.
  - Controllare se l'attività pianificata è configurata con il codice seguente.
      * MaintenanceSettings: l'attività deve essere configurata con un periodo, una scadenza.
      * Enabled: l'attività deve essere abilitata.
      * WakeToRun: l'attività deve essere autorizzata a riattivare il computer.
  - Per la pianificazione delle riattivazioni da CS, il computer deve essere in grado di supportare AOAC.
  - Per la pianificazione delle riattivazioni nei computer S3,
      * Controllare se il computer è stato inserito in S3 sull'alimentazione AC.
      * Per la manutenzione del sistema deve essere **abilitata la riattivazione** in criteri di gruppo.
 
Standby connesso è lo stato del sistema che può essere inserito da un sistema conforme a AOAC.

Vedere differenze tra Modern standby e S3 nell'argomento [Modern standby vs S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definizione di un'attività di manutenzione automatica

È possibile convertire qualsiasi attività Utilità di pianificazione in un'attività di manutenzione. A tale scopo, è necessario verificare che l'applicazione possa essere sospesa. Quindi, è necessario estendere la definizione di attività con i nuovi elementi [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) e [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) .

La preoccupazione principale della creazione di un'attività di manutenzione consiste nel garantire che il sistema sia in grado di sospendere e riavviare l'attività. È probabile che il sistema sospenda più volte un'attività di manutenzione; Pertanto, è necessario assicurarsi che l'applicazione sia in grado di salvare il proprio stato e quindi riprendere in un momento arbitrario. In questo modo si garantisce che il sistema non esegua più volte la stessa parte dell'attività.

Dopo aver verificato che l'applicazione possa essere sospesa e ripresa normalmente, è possibile usare gli elementi **MaintenanceSettings** e **AllowStartOnDemand** per definire la pianificazione. **MaintenanceSettings** viene definito in base a periodo, scadenza ed esclusività.

-   Il **periodo** è obbligatorio e definisce la frequenza con cui l'attività deve essere eseguita. In genere, questo è definito in termini di ciclo di più giorni, ad esempio "una volta ogni 5 giorni". Un periodo deve essere di almeno un giorno, pertanto non è possibile pianificare l'esecuzione di un'attività più volte in un giorno.
-   La **scadenza** è facoltativa e definisce per quanto tempo l'utilità di pianificazione può non riuscire a completare l'attività prima di inviare una notifica all'utente o di eseguire una manutenzione di emergenza. La scadenza deve essere superiore a quella del periodo, vale a dire che il sistema deve avere la possibilità di provare l'attività almeno una volta prima di inviare una notifica all'utente.
-   Inoltre, un'attività di manutenzione può essere facoltativamente definita come *esclusiva*. Un'attività esclusiva viene eseguita separatamente da altre attività di manutenzione. In genere, un'attività esclusiva prevede l'uso di una grande quantità di risorse, ad esempio un tempo di CPU elevato o l'accesso esclusivo a un database. Prima di avviare un'attività esclusiva, il sistema completa tutte le attività di manutenzione non esclusive. Pertanto, è necessario dichiarare un'attività come esclusiva solo quando necessario.

Al contrario, **AllowStartOnDemand** indica semplicemente che il sistema o l'utente può avviare l'attività in qualsiasi momento. Ciò consente al sistema di avviare l'attività durante la normale manutenzione. In caso contrario, sarebbe necessario impostare un trigger univoco per l'attività.
